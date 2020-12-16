+++
author = "Kevin Kopp"
title = "Event Listeners (Éxperience)"
date = "2020-12-04"
description = "Petit point théorique sur les event listeners"
tags = [
    "js",
    "DOM",
    "html"
]
+++

Aujourd'hui, j'ai envie de m'attaquer aux event listeners. Les eventListener permettent écouter tous les événements qui ont lieu sur une page web. On pourrait se dire que c'est assez basique et qu'il n'a pas grand chose à savoir, mais c'est un sujet qui peut se complexifier assez rapidement. 

{{< youtube Q6HAJ6bz7bY >}}

<br>

Je suis de bonne humeur et souhaite donc me pencher sur une petite expérience qui est les event Bubbling et Capturing. Je souhaite traiter ce sujet en faisant une expérience, car c'est une partie théorique qui peut souvent porter à confusion chez de nombreux programmeurs.

### Capturing and bubbling

Nous avons le code suivant : 

{{< highlight javascript >}}

little.addEventListener("click", e => {
    console.log("little")
})

middle.addEventListener("click", e => {
    console.log("middle")
})

big.addEventListener("click", e => {
    console.log("big")
}, {capture : true})

{{< /highlight >}}

il est accompagné d'un html qui nous donne le rendu suivant:

![Example image](/static/rectangle.PNG)

Nous pouvons voir que nous avons un event listener sur chacun des carré, du jaune (little) au grand carré rouge (big). En tant normal, si je clique sur le carré jaune, les 3 éléments vont écrire leur message dans la console. Cependant, si nous regardons le code javascript de plus prêt nous voyons un second paramètre sur l'élément big qui est "capture : true". Il faut savoir que lorsqu'on clique sur un élément, il y a 2 phases qui se déclenchent. La première qui est le capturing. Si je clique sur l'élément jaune, la phase de capturing va passer sur tous les éléments qui englobent le petit carré. C'est-à-dire qu'il va tout d'abord passer sur le document lui-même, puis sur l'élément big, puis middle puis enfin sur l'élément little, donc le carré jaune. En tant, normal, on ne remarque pas cela, car le capturing n'est pas activé. Sur le code ci-dessus, j'ai mis la capture a true, ce qui donne le résultat suivant dans la console :

![Example image](/static/console.PNG)

On peut voir qu'en cliquant sur l'élément little, il m'affiche d'abord l'élément big, car sur l'élément big la capture est activé. Cependant, dans la deuxième phase qui s'appelle bubbling, l'élément big ne s'affiche pas, car il a déjà été activé dans la phase de capturing.

J'ai trouvé intéressant de faire cette petite expérience avec les event listeners, car il peut arriver qu'on ne comprenne pas son comportement, car il est plus compliqué que l'on pense.






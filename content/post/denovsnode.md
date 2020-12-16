+++
author = "Kevin Kopp"
title = "node vs deno"
date = "2020-12-10"
description = "Quelles sont les réelles différences entre ces deux js runtimes?"
tags = [
    "deno",
    "node",
    "backend",
    "js"
]
+++

Dans cet article je souhaite aborder les différences qui existent entre node et deno et pour quelle option on devrait opter si l'on souhaite faire du full-stack.

{{< youtube 1gIiZfSbEAE >}}

</br>

Afin de mettre un contexte autour de ces deux runtimes il est important de préciser qu'ils ont été développés par la seul et même personne, Ryan Dahl. Lors d'une conférence en 2018, Ryan Dahl parlait des 10 choses qu'il regrette à propos de node et annonça par la même occasion Deno. 

On entend beaucoup parler de Deno comme le runtime qui va révolutionner le monde du backend. En effet, Ryan avait pour but de ne pas reproduire les mêmes erreurs qu'il a pu faire avec Node et ainsi sortir un produit "parfait". Cependant, il faut faire attention, car bien que puissant, Deno n'est pas encore si parfait que ca. Alors oui, Deno supporte Typescript dans sa version vanilla, il permet d'accéder à l'objet window alors qu'on code en backend, et il n'a même plus besoin de npm et ses gros fichiers node_modules pour fonctionner. Cependant, le problème est que Deno ne permet pas d'importer son projet javascript fait sur Node. Le runtime étant très jeune, il y a très peu de fonctionnalités qui ont été ajoutées a Deno. C'est n'est donc pas une v2 de Node, mais une toute nouvelle façon de fonctionnalité qui les sépare en deux mondes différents. Ce qui est sur est que Deno à toutes les cartes en main pour réussir et trouver sa communauté de développeurs. Il faut juste lui laisser un peu de temps.
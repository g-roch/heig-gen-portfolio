# Portfolio *GEN* - 2020

***Auteur***: Gabriel Roch

***Pseudo `git`***: `g-roch`

[TOC]

## `Git` et `github`/`gitlab`

Pendant ce semestre, j'ai put voire une grande amélioration dans mon utilisation de `git`. Depuis quelques année déjà, j'utilise régulièrement `git`, pour mes laboratoires et mes projets personnels. J'avais donc déjà une bonne maîtrise de cet outils avant le début du cours de *GEN*, j'en ai donc profité (ainsi que du cours de *RES*) pour amélioré mon utilisation de cet outil.

### Utilisation d'avant le cours

Pour illustré les changements que j'ai apporté à mon utilisation de `git`, je vais prendre des exemples d'un projet personnel que j'ai commencé avant le début du semestre, et qui est encore en cours [^1] : https://github.com/HEIG-TS/heig-bot

Je faisais de temps à autres des commits un peu trop gros ([`b00bd84efcb9c2d0a0ebe0533bfd9cd5af72cc37`](https://github.com/HEIG-TS/heig-bot/commit/b00bd84efcb9c2d0a0ebe0533bfd9cd5af72cc37)), avec des messages pas clair sur l'utilité du commit ([`9349bc1c5aca2fad590e1953ce9c276657764082`](https://github.com/HEIG-TS/heig-bot/commit/9349bc1c5aca2fad590e1953ce9c276657764082)), voir même les deux à la fois ([`c966095fc83db95ac2132f2206e411e4d666cc8e`](https://github.com/HEIG-TS/heig-bot/commit/c966095fc83db95ac2132f2206e411e4d666cc8e))

J'ai donc mis un accent particulier à faire des commits plus petit et avec un message qui aide vraiment à la compréhension, comme vous pouvez le constater sur mes commit du [7 et 9 mars](https://github.com/HEIG-TS/heig-bot/commits/master).

### Utilisation en parallèle de *GEN*

#### Durant le cours de *PRO*

Durant ce projet nous avons essayer de faire de commit de taille raisonnable et avec des commentaires pertinent. Malheureusement, au fur et à mesure de notre avancement, nous avons perdu notre rigueur et nous nous retrouvons avec un projet contenant quelques commits de médiocre qualité : [https://github.com/HEIGVD-PRO-A-07/HEIGVD-PRO-A-07](https://github.com/HEIGVD-PRO-A-07/HEIGVD-PRO-A-07)

J'ai put constater le malheur qu'est d'avoir de tel commit lors de la fin du projet. En effet, nous avons constaté qu'un bug avait été introduit, malgré le fait que nous testions presque chaque commit.[^2] J'ai donc utilisé l'excellente commande `git bisect` pour trouver le commit ayant le bug, après être tomber sur plusieurs commits qui ne compilait pas, j'ai identifié le commit intégrant le bug, ([fce9e7ab8a87afdac4432cd229a41d4401dbca09](https://github.com/HEIGVD-PRO-A-07/HEIGVD-PRO-A-07/commit/fce9e7ab8a87afdac4432cd229a41d4401dbca09)) et constaté qu'avec plus de 250 lignes modifiées, cela ne permettait pas d'identifier rapidement la source du problème. J'ai donc appris l'utilité (voir la nécessité) d'avoir de petit commit qui ne modifie qu'une chose à la fois, ce que je n'hésiterais donc plus à imposé à mes partenaire de laboratoire.

#### Laboratoire



[^1]: Ce projet est bien sur en pause en ce moment au vu des restrictions actuelles sur GAPS.
[^2]: Nous n'avons malheureusement pas pu mettre en place de test automatiser, ce qui nous aurait sûrement permis d'évité ce bug.


# Portfolio *GEN* - 2020

***Auteur***: Gabriel Roch

***Pseudo `git`***: `g-roch`

***Identités avec lesquels des commits ont été faits***: 

- `Gabriel Roch <gabriel.roch@heig-vd.ch>`
- `Ciol Hcor <ciol@hcor.ch>`

-------

[TOC]

## Introduction

- Les liens vers les dépôts sont cliquable 
- Les références de commit sont des liens qui pointe directement sur le bon commit dans l'interface web de `github`
- Lors de la citation d'un logiciel, son nom est cliquable et pointe sur la page d'accueil du projet correspondant.

## `Git` et `github`

`Git ` est un logiciel de gestion de version de fichier texte. Il est également capable de gérer des fichiers binaires, mais ce n'est pas dans ce domaine qu'il excelle. Le gros avantage de `git` est sa rapidité dans les opérations courantes. Par exemples la création d'une branche ne prend que le temps de création d'un fichier sur le disque, c'est très rapide par rapport à d'autre système qui nécessite de copier l'intégralité des fichiers.

De plus la gestion de la fusion des branches est très performante, je n'ai que très rarement du faire un `merge` à la main. Même quand cela arrive, il y a des outils pratiques pour effectuer le `merge` (notamment : [`gitg`](https://wiki.gnome.org/Apps/Gitg/)). La recherche de commit introduisant un bug est facilité par la commande `git bisect` qui nous aide à faire une recherche dichotomique de notre commit à travers notre dépôt de code.

Depuis quelques années déjà, j'utilise régulièrement `git`, pour mes laboratoires et mes projets personnels. J'avais donc déjà une bonne maîtrise de cet outil avant le début du cours de *GEN*, j'en ai donc profité (ainsi que du cours de *RES*) pour amélioré mon utilisation de cet outil.

Cependant, comme n'importe quel logiciel, on n'en a pas forcément une bonne utilisation. J'ai pu voir une grande amélioration dans mon utilisation de `git` durant ce semestre, notamment sur ma manière de nommé mes commits.

### Utilisation d'avant le cours

Pour illustrer les changements que j'ai apporté à mon utilisation de `git`, je vais prendre des exemples d'un projet personnel que j'ai commencé avant le début du semestre, et qui est encore en cours [^1]:

| Nom du dépôt | URL                                                          |
| ------------ | ------------------------------------------------------------ |
| heig-bot     | [https://github.com/HEIG-TS/heig-bot](https://github.com/HEIG-TS/heig-bot) |

Je faisais de temps à autres des commits un peu trop gros ([`b00bd84`](https://github.com/HEIG-TS/heig-bot/commit/b00bd84efcb9c2d0a0ebe0533bfd9cd5af72cc37)), avec des messages pas clairs sur l'utilité du commit ([`9349bc1`](https://github.com/HEIG-TS/heig-bot/commit/9349bc1c5aca2fad590e1953ce9c276657764082)), voir même les deux à la fois ([`c966095`](https://github.com/HEIG-TS/heig-bot/commit/c966095fc83db95ac2132f2206e411e4d666cc8e))

J'ai donc mis un accent particulier à faire des commits plus petit et avec un message qui aide vraiment à la compréhension, comme vous pouvez le constater sur mes commit du [7 et 9 mars](https://github.com/HEIG-TS/heig-bot/commits/master).

[^1]: Ce projet est bien sûr en pause en ce moment au vu des restrictions actuelles sur GAPS.

### Utilisation en parallèle de *GEN*

#### Durant le cours de *PRO*

| Nom du dépôt                                 | URL                                                          |
| -------------------------------------------- | ------------------------------------------------------------ |
| Dépôt principale de notre projet de semestre | [https://github.com/HEIGVD-PRO-A-07/HEIGVD-PRO-A-07](https://github.com/HEIGVD-PRO-A-07/HEIGVD-PRO-A-07) |

Durant ce projet nous avons essayé de faire de commit de taille raisonnable et avec des commentaires pertinents. Malheureusement, au fur et à mesure de notre avancement, nous avons perdu notre rigueur et nous nous retrouvons avec un projet contenant quelques commits de médiocre qualité.

J'ai pu constater le malheur qu'est d'avoir de tel commit lors de la fin du projet. En effet, nous avons constaté qu'un bug avait été introduit, malgré le fait que nous testions presque chaque commit.[^2] J'ai donc utilisé l'excellente commande `git bisect` pour trouver le commit ayant le bug, après être tombé sur plusieurs commits qui ne compilait pas, j'ai identifié le commit intégrant le bug, ([`fce9e7a`](https://github.com/HEIGVD-PRO-A-07/HEIGVD-PRO-A-07/commit/fce9e7ab8a87afdac4432cd229a41d4401dbca09)) et constaté qu'avec plus de 250 lignes modifiées, cela ne permettait pas d'identifier rapidement la source du problème. J'ai donc appris l'utilité (voir la nécessité) d'avoir de petit commit qui ne modifie qu'une chose à la fois, ce que je n'hésiterais donc plus à imposer à mes partenaires de laboratoire.

En tant que chef de projet j'ai également du retrouvé qui avait inséré une ligne problématique dans le code source. Pour cela j'ai utilisé la commande `git blame` et le petit utilitaire [`tig`](https://jonas.github.io/tig/).

[^2]: Nous n'avons malheureusement pas pu mettre en place de test automatiser, ce qui nous aurait sûrement permis d'éviter ce bug.

#### Laboratoire

| Nom du dépôt | URL |
| --- | ---- |
| Dépôt upstream sur `gitlab`    |[https://gitlab.com/reds-public/pco20_student](https://gitlab.com/reds-public/pco20_student)      |
| Dépôt personnel sur `github`    | [https://github.com/g-roch/heig-pco-lab](https://github.com/g-roch/heig-pco-lab)     |

J'ai utilisé `git` pour l'ensemble de mes laboratoires ce semestre. J'ai obtenu une bonne expérience dans la gestion d'un dépôt au long cours avec des fusions régulières depuis un autre dépôt. En *PCO* par exemple, la donnée de nos laboratoires nous est fournie dans un dépôt `gitlab`, cependant j'ai choisi avec ma camarade, d'utilisé `github` pour ce laboratoire. J'avais donc quelques manipulations particulières pour récupérer la donnée sur `gitlab` puis de l'envoyer sur `github`, endroit où nous avions également nos solutions.

Les opérations que je faisais peuvent se résumer comme suit : 

- Effectuer un `fetch` sur le `remote` `gitlab` configurer pour suivre le dépôt du professeur.
- Effectuer un `pull` pour être évité d'avoir à faire plusieurs `merge` par la suite.
- Effectuer une fusion de la branche `gitlab/master` sur `master`.
  - Effectuer la fusion à la main si nécessaire.
- Faire un `push` sur `origin` (qui corresponds à mon dépôt privé)

J'ai au fil du semestre compris de mieux en mieux la notions de `remote`.

#### Portfolio de GEN

| Nom du dépôt | URL                                                          |
| ------------ | ------------------------------------------------------------ |
| Portfolio    | [https://github.com/g-roch/heig-gen-portfolio](https://github.com/g-roch/heig-gen-portfolio) |

J'ai également essayé de faire un effort sur les commits pour le portfolio.

## Diagrammes UML

### Durant le projet de semestre (*PRO*)

Dans le cours de *PRO* une des premières étapes est la modélisation du projet. Malheureusement cette étape est arrivée pour nous en même temps que la partie du cours de *GEN* sur les diagrammes UML, nous n'avons donc que très peu appliquer ce qui a été vu en *GEN*.

Après avoir vraiment vus en détails UML, je comprends vraiment l'utilité d'utilisé une nomenclature commune entre tous. Nous avons effectivement eu des difficultés à faire comprendre nos schémas à notre professeur (d'autant plus que cela s'est fait à distance)

Entre autres, à la place des schémas de la première page ([voir annexe 01](https://github.com/g-roch/heig-gen-portfolio/blob/master/Annexe-01-Modelisation-v1.0.pdf)), nous aurions pu faire deux schémas de cas d'utilisation avec comme acteur : les élèves, les enseignant, le serveur AD et l'autre partie de l'application. Cela aurait permis en plus d'expliqué plus facilement notre projet, d'être nettement plus au clair entre-nous sur nos objectifs et l’infrastructure à mettre en place.

J'ai également constaté que dans ces deux graphiques on a essayé de rassembler les technologies utilisés et l'infrastructure. Ces deux parties aurait gagné à être représentée chacun sur des schémas séparés.

## Test unitaire & TDD

| Nom du dépôt               | URL                                                          |
| -------------------------- | ------------------------------------------------------------ |
| Laboratoire *POO1* - échec | [https://github.com/g-roch/poo1-lab09](https://github.com/g-roch/poo1-lab09) |
| *GEN* - TDD                | [https://github.com/GEN-Labs-2020/GEN-L-02](https://github.com/GEN-Labs-2020/GEN-L-02) |
| *GEN* - Monopoly           | [https://github.com/GEN-Labs-2020/GEN-L-03](https://github.com/GEN-Labs-2020/GEN-L-03) |

Un test unitaire, c'est un petit bout de code facilement exécutable et qui vérifie le bon fonctionnement d'une fonctionnalité du projet. 

### *POO1* laboratoire sur le jeu d'échec

Le premier gros projet que nous avons fait à l'HEIG était le semestre passé en *POO1*, c'était un laboratoire ou nous devions mettre en place les règles du jeu d'échecs. Pour ce laboratoire, mettre en place des tests unitaires aurait été très performant. Nous avions une structure de base relativement rigide à respecter (notamment pour l’interaction avec l'interface graphique fourni), ce qui fait que nous aurions pu écrire les tests avant même de mettre en place nos structures de données.

### *GEN* laboratoire

Les laboratoire TDD et Monopoly sont les deux premiers laboratoires où nous avons mis en place des tests unitaires automatisé. Ce laboratoire nous a bien permis de voir le fonctionnement des tests unitaires en plus de montrer la manière dont on peut les utilisés lors de développement.

L'avantage du *TDD*, et que l'on n'a pas besoin de réfléchir lorsqu'on écrit le code, mais en amont sur ce que l'on veut que notre code fasse. Cela permet facilement de répartir le développement, car on a tous les mêmes objectifs (faire passer les tests)

Un autre très avantage d'avoir des tests unitaires dans un projet, c'est de vérifier que l'on n'a pas réintroduit un bug par erreur. On peut même automatiser cette tâche grâce à des outils comme [Jenkins](https://alternativeto.net/software/jenkins/about/) ou Travis que nous avons utilisé en *GEN* et *RES*.

## Conclusion

Le cours de GEN, est un cours qui nous apport énormément de méthodologie, chose que l'on peut facilement manquer en entrant à l'HEIG. Notamment dans la gestion de codes source dans `git`, la mise en place de tests unitaires et la réalisation de schéma utilisable et compréhensible par tous. Cependant, je trouve que certaine partie du cours serait bien mieux plus tôt dans notre formation. 

- L'apprentissage de `git` plus tôt dans la formation permettrais une bien meilleure collaboration entre étudiant durant les laboratoires, un positionnement de ce chapitre durant la première année me parais pertinent.
- La notion de diagramme UML de cas d'utilisation, d'activité, etc. ainsi que du cycle de vie d'un projet serais bien positionner avant PRO. (Peut-être décalé PRO vers un autre semestre moins chargé).

J'ai pu également constater que c'est le premier cours où on ne nous apprend pas des techniques informatiques en nous disant de nous débrouiller avec, mais un cours où on nous apprend à collaborer dans notre futur métier.

## Annexes

| Numéro | Nom                 | Nom du fichier                                               |
| ------ | ------------------- | ------------------------------------------------------------ |
| 01     | Modélisation de PRO | [`Annexe-01-Modelisation-v1.0.pdf`](https://github.com/g-roch/heig-gen-portfolio/blob/master/Annexe-01-Modelisation-v1.0.pdf) |


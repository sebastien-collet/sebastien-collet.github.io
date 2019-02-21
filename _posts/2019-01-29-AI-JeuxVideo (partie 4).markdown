---
layout: post
title:  "L'IA dans les jeux vidéo - Partie 4"
date:   2019-01-29
lang: fr
ref: jv4
categories: Vulgarisation
---


Récemment, beaucoup de médias ont abordé les thématiques d’IA et de jeux vidéo, en présentant des agents capable de rivaliser ou de battre des joueurs professionnels sur des jeux vidéo complexes notamment Dota 2 ou très récemment Starcraft 2 avec l’algorithme AlphaStar.

Jusqu’ici nous nous sommes surtout intéressés à ce que l’IA pouvait apporter au monde du jeu vidéo. Nous avons vu comment elle pouvait permettre de créer des mondes plus grands, plus vivants, plus cohérents etc.. Cependant la relation entre les deux domaines ne s'arrête pas là. Les jeux vidéo peuvent ainsi être un moyen d’améliorer et d'accélérer la recherche en IA. Dans cet article, nous allons donc nous intéresser au jeu vidéo en temps que médium de recherche en IA en présentant quelques réussites importantes du domaine.

<h2> L'intérêt des jeux vidéo</h2>
En quoi les jeux peuvent-ils aider à développer de meilleurs systèmes d’IA et pourquoi les chercheurs s'intéressent-ils tant aux jeux vidéo ? L’objectif de la recherche en IA est de produire des agents de plus en plus complexes capables de comprendre leur environnement, de raisonner et de prendre des décisions complexes. À terme l’idée est d’avoir des agents capables de prendre des décisions importantes (par exemple économiques, environnementales etc..) en prenant en considération plus de paramètres qu’il est possible pour un humain de le faire. 

La meilleure approche que nous ayons pour l’instant pour atteindre ces objectifs est de se baser sur un apprentissage. Ainsi, plutôt que de dire explicitement à l’agent comment il doit agir, on va essayer de lui faire apprendre de lui-même un comportement. On parle de  [Machine Learning](https://sebastien-collet.github.io/vulgarisation/2017/11/10/Machine-Learning-(en).html) et plus particulièrement d’apprentissage par renforcement. Il s'agit d’un framework d’apprentissage très ouvert qui permet d’obtenir de bons résultats sur des tâches variées. Cependant, pour mettre en place cet apprentissage, il faut des données. Beaucoup de données. Et il faut aussi souvent expliciter un objectif précis pour orienter l’apprentissage.

Les problématiques du monde réel sont en général assez difficiles à représenter dans ce framework puisqu’il n’y a souvent pas de grands volumes de données accessibles, ni d’objectifs bien définis.
Les jeux sont donc très propices à l’apprentissage d’IA puisqu’ils peuvent être assez analogues au monde réel tout en proposant des objectifs très clairs (par exemple battre le joueur en face, ou maximiser un score). Ainsi, le jeu Starcraft représente un environnement partiellement observable ou le joueur doit prendre des décisions stratégiques sans avoir accès à toutes les informations. Cet environnement peut-être rapproché en terme de complexité à des scénarios compétitifs du monde réel comme la logistique ou la gestion de chaîne d'approvisionnement par exemple.
De plus, les jeux peuvent être joués un très grand nombre de fois puisque ce sont des programmes, ce qui permet de générer énormément de données. On peut aussi accélérer le processus en parallélisant l’apprentissage sur des centaines ou des milliers d’instances du jeu en même temps.

Transférer directement un apprentissage effectué dans un jeu vidéo à une problématique du monde réel est quelque chose de difficile. Cependant, les méthodes inventées pour résoudre les problèmes dans les jeux s’avèrent souvent utiles aussi pour d’autres problématiques du monde réel.

Par exemple, la méthode Monte Carlo Tree Search (inventée pour le jeu de Go) dont nous avons parlé dans les articles précédents a déjà été appliquée à des problématiques du monde réel comme la planification de trajectoires interplanétaires de sondes spatiales. De même l’algorithme d’apprentissage par renforcement développé par OpenAI pour jouer à Dota2 a pu être utilisé quasiment directement pour apprendre dans une simulation à une main mécanique à contrôler et déplacer des objets.


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/simulated-camera-grid.png" title="hand" style="width:1000px;"/> 
 <figcaption> <br/> Environnement de simulation d'une main mécanique

 </figcaption>
</figure>
<br/>

Les développeurs d’OpenAI ont même réussi à transférer ce qui avait été appris dans cette simulation et à l’appliquer au monde réel.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/finger_traits_openai.gif" title="hand_real" style="width:800px;"/> 
 <figcaption> <br/> Vrai main mécanique
 </figcaption>
</figure>
<br/>

Ainsi, ils ont appris à une véritable main mécanique à contrôler des objets en faisant l’apprentissage dans une simulation grâce à ue algorithme développé pour un jeu vidéo.

<h3>L’évolution des médias</h3>

Les jeux (principalement les échecs) ont depuis longtemps été considérés comme “[la drosophile de L’IA](https://link.springer.com/chapter/10.1007/978-1-4613-9080-0_14)”. La drosophile ou “mouches des fruits” a été énormément utilisée dans les laboratoires pour effectuer de la recherche en génétique. Même si elle ne présente pas d'intérêt en soit, elle est très pratique pour la recherche puisqu'elle se reproduit très rapidement et elle est simple à nourrir et à conserver. Il est donc facile de tester et comparer rapidement différentes expérimentations. 
Les jeux de la même façon fournissent un environnement simple et stable pour mesurer les performances des différents algorithmes d’IA. Les jeux de dames puis les échecs ont donc longtemps servi de benchmark pour la recherche en IA. Cependant, la recherche évoluant, lorsqu’un jeu devient trop simple à résoudre avec les méthodes actuelles, on trouve un jeu plus difficile pour le benchmark. Ainsi le jeu de Go a remplacé les échecs et les jeux vidéo comme  Starcraft II ou Dota 2 remplacent le jeux de Go. L'intérêt de la recherche en IA pour les jeux vidéos reste ainsi relativement récent. La majorité des compétitions et des benchmarks d’IA effectués sur des jeux vidéos datent de dix dernières années.


<h3>L'intérêt du grand public </h3>

Les jeux sont de bon médiums puisqu’ils suscitent l'intérêt du public. Il suffit de voir l’engouement généré par les compétitions d’e-sport sur les plus grands jeux pour se rendre compte de l’importance du phénomène. De plus les oppositions entre IAs et humains ont toujours fasciné ou au moins intéressé la plupart d’entre nous.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/2018-08-23-image-7.jpg" title="hand_real" style="width:800px;"/> 
 <figcaption> <br/> Événement d'E-sport sur Dota 2
 </figcaption>
</figure>
<br/>

Ainsi, les jeux permettent de mesurer l’évolution des performances des algorithmes d’IA de manière accessible pour tout le monde. Savoir qu’un algorithme a battu le champion du monde aux échecs est probablement plus parlant que de savoir que l’état de l’art en classification d’image est de 2.25% en top-5 error sur ImageNet. 


Un autre point plus matérialiste est qu’en intéressant le grand public aux problématiques de l’IA, on diminue le risque de voir venir un nouvel [hiver de l’IA](https://en.wikipedia.org/wiki/AI_winter) (un gel des investissements dans l’IA).


<h1> La recherche en IA </h1>

<h2>Avant le Deep Learning</h2>


Le jeu Pac-Man a été assez important dans le développement de l'intérêt pour les jeux vidéo dans le milieu de la recherche en IA. Ainsi, Pac-Man a été considéré comme un problème intéressant pour l’IA dès le début des années 90, mais la recherche à réellement commencé dessus au début des années 2000. Les premières approches pour jouer aux jeux se basaient sur des algorithmes génétiques et des réseaux de neurones simples.  
Rapidement, la recherche est passée sur le jeu Ms. Pac-Man qui rajoutait un petit peu d’aléatoire dans le déplacement des fantômes, ce qui rend le problème plus difficile d’un point de vue algorithmique. L'intérêt croissant des chercheurs pour Ms. Pac-Man a ainsi permis la création de deux compétitions basées sur le jeu. La première, la “Ms. Pac-Man AI Competition” eut lieu de 2007 à 2011 et l’objectif était de développer un agent faisant le meilleur score possible dans le jeu. La deuxième compétition, “Pac-Man vs Ghosts competition”  eut lieu de 2011 à 2012 est permettait de développer des agents pour contrôler les fantômes. Les agents contrôlant Pac-man et ceux contrôlant les fantômes jouaient ainsi les uns contre les autres.  
Ces deux compétitions ont permis d’améliorer certains domaines, notamment les algorithmes génétiques, mais c’est surtout la méthode MCTS (encore elle) qui fut beaucoup développée grâce à ce jeu. Des approches à base d’apprentissage par renforcement furent testées mais sans grand succès par rapport aux autres approches.

L'intérêt pour la communauté scientifique sur ces compétitions, lança en quelque sorte le domaine et ainsi des compétitions sur d’autres jeux furent créés. Aujourd'hui l'intérêt en IA pour Ms. Pac-Man est retombé, mais le jeu fut important pour le domaine.

Un autre jeu important fut Super Mario Bros. avec “The Mario AI Competition” qui eu lieu de 2009 a 2012. La compétition fut d’abord orientée vers la création d’agents pouvant jouer au jeu comme pour celles sur Ms. Pac-Man. Le jeu étant très différent, cela présentait une alternative intéressante d’un point de vue de la recherche. De nombreuses solutions furent proposées, notamment des approches classiques à base d’apprentissages par renforcement, d’algorithmes génétiques et de réseaux de neurones, mais la première place fut remporté à la surprise générale par un agent implémentant un simple algorithme de recherche A\*. [Cette vidéo](https://www.youtube.com/watch?time_continue=1&v=DlkMs4ZHHr8) permet de voir l’agent en action. Cela mit en avant le fait qu’un algorithme très simple mais bien implémenté peut faire mieux que des solutions plus complexes. Les années suivantes, des niveaux plus labyrinthiques de Mario furent proposés et l’algorithme A\* montra rapidement ses limites.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/mario_A*.jpeg" title="hand_real" style="width:600px;"/> 
 <figcaption> <br/> En rouge, on peut voir les différentes trajectoires évaluées par l’algorithme de planification A*
 </figcaption>
</figure>
<br/>

En 2010, une tâche de génération procédurale sur le jeu fut proposée. Voir la [partie 3 de cette série]({{ site.baseurl }}/vulgarisation/2019/01/11/AI-JeuxVideo-(partie-3).html) et [cet article](https://aiandgames.com/the-mario-ai-competition/) pour avoir plus de détail sur les solutions proposées. Ainsi, l’IA dans les jeux vidéo ne se limitait plus simplement à faire des agents jouant bien aux jeux.

En 2012, une autre approche de recherche fut proposée : mettre en place des agents qui jouent exactement comme des humains. L’objectif est qu’une personne extérieure regardant la manière de jouer ne puisse pas déterminer si c’est un humain ou une IA qui joue. On parle donc de test de Turing pour un jeu puisque c’est une variante du [test de Turing](https://fr.wikipedia.org/wiki/Test_de_Turing) classique. 
Cette tache sur le jeu Mario n’eu lieu qu’une année et les agents ne furent pas capables de passer le test. 

Cependant, cette tâche fut aussi proposée sur d’autres jeux, notamment sur [Unreal Tournament 2004](https://fr.wikipedia.org/wiki/Unreal_Tournament_2004) entre 2008 et 2012. Sur ce jeu [deux agents](https://en.wikipedia.org/wiki/Computer_game_bot_Turing_Test) ont réussi à passer le test en 2012. Les deux agents apprenaient à imiter les comportements humains jusqu'à présenter un comportement quasiment indissociable.


<h2>Depuis le Deep Learning</h2>
L’arrivée du Deep Learning en 2012 a transformé nombre de domaines en IA comme la reconnaissance d’images ou l’analyse de langage. Le monde de l’IA sur les jeux vidéo a aussi été fortement impacté principalement à travers l’évolution de l’apprentissage par renforcement. 

En baisse de régime depuis le début des années 2000, l'intérêt pour le renforcement a été relancé par DeepMind en 2013 et leur solution appelée DQN (Deep Q-Network). Ils ont réussi à créer un système d’apprentissage par renforcement basé sur du Deep Learning capable de jouer à certains vieux jeux [Atari 2600](https://fr.wikipedia.org/wiki/Atari_2600) aussi bien que les humains en utilisant seulement les images du jeu (comme un humain jouerait). Ils ont ensuite amélioré leur [solution en 2015](https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf) (après un rachat par Google entre temps). Cette fois ci, l’algorithme joue mieux que des professionnels sur une trentaine de jeux et presque aussi bien sur une vingtaine d’autres. 

Là où leur solution est intéressante, c’est qu’ils ont utilisé la même architecture avec les mêmes paramètres pour tous les jeux. Un apprentissage du réseau pour chacun des jeux est bien effectué, mais il s’agit à chaque fois du même réseau initial, ce qui est une avancé importante en Machine Learning où il est souvent nécessaire de concevoir une architecture spécifique pour chaque problème. Avoir un seul algorithme capable de développer un large panel de compétences sur des tâches variées est un des objectifs de l’intelligence artificielle générale.

Avant de s'intéresser plus en détail à leur solution, faisons d'abord un petit point sur l’apprentissage par renforcement

<h3>Apprentissage par renforcement et Q-Learning</h3>

L’apprentissage par renforcement est la dernière approche principale du Machine Learning (avec l’apprentissage supervisé et l’apprentissage non supervisé). C’est la forme d’apprentissage la plus libre puisqu’elle ne nécessite pas de données en amont, celles-ci vont être en quelque sorte construites au cours de l’apprentissage. De nombreux cas d’usage peuvent donc être traités par l’apprentissage par renforcement. Cependant, en pratique c’est aussi l’approche la plus difficile à mettre en place et à faire fonctionner, justement parce que les données sont beaucoup plus brutes que pour les approches supervisées ou non supervisées.

L’approche reprend les notions d’agents, d’environnements, d’états et d’actions que nous avons vu dans le premier article de cette série avec les automates finis.
Pour rappel, dans un jeu vidéo, un état correspond à n’importe quelle situation qu’il est possible de rencontrer dans le jeu. En général, même les jeux simples présentent un très grand nombre d’états.
Une action correspond à une des possibilités qu’a un agent pour faire passer le jeu d’un état à un autre. Par exemple, les déplacements d’un agent sont des actions.

Ici, plutôt que de définir manuellement les actions que l’agent doit effectuer en fonction de l’état dans lequel il se trouve, on va laisser l’agent trouver lui-même les actions pertinentes à effectuer. Pour décider si une action est pertinente l’agent va se baser sur une notion appelée récompense. A chaque action effectuée, l’agent reçoit une récompense. Cette récompense va indiquer si l’état dans lequel se trouve l’agent est positif ou non. En général, on définit l’agent de façon à ce qu’il essaye de faire les actions qui sont censées maximiser ses récompenses dans le futur. Il essaie ainsi d’estimer la meilleure façon d’agir pour obtenir le plus de récompenses possible au global.


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/reinforcemenet_learning.png" title="hand_real" style="width:600px;"/> 
 <figcaption> <br/> Le processus itératif de l'apprentissage par renforcement
 </figcaption>
</figure>
<br/>

C’est le concepteur de l’algorithme qui doit définir comment les récompenses sont distribuées pour que l’apprentissage de l’agent puisse se faire. Si le système de récompenses a été bien défini, le fait de maximiser celles-ci revient à résoudre le problème d’apprentissage. Si elle a été mal défini, l’agent maximisera la récompense mais n’agira pas forcément comme prévu, c’est donc un des points cruciaux dans la réussite de l’apprentissage.

Avec l’apprentissage par renforcement, le jeu de données est construit de manière itérative en fonction des différentes actions effectuées par l’agent. Un échantillon de données correspond donc à une transition d’état, c’est-à-dire un état initial, l’action effectuée par l’agent, l’état après l’action et la récompense obtenue pour l’action. Avec beaucoup d’échantillons comme cela, il est possible pour un algorithme d’apprendre les meilleures actions à effectuer pour obtenir le plus de récompense. Dans la vrai vie, il est difficile de construire ces échantillons puisqu'il faut réellement effectuer des actions et observer les récompenses. Par contre, dans une simulation ou un jeu vidéo, cela ne pose en général pas de problèmes.

Voyons un exemple d’algorithme avec le Q-Learning. Le Q-learning est une approche qui se base sur une fonction particulière appelée la Q-value.
La fonction Q-value peut-être considérée comme un grand tableau de valeurs qui regroupe tous les états et toutes les actions possibles associées. Pour chaque état et action possibles, on a une valeur qui représente la récompense que l’on peut espérer obtenir si l’on effectue cette action alors qu’on était dans cet état. 
Ainsi, quel que soit l’état dans lequel on se trouve, il suffit de regarder les valeurs des différentes actions dans le tableau pour savoir comment se comporter. 

Pour construire le tableau de valeur de la Q-value, il faut donc jouer au jeu et tester toutes les actions dans tous les états possible et observer les récompenses obtenues. Si le jeu n’est pas déterministe, c’est-à-dire si certains événements sont aléatoires dans le jeu, il faut tester chaque action dans chaque état plusieurs fois. Il est assez clair que s’il l’on joue à un jeu avec beaucoup d’états et d’actions cela devient impossible. Donc, plutôt que de construire entièrement le tableau, on va essayer d’en faire une approximation. L’idée est d’être capable de construire une fonction qui donne la valeur de récompense estimée pour n’importe quelle paire d’état et d’action mais sans avoir besoin de tout calculer. 

Le meilleur outil d’approximation de fonction dont on dispose actuellement en IA, c’est le Deep Learning. L’idée du DQN (Deep Q Network) est donc de faire du Q-Learning en approximant le tableau de Q-value avec un réseau de neurones. 


<h4> DQN </h4>

Cette approximation du tableau avec du Deep Learning est possible parce qu’un réseau de neurones est capable de trouver les similitudes entre des états proches. Ainsi, il ne sera pas nécessaire de tester l’ensemble des cas possibles pour estimer la Q-value de façon pertinente.

Concrétisons cela en nous intéressant au problème Atari. Les différents jeux Atari 2600 tournent sur un émulateur ce qui permet de récupérer facilement les différentes images (on parle de frames) et de brancher un algorithme qui effectuera les actions à la place du joueur.
L’algorithme a accès aux mêmes informations qu’un joueur humain pour que la comparaison puisse être cohérente. Les états du jeu sont donc simplement les frames du jeu.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/breakout.png" title="hand_real" style="width:600px;"/> 
 <figcaption> <br/> Une frame du jeu breakout
 </figcaption>
</figure>
<br/>

Il y a quand même une petite subtilité, dans le cadre de l’apprentissage par renforcement, un état doit contenir l’ensemble des informations nécessaires à la compréhension d’une situation donnée pour pouvoir prédire la suite. On dit que le futur doit être indépendant du passé au vu du présent.

Prenons le jeu breakout comme exemple, si on défini un état comme étant une seule frame on a un problème : on ne sait pas dans quelle direction se déplace la balle. On ne peut donc clairement pas déterminer la suite du mouvement. Pour résoudre ce problème, il suffit de définir un état comme étant une succession de frames. Dans leur solution, DeepMind utilisent quatre frames pour définir un état.

Les actions possibles sont les différentes combinaisons de touches permises par les jeux. Au maximum, il y a dix-huit actions (dix,septs actions permises par le joystick de l'Atari 2600 de l’époque + l’action de ne rien faire), mais dans beaucoup de jeux le nombre d’actions est beaucoup plus restreint. Par exemple dans Pong il y a trois actions possible (haut, bas et ne rien faire)

Enfin, l’objectif à maximiser est le score du jeu. Celui-ci est visible en haut des frames donc il suffit de l’extraire pour savoir si les actions choisies ont eu des résultats positifs ou négatifs. L’objectif de l’algorithme est de prendre les décisions qui vont maximiser le score futur espéré.

Le tableau de Q-value est remplacé par un réseau de neurones qui prend en entrée un état du jeu (donc 4 frames). Le réseau va traiter ces frames et en sortie indiquer la récompense espérée pour chacune des différentes actions possibles. En prenant la meilleure action on maximise la récompense et donc le score sur le jeu.


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/dqn.png" title="hand_real" style="width:900px;"/> 
 <figcaption> <br/> Principe du DQN. En entrée on a 4 frames qui décrivent l’état du jeu et en sortie on a la récompense associée à chacune des actions.

 </figcaption>
</figure>
<br/>

Jusqu'ici on a décrit le fonctionnement du réseau de neurones, mais on n’a pas encore vu comment se passe l’apprentissage. En effet, au début le réseau n’a jamais joué au jeu, il n’a vu aucune frame et donc il ne sait pas estimer quelles actions sont pertinentes.

Un réseau de neurones classique (c’est-à-dire dans le cadre d’un apprentissage supervisé) s’apprend en comparant ses propres prédictions avec une vérité terrain (un label). Par exemple pour de la classification d’image, si un réseau prédit que l’image est un chien alors que c’est une image de chat, le réseau va avoir une grosse erreur de prédiction. Cette erreur va ensuite être utilisée pour mettre à jour les différents poids du réseau afin qu’il ne fasse plus une aussi grosse erreur si jamais il revoit cette image de chat dans le futur.
Lorsque l’on fait de l’apprentissage par renforcement, on n'a pas accès à une vérité terrain puisqu’on n'a pas de label. Il faut donc trouver une autre façon de calculer ses erreurs de prédictions.

Les seules informations dont on dispose lorsque l’on fait de l’apprentissage par renforcement sont la récompense associée à l’action que l’on vient de choisir et le nouvel état dans lequel on se trouve.
On peut donc comparer les récompenses futures que l’on estimait avant de faire l’action avec les récompenses futures que l’on estime dans le nouvel état une fois que l’action est faite. En comparant ces deux estimations de récompenses futures et en prenant en compte la vrai récompense que l’on a reçu pour l’action effectuée, on peut calculer une erreur de prédiction du réseau. Le réseau s’utilise donc lui-même pour mesurer ses performances et donc s’améliorer. Cette pratique d’utiliser le même réseau à l’état suivant pour s’auto-évaluer s’appelle le bootstrapping.

Il y a quand même un soucis avec le DQN. L’idée d’appliquer des réseaux de neurones au Q-Learning n’est pas nouvelle. En effet, cela avait déjà été appliqué quand l'appellation Deep Learning n’existait pas encore et cette idée ne marchait pas. Lorsque l’on fait du Q-Learning avec un réseau de neurones, l’apprentissage a tendance à diverger à cause de ce que l’on appelle la Deadly Triad. En pratique, ce qu’il se passe c’est qu’un réseau qui s’utilise lui-même pour s’évaluer et s’améliorer présente une forte tendance à apprendre n’importe quoi.

Pour lutter contre cela et permettre quand même l’apprentissage, DeepMind a proposé deux idées :
La première idée consiste à utiliser un deuxième réseau de neurones en parallèle du premier pour estimer les erreurs. Le deuxième réseau de neurones est mis à jour beaucoup moins régulièrement que le premier. Ainsi, on ne calcule pas l’erreur de prédiction en fonction d’une cible qui change tout le temps, mais plutôt en fonction d’une cible stable générée par un réseau qui est fixé la plupart du temps. Cela permet d’aider à stabiliser l’apprentissage.

La deuxième idée est d’utiliser ce qu’ils appellent un expérience replay. On peut voir cela comme une bibliothèque contenant un grand nombre d’états, d’actions et de récompenses passées (par exemple 50000). Au lieu de faire l’apprentissage du réseau de neurones en suivant le cours du jeu, on tire au hasard dans la bibliothèque des triplets état, actions, récompenses qui vont être utilisés pour mettre à jour le réseau. L’idée avec cette méthode est d'enlever la corrélation temporelle que l’on peut avoir quand on prend les actions de façon séquentielle, ce qui permet aussi de stabiliser l’apprentissage. 

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/dqn4.png" title="hand_real" style="width:800px;"/> 
</figure>
<br/>

Une fois le réseau appris, on peut afficher les Q-values pour différents états pour voir ce que l’agent a compris du jeu. L’agent contrôlé par l’algorithme est à droite en vert. Dans le jeu Pong il y a trois actions possibles : haut, bas et ne rien faire.
À l’état 1, la balle est encore loin donc l’algorithme estime que les trois actions se valent en terme de récompense.
À l’état 2, la balle se rapproche et la valeur de récompense estimée de l’action “haut” augmente alors que celle de “bas” et “ne rien faire” deviennent négatives. L’algorithme a compris que s’il ne va pas vers le haut à partir de maintenant le point sera perdu.
À l’état 3, l’agent continue de faire l’action “haut” et touche la balle
À l’état 4, la balle est partie de l’autre côté et le point va être gagné donc l’algorithme a compris que quelle que soit l’action effectuée le point sera gagné. C’est pourquoi les valeurs des trois actions sont à 1.

Pour chacun des jeux, l’apprentissage s’est fait sur 50 millions de frames, ce qui correspond à près de 38 jours de jeux au total. L’agent faisant son apprentissage sur un émulateur, toutes les parties ont en pratique été jouée en accélérée, l’apprentissage n’a donc pas vraiment pris 38 jours.
Le DQN n’est pas un algorithme efficace, il a besoin d'énormément de données pour obtenir un niveau satisfaisant. Ainsi, il lui faut 38 jours pour apprendre à jouer aux jeux alors qu’un humain aurait probablement besoin de 30 secondes pour comprendre leur fonctionnement. De nombreuses améliorations de l’algorithme ont été proposées par la suite afin d’améliorer cette efficacité et permettre donc l’apprentissage de tâches plus complexes.


<h3> Regain d'intérêt pour le renforcement </h3>


Le succès du DQN a vraiment relancé l'intérêt général pour l’apprentissage par renforcement. De nombreuses variantes et améliorations de l’algorithme ont donc rapidement été développées.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/rl_in_games.png" title="hand_real" style="width:800px;"/> 
 <figcaption> <br/> Les algorithmes principaux de renforcement dérivés du DQN et les différentes plateformes sur lesquelles ils ont été testés.
 </figcaption>
</figure>
<br/>


Le problème posé par l’environnement Atari étant en grande partie résolu, il fallait trouver de nouveaux sujets plus difficiles. Ainsi, de nombreuses plateformes de recherche sur des jeux vidéo ont été déployées dans le but de faciliter et d'accélérer la recherche. 

De bons environnements ou plateformes de recherche sont importants pour pouvoir développer et comparer des algorithmes de manière efficaces et sérieuse. La principale plateforme technique est probablement [OpenAI Gym](https://gym.openai.com/). Il s’agit d’une interface assez simple en Python qui facilite la comparaison d’algorithmes de renforcement. La plupart des plateformes de recherches qui existent sont basées sur Gym. Il n’est pas possible d’aborder toutes les plateformes, nous allons donc en présenter quelques-unes qui semblent importantes.

<h4>Les environnements d’OpenAI</h4>

On peut citer tout d’abord [Universe](https://github.com/openai/universe) développé par OpenAI en 2016. Universe élargissait les possibilités offertes par l’environnement Atari en proposant de travailler sur des jeux flash ou même des jeux comme GTA V. L’objectif d’Universe était de pouvoir généraliser un apprentissage fait sur un jeu à d’autres jeux ou d’autres environnement. Universe était probablement trop ambitieux et les résultats ne furent pas concluants. Le principal problème était que pour pouvoir lancer des types de jeux aussi variés, l’environnement lançait un navigateur chrome dans un docker. Du fait de ce choix d'implémentation, le système n’était pas stable et les algorithmes devaient forcément interagir avec les jeux en temps réel ce qui est gênant pour faire de très gros apprentissages.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/retro-contest.gif" title="hand_real" style="width:800px;"/> 
 <figcaption> <br/> Environnements de jeux de Retro
 </figcaption>
</figure>
<br/>


C’est pourquoi OpenAI a développé [Retro](https://blog.openai.com/gym-retro/) pour remplacer Universe. L’objectif de Retro était de revenir à un système plus fiable tout en proposant des environnements qui restent challengeant pour les algorithmes. Avec Retro il est donc seulement possible d’apprendre des modèles sur des jeux de Mega Drive (console de SEGA). Les jeux de la Mega Drive sont plus poussés que ceux de l’Atari, ils proposent donc un challenge plus grand. De plus l’objectif de l’environnement est encore une fois d’essayer d’apprendre des comportements qui peuvent être généralisés sur plusieurs jeux différents.  
Un [concours](https://blog.openai.com/retro-contest/) sur Retro à été mis en place à la sortie de l’environnement. Les différentes équipes participantes doivent apprendre un agent sur certains niveaux du jeu Sonic et ensuite leur agent est testé sur d’autres niveaux inédits. L’agent qui va le plus loin dans le niveau remporte la compétition.

Les [résultats](https://blog.openai.com/first-retro-contest-retrospective/) ont montrés que les solutions les plus performantes étaient des approches assez classiques d’apprentissage par renforcement (notamment la 2ème place qui utilise une variante améliorée du DQN) ce qui est assez encourageant car ce ne sont pas des solutions très manuelles et spécifiques au problème qui ont gagné. Par contre les résultats obtenus sont assez loin du score maximal théorique ce qui montre que le problème est encore loin d’être résolu.

Les résultats du concours ont montré que les agents sont performants sur les niveaux utilisés pour faire l’apprentissage mais assez mauvais sur de nouveaux niveaux présentant des situations inédites. Les algorithmes d’apprentissage par renforcement présentent donc des problèmes de généralisation. Les niveaux de Sonic étant assez complexes et labyrinthiques, la tâche proposée par le concours Retro est vraiment difficile. C’est pourquoi OpenAI a décidé de développer un environnement appelé [CoinRun](https://blog.openai.com/quantifying-generalization-in-reinforcement-learning) spécifiquement dédié à la généralisation. CoinRun présente un environnement de jeu de plateforme ou un personnage doit atteindre une pièce à l’autre extrémité d’un niveau.


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/coinrun-plus-difficulty.jpg" title="hand_real" style="width:1000px;"/> 
 <figcaption> <br/> Deux niveaux de CoinRun. Un niveau facile à gauche et un plus difficile à droite
 </figcaption>
</figure>
<br/>

Les niveaux de CoinRun sont en général beaucoup plus simples que ceux de Sonic mais les agents sont toujours testés sur des niveaux qu’ils n’ont pas vu durant leur apprentissage. L’objectif de cet environnement est donc d’être un bon compromis entre challenge d’un point de vue recherche et difficulté de la tâche.

<h4> VizDoom</h4>

[VizDoom](http://vizdoom.cs.put.edu.pl/) comme son nom l’indique est une plateforme qui permet de faire l’apprentissage par renforcement dans le jeu [Doom](https://fr.wikipedia.org/wiki/Doom). La plateforme permet d’obtenir plusieurs types d’informations sur le jeu, comme l’image affichée, la position et le type des différentes éléments, des informations de profondeurs ou encore des informations sur le niveau vu d’en haut. Elle permet aussi bien sur de faire tourner le jeu très rapidement pour accélérer les apprentissages.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/vizdoom.gif" title="hand_real" style="width:1000px;"/> 
 <figcaption> <br/> Les différents types d’informations accessibles à travers Vizdoom.
 </figcaption>
</figure>
<br/>

Depuis trois ans, une compétition a lieu sur la plateforme. Il s’agit de la [Visual Doom AI Competition](http://vizdoom.cs.put.edu.pl/competitions/vdaic-2018-cig/results) (VDAIC). Dans cette compétition, des agents qui n’ont accès qu'aux images du jeu doivent s’affronter dans des matchs à mort. Jusqu’ici, les agents de cette compétition n’ont pas encore atteint le niveau des humains

D’autre approches assez innovantes ont été développées sur VizDoom notamment celle des [World Models](https://worldmodels.github.io/). Il s’agit d’une approche d’apprentissage par renforcement où un agent se construit un modèle du monde (comme une sorte de rêve) et apprend à agir dans ce modèle du monde rêvé. 

En tout, la plateforme VizDoom a permis la publication de plus de 150 articles de recherche.

<h4> TORCS </h4>

[TORCS](http://torcs.sourceforge.net/) (The Open Racing Car Simulator) est un jeu de simulation de course automobile. Il est utilisé en temps que jeu et en temps que plateforme de recherche. Il s’agit d’une simulation donc les agents qui jouent doivent prendre en compte de nombreux paramètres comme les arrêts au stand ou l’usure et la température des pneus par exemples. Le jeu a servi de base pour de nombreuses compétitions en IA, que ce soit la création d’agents conduisant les voitures ou d’agents construisant automatiquement de nouveaux circuits. Il y a même tous les ans un [championnat du monde](http://www.berniw.org/trb/events/event_view.php?vieweventid=24) sur le jeu qui est organisé. Il s’agit d’un championnat entre agents ou chaque équipe propose en amont une IA qui doit concourir durant différentes courses.


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/1.jpeg" title="hand_real" style="width:800px;"/> 
 <figcaption> <br/> Le jeu TORCS
 </figcaption>
</figure>
<br/>

Les environnements de course automobile très proches de la réalité sont intéressants puisqu’ils peuvent servir de base pour la conception d’algorithmes destinés aux voitures autonomes. Le fait que le jeu soit libre de droit est important. En effet, plusieurs projets de recherche de simulation de voiture autonome basés sur le jeu GTA V (dont un dans l’environnement Universe de OpenAI) ont dû être [complètement arrêtés](https://www.forbes.com/sites/aarontilley/2017/10/04/grand-theft-auto-v-the-rise-and-fall-of-the-diy-self-driving-car-lab/#66de62127d7a) pour des questions de droits liés à l’éditeur du jeu Take-Two Interactive. L’environnement TORCS est moins photo-réaliste que GTA V, mais il n’y a pas de risque que les projets de recherches basés dessus soient stoppés pour des raisons similaires.


<h4> Le projet Malmo </h4>

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/Project_Malmo_1920x577.jpg" title="hand_real" style="width:1500px;"/> 
</figure>
<br/>

Un autre projet de plateforme notable est le projet Malmo. L’objectif ici est de développer des algorithmes d’IA capable de comprendre un environnement complexe, d'interagir avec le monde, d’apprendre des compétences et de les appliquer sur de nouveaux problèmes difficiles. L’environnement choisi pour développer des solutions à ces problématiques est le jeu Minecraft. Minecraft est un jeu bac à sable dans lequel le joueur est beaucoup plus libre que dans la plupart des autres jeux. Les possibilités d’action sont très vastes, allant de tâches très simples comme se promener pour chercher du minerais à des tâches très complexes comme la construction de superstructures. Cette liberté fait donc de Minecraft un bon bac à sable pour les algorithmes mais il est assez probable que le projet Malmo permette des avancées en IA à plus long terme que les autres environnements.


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/minas-tirith-minecraft.jpg" title="hand_real" style="width:800px;"/> 
 <figcaption> <br/> Une construction dans Minecraft
 </figcaption>
</figure>
<br/>

Pour finir, tout récemment Unity a mis à disposition un environnement appelé [The Obstacle Tower](https://storage.googleapis.com/obstacle-tower-build/Obstacle_Tower_Paper_Final.pdf?elqTrackId=7bf0fd56f0214c49a65313d157c09583&elqaid=2003&elqat=2) en proposant en parallèle un [concours](https://create.unity3d.com/obstacletower) (qui commencera le 11 février prochain) sur cet environnement. 


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/image1-1.png" title="hand_real" style="width:800px;"/> 
 <figcaption> <br/> The Obstacle Tower
 </figcaption>
</figure>
<br/>

Il s’agit d’un jeu en 3 dimensions dans lequel l’agent doit monter dans un tour de 100 étages. Chaque étage correspond à un niveau et la difficulté est croissante. Le jeu peut être joué par des humains, mais il est destiné à la recherche. Avec quelques minutes d'entraînement, les humains qui ont testé le jeu arrivent en général à atteindre le 20ème niveau. L’environnement est donc difficile, et même pour un humain atteindre le haut de la tour semble être un challenge.
Unity propose cet environnement dans l’objectif d’être un benchmark sur une tâche difficile pour remplacer un précédent environnement difficile : le jeu Atari 2600 [Montezuma’s Revenge](https://en.wikipedia.org/wiki/Montezuma%27s_Revenge_(video_game)).

<h4>Montezuma’s Revenge </h4>

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/montezuma2.jpg" title="hand_real" style="width:800px;"/> 
 <figcaption> <br/> Les jeux avec les scores les plus bas de l’algorithme DQN

 </figcaption>
</figure>
<br/>

Si l’on regarde les scores de l’algorithme DQN sur les différents jeux Atari 2600 et que l’on s'attarde sur le fond du classement, on remarque un jeu avec un score de 0% (ce qui correspond au score obtenu en jouant aléatoirement). Cela signifie que l’agent DQN qui est capable de jouer mieux que des joueurs professionnels sur une trentaine de jeux n’est pas capable de faire mieux que l’aléatoire sur ce jeu en particulier : Montezuma’s Revenge. Pourquoi donc ? Qu’est-ce qui rend ce jeu si différent des autres ? Intéressons-nous un petit peu à ce jeu.


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/monte.png" title="hand_real" style="width:700px;"/> 
</figure>
<br/>

Voici le premier niveau de Montezuma’s Revenge. C’est un jeu labyrinthique où le joueur doit avancer en trouvant des clés pour ouvrir des portes, tout en combattant des ennemis. Pour gagner des points dans ce jeu, il faut soit trouver une clé, soit ouvrir une porte (ce qui nécessite une clé). L’image présentée ici est la toute première salle du jeu.

Afin de pouvoir obtenir des points dans cette salle, le joueur doit donc descendre de l'échelle, aller vers la droite (le sol est un tapis roulant qui va à gauche et qui projette dans le vide), sauter sur la corde, sauter sur la plateforme de droite, descendre l'échelle, aller à gauche, sauter par-dessus la tête de mort qui bouge, monter l'échelle et enfin sauter sur la clé.


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/montezuma.png" title="hand_real" style="width:700px;"/> 
 <figcaption> <br/> Voici les étapes à faire pour obtenir les premiers points. Il est possible de tester le jeu dans un navigateur <a href="https://www.retrogames.cz/play_124-Atari2600.php">ici</a>. Il vous faudra probablement plusieurs essais avant d’arriver à atteindre la clé. </figcaption>
</figure>
<br/>

L’apprentissage par renforcement se base sur les récompenses obtenues pour estimer si les actions faites sont pertinentes ou non. Si on ne reçoit aucune récompenses, il n’y a pas de moyen de s’améliorer. Les algorithmes de renforcement commencent donc en général par jouer de façon aléatoire au début afin de voir quelles actions donnent des récompenses et lesquelles n’en donnent pas. Le problème de Montezuma’s Revenge est qu’en jouant aléatoirement, il est quasiment impossible d’obtenir la première clé et donc impossible d’obtenir de récompense. L’algorithme DQN se casse donc les dents sur ce jeu puisque l’apprentissage ne peut même pas démarrer. Les nombreuses variantes et améliorations du DQN ont permis d’améliorer quelque peu les résultats, mais aucune ne donnent des résultats vraiment satisfaisants. Aucune n’arrive à finir le premier niveau. Pour donner un ordre d’idées, il y a 23 autres salles de ce genre à compléter pour finir le premier niveau du jeu.

Récemment, DeepMind et OpenAI ont proposé des méthodes pour jouer à Montezuma’s Revenge. Leurs méthodes ont réussi à terminer le premier niveau du jeu, ce qui est un résultat bien supérieur à ce qui était possible jusque-là. Cependant on ne peut pas vraiment considérer que leurs approches ont résolu le jeu par de l’apprentissage par renforcement pur. En effet, leurs méthodes sont basées sur des démonstrations humaines pour aider l’apprentissage.

La première méthode de DeepMind se base sur des vidéos Youtube de joueurs humains complétant le niveau. À partir de ces vidéos, ils construisent une récompense qui correspond au fait d’atteindre des zones visités par les joueurs. L’algorithme obtient donc des récompenses bien plus fréquemment ce qui permet l’apprentissage.

L’approche d’OpenAI utilise les trajectoires d’un joueur humain pour initialiser l’agent différemment. En effet, si on initialise l’agent juste devant la clé, un algorithme classique trouvera sans problème qu’il faut sauter dessus pour obtenir des points. Une fois que cette phase est apprise, on peut initialiser l’agent en bas de l'échelle sous la clé. Encore une fois depuis cette initialisation, un agent va forcément monter en haut de l’échelle. Une fois en haut, il se trouve dans une situation qu’il connaît puisqu’il l’a appris juste avant, il va donc sauter pour récupérer la clé.


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/monteopenai.png" title="hand_real" style="width:700px;"/> 
 <figcaption> <br/> Initialisations de l’agent de plus en plus loin de la clé au fur et à mesure de l’apprentissage.
 </figcaption>
</figure>
<br/>

En continuant ainsi l’apprentissage en éloignant de plus en plus le point de démarrage, on peut réussir à apprendre un agent capable de résoudre le premier niveau. Cependant, cela demande du travail spécifique puisqu’il faut définir plusieurs points d’initialisation qui suivent la trajectoire d’un joueur humain mais en sens inverse.

Ces deux approches sont intéressantes mais elles présentent un problème.
Utiliser des démonstrations humaines pour apprendre une tâche n’est pas un problème en soit (c’est en général comme cela que les humains apprennent de nouvelles compétences d'ailleurs) mais ça l’est dans le cadre de Montezuma’s Revenge. En effet, le jeu est déterministe, c’est-à-dire qu'à chaque fois qu’on y joue, il y aura les mêmes salles, les mêmes ennemis et rien ne sera laissé au hasard.

En utilisant une démonstration humaine sur le jeu, on ne permet pas à l’agent de comprendre la démonstration et de la généraliser à de nouvelles situations, on lui permet juste d’apprendre par cœur les trajectoires qu’il doit prendre pour résoudre le jeu. Ce qui est appris au final n’est pas comment jouer à Montezuma’s Revenge, mais plutôt comment exécuter une séquence d’actions spécifique pour finir le jeu. Ceci n’était clairement pas l’objectif initial puisque l’on cherche plutôt à créer des méthodes d’apprentissage par renforcement les plus générales possibles.

<b> L'approche RND </b>   
Très récemment (fin octobre 2018), OpenAI a proposé un algorithme capable de parfois terminer le premier niveau sans se baser sur une démonstration humaine. Leur approche, appelée [RND](https://blog.openai.com/reinforcement-learning-with-prediction-based-rewards/) (Random Network Distillation) encourage l’agent à explorer son environnement en attisant en quelque sorte sa curiosité. Ainsi, ils proposent un système de récompense supplémentaire qui va encourager l’agent à visiter les zones qu’il n’a pas encore vu. En explorant ainsi de façon plus méthodique les différentes zones du jeu, il va tomber sur les éléments qui donnent les vraies récompenses, comme les clés ou les portes et ainsi l’apprentissage sera facilité.

Pour trouver les zones non visitées, l’agent se base sur ses propres prédictions de l’état futur. En effet, si l’agent est capable de prédire ce qu’il va se passer après une action, c’est qu’il est dans une zone connue. Au contraire, s’il ne peut pas prédire ce qu’il va se passer, c’est qu’il n’a jamais dû parcourir la zone. En donnant une récompense à l’agent quand il n’arrive pas à prédire le futur, on le pousse à toujours aller dans de nouvelles zones. En combinant cette approche favorisant l’exploration avec un algorithme classique d’apprentissage par renforcement, le jeu à pu être résolu.

Montezuma’s Revenge a longtemps montré les limites de nos algorithmes d’apprentissage. On a longtemps cru que pour bien résoudre le jeu, les agents devraient avoir une meilleure compréhension des différents concepts du jeu, comme ce qu’est une clé, ce qu’est une porte, le fait qu’une clé ouvre une porte, etc.
Au final, en trouvant un moyen astucieux pour explorer le niveau et avec un apprentissage suffisamment long, le jeu a pu être résolu. Il semble donc que les différents problèmes difficiles qui paraissent nécessiter des capacités humaines (comme la compréhension de concepts, le raisonnement, etc.) pour être résolu, peuvent souvent au final être résolu de manière complètement différente par les algorithmes. 

L’environnement d’Unity, The Obstacle Tower est pensé pour être une sorte de successeur à Montezuma’s Revenge. Le futur nous dira si l’environnement se montre vraiment intéressant en terme de recherche en IA.


<h2> Les approches principales de DeepMind et OpenAI</h2>

Nous allons maintenant nous intéresser particulièrement à trois approches présentant des résultats vraiment impressionnants. Ces méthodes sont très récentes, elles ont été développées en 2018 et 2019 et ont fait beaucoup parler d’elles dans les médias. Elles sont développées par DeepMind et OpenAI qui ont des moyens en terme de puissance de calcul bien supérieur aux laboratoires de recherches académiques. Cela permet à ces équipes de s'intéresser à des sujets à la fois en temps que problèmes de recherche, mais aussi comme des problèmes d’ingénierie. Les laboratoires académiques s'intéressent en général à des problèmes plus restreints et/ou fondamentaux principalement par manque de moyens.
Les jeux concernés par ces approches sont Quake III, Dota 2 et Starcraft 2.

<h3> Quake III </h3>

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/linstant-retro-gaming-de-mysticktchii-quake-iii-arena-31363.jpg" title="hand_real" style="width:800px;"/> 
 <figcaption> <br/> </figcaption>
</figure>
<br/>


La première approche est le travail de DeepMind sur le jeu [Quake III](https://fr.wikipedia.org/wiki/Quake_III_Arena). En pratique, il s'agit d'un clone maison de Quake III qui s'appelle [DeepMind Lab](https://github.com/deepmind/lab)). Le mode de jeu sur lequel ils ont travaillé s’appelle Capture The Flag (CTF ou [Capture du drapeau](https://fr.wikipedia.org/wiki/Capture_du_drapeau) en français). Il s’agit d’un mode ou deux équipes s’affrontent pour essayer de voler le drapeau du camp adverse et le ramener à son propre drapeau. L’équipe qui a réussi à ramener le drapeau adverse le plus de fois dans son propre camp en 5 minutes l’emporte. Cette [courte vidéo](https://www.youtube.com/watch?v=-5KQw7PiVFI) de Deepmind explique le principe. Les règles sont simples, mais les dynamiques de ce mode de jeu sont complexes. Pour être performant, il est nécessaire de mettre en place des stratégies, des tactiques et surtout de jouer en équipe.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/ctf.png" title="hand_real" style="width:600px;"/> 
 <figcaption> <br/> Interface du jeu utilisée pour jouer à Capture The Flag
 </figcaption>
</figure>
<br/>

Deepmind a réussi à développer des agents capables de jouer aussi bien voir mieux que des humains à ce mode de jeu. De façon intéressante, leurs agents arrivent à travailler en équipe avec d’autres agents, mais aussi avec des humains.

Le problème posé par ce jeu s’appelle le multi-agent learning. En effet, plusieurs agents doivent apprendre à agir indépendamment tout en apprenant à interagir et coopérer avec d’autres agents. C’est une tâche difficile puisque comme les agents évoluent durant leur apprentissage, l’environnement auquel ils sont confrontés change continuellement. De plus pour que les agents apprennent réellement à jouer au mode CTF plutôt que de retenir par cœur la disposition de l’environnement, ils jouent dans des environnements générés procéduralement (et oui la génération procédurale peut aussi servir à créer un meilleur cadre d’apprentissage !).


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/quake_maps.jpg" title="hand_real" style="width:700px;"/> 
 <figcaption> <br/> Exemple de 36 environnements de jeu générés procéduralement, vus d’en haut.

 </figcaption>
</figure>
<br/>

Comme pour beaucoup d’autres approches présentées dans ce poste, les agents ont accès aux mêmes informations que les joueurs humains, c’est-à-dire simplement les informations qui s’affichent à l’écran. Les règles du CTF ne sont jamais explicitées, les agents doivent les comprendre d’eux-mêmes. De plus, les différents agents n’ont pas de moyen pour communiquer entre eux, ils doivent donc agir et apprendre indépendamment.


<b>L’architecture des agents</b>   
Comme pour l’algorithme DQN, le cœur de l’agent va être un réseau de neurones. Ici tout est juste un peu plus complexe. Les agents doivent être capables d’être performants à plusieurs échelles de temps : ils doivent pouvoir réagir vite quand un ennemi apparaît ou que le drapeau est volé par exemple et ils doivent aussi pouvoir agir sur le plus long terme pour mettre en place une stratégie. En général, quand on a ce genre de problématiques, on s'intéresse à ce que l’on appelle l’apprentissage par renforcement hiérarchique. Ainsi, pour pouvoir proposer un tel comportement les agents sont donc basés sur un réseau récurrent hiérarchique à deux niveaux de temporalité. Les réseaux récurrents sont les réseaux que l’on utilise classiquement pour traiter des données séquentielles (comme le texte). Les plus connus sont les [LSTMs](https://www.bioinf.jku.at/publications/older/2604.pdf). Les agents sont donc pourvus d’une hiérarchie de deux LSTMs (en pratique les réseaux utilisés sont un peu plus complexes que des LSTMs mais l’idée reste la même). Le premier voit tous les états et agit à toutes les étapes tandis que le deuxième ne voit qu’un état de temps en temps. Les deux niveaux peuvent donc traiter l’information de façons différentes. De plus, les agents sont équipés d’un système de [mémoire](https://deepmind.com/blog/differentiable-neural-computers/) qui leur permet de stocker les informations qu’ils jugent importantes afin de pouvoir les réutiliser au moment opportun.


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/archi_quakeIII.png" title="hand_real" style="width:800px;"/> 
 <figcaption> <br/> L’architecture des réseaux de neurones des agents</figcaption>
</figure>
<br/>

En amont de ce système se trouve un réseau convolutionnel classique qui est simplement là pour comprendre les images et extraire les informations importantes (n’oublions pas que les agents jouent avec comme seule information les images à l’écran). Comme pour le DQN, un état est une succession de 4 images. Le jeu tourne à 60 images par seconde, cela fait donc 15 étapes d’apprentissage par seconde.

<b>Les différentes actions</b>   
En sortie de la hiérarchie de LSTMs, une action pour l’agent est choisie. Dans l’environnement Atari, il y avait 17 actions possibles. Ici le jeu est beaucoup plus compliqué, les actions possibles sont continues plutôt que discrètes (on peut déplacer le viseur n’importe où sur l’écran) et elles sont combinables (on peut par exemple avancer, sauter, déplacer le viseur et tirer en même temps). Pour simplifier grandement cela, les actions ont été limitées principalement au niveau du viseur. Ainsi, il devient seulement possible pour l’agent de déplacer le viseur d’une certaine valeur verticale et/ou horizontale par rapport à la position à l’étape d’avant (Ainsi par exemple seuls les déplacements horizontaux du viseur avec un angle de 10 degrés ou de 60 degrés sont autorisés). Grâce à cette simplification, le nombre d’actions possible à chaque étape est de 540.
La hiérarchie de LSTMs choisit donc une de ces actions en fonction des images qu’elle reçoit et des informations du passé.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/quake3.png" title="hand_real" style="width:600px;"/> 
 <figcaption> <br/> Comparaison des interactions possibles avec le jeu entre humains et agents</figcaption>
</figure>
<br/>


<b>La récompense</b>   
Les agents ont donc un moyen de choisir des actions en fonction des états. 
Comme dans tout algorithme d’apprentissage par renforcement pour apprendre comment choisir ces actions de façon pertinente on utilise la récompense. Comme le but est d’apprendre aux agents à gagner au CTF, la récompense est positive si l’équipe de l’agent gagne la partie, négative si elle perd et nulle s'il y a match nul. Le problème est que cette récompense est très rare, en effet des milliers d’actions peuvent être faites avant la fin d’une partie. On tombe donc dans le même type de problème qu’avec le jeu Montezuma’s Revenge ou l’apprentissage n’est pas possible puisque l’agent n’arrive pas à faire le lien entre actions et récompenses. Il faut donc trouver un moyen de fournir aux agents des récompenses plus fréquemment. Quake III contient un système de points pour chaque joueur qui est indépendant du score de l’équipe (qui est lui basé seulement sur les captures de drapeaux). Les joueurs gagnent des points en touchant des joueurs ennemis, en capturant un drapeau, en ramenant son propre drapeau dans sa base etc..
Deepmind propose un système où l’agent se crée son propre système de récompense interne basé sur le système de points de Quake III. Avec ce système, les récompenses deviennent beaucoup plus fréquentes et l’apprentissage devient possible.


<b>L’algorithme d’apprentissage</b>   
L’algorithme de renforcement utilisé pour l’apprentissage est l’algorithme UNREAL (aussi développé par DeepMind) qui est une amélioration de l’algorithme [A3C](https://arxiv.org/pdf/1602.01783v2.pdf) (Asynchronous Advantage Actor-Critic) avec des tâches non supervisées pour accélérer l’apprentissage. [Cet article](https://deepmind.com/blog/reinforcement-learning-unsupervised-auxiliary-tasks/) du blog de DeepMind donne plus de détails sur cette méthode. L’algorithme A3C est lui-même une amélioration de l’algorithme DQN. Ces algorithmes sont visibles sur la figure présentant les algorithmes principaux de renforcement dérivés du DQN présentée précédemment.


<b>L’apprentissage</b>   
On a vu comment était représenté un agent, son système de récompense et l’algorithme de renforcement utilisé. Désormais, il faut des données pour faire l’apprentissage. Une solution possible pour apprendre ce type d’agent est de le faire jouer contre lui-même. Cependant, cette approche peut être assez instable et n’apporte pas beaucoup de variété. En effet l’agent va jouer continuellement contre une version de lui-même qui sera de plus en plus forte au cours du temps, mais qui aura probablement un comportement global assez similaire sur le long terme. Afin d’amener de la diversité dans les tactiques et les stratégies de jeux, ce n’est pas un agent mais une population entière d’agents différents qui est entraînée en parallèle. Les différents agents jouent les uns contre les autres ce qui permet de stabiliser l’apprentissage. Cette population d’agent évolue dans le temps grâce à un algorithme génétique appelé [PBT](https://arxiv.org/pdf/1711.09846v2.pdf). Cet algorithme remplace les agents les moins performants par des versions mutées des agents les plus performants. Ainsi, l’ensemble de la population s’améliore au cours du temps. C’est aussi cet algorithme qui adapte le système de récompense interne de chaque agent. Ainsi, les objectifs les plus pertinents pour un agent ne seront peut-être pas les mêmes pour un autre agent.

L’apprentissage des agents a nécessité 450 000 parties. À la fin de cette phase ils sont bien meilleurs que les humains. Après un peu plus de 100 000 parties la population d’agents jouait au niveau d’un humain moyen.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/CTF-Fig-Tagging-180703-r01.width-1500.png" title="hand_real" style="width:800px;"/> 
 <figcaption> <br/> Évolution du niveau de la population d’agents au cours de l’apprentissage. Le niveau des agents est calculé avec un <a href="https://fr.wikipedia.org/wiki/Classement_Elo">système Elo</a> comme aux échecs par exemple
</figcaption>
</figure>
<br/>

Le système proposé par DeepMind pour jouer au Capture The Flag est donc une approche complexe à deux niveaux d’apprentissage mélangeant algorithme génétique et apprentissage par renforcement. Grâce à ce système, les agents découvrent comment équilibrer leurs objectifs individuels (leur système de récompense interne) avec l’objectif de l’équipe (la récompense finale, c’est-à-dire gagner ou perdre la partie).


Il est intéressant de noter que différents comportements stratégiques et de travail d’équipe comme ceux-ci dessus ont été découverts et compris durant l’apprentissage. Les agents une fois entraînés ont tendance à mieux coopérer avec leurs équipiers que les joueurs humains.


<h3> Dota 2</h3>

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/dota-card-2.jpg" title="hand_real" style="width:900px;"/> 
</figure>
<br/>

Plus ou moins en même temps que la solution proposée par DeepMind pour jouer à Quake III CTF, OpenAI à fini de mettre au point son approche pour jouer à Dota 2 en 5v5. Durant le printemps et l’été 2018, ils ont continuellement amélioré et complété leur approche, proposant des agents de plus en plus performants jusqu’au point culminant fin août : deux matchs contre des équipes de joueurs professionnels à The International 2018, la plus grosse compétition du monde sur Dota 2.

[Dota 2](https://en.wikipedia.org/wiki/Dota_2) est un jeu de type Moba (Multiplayer online battle arena). C’est un type de jeu où deux équipes d’en général 5 joueurs chacune s'affrontent dans le but de détruire la base de l’équipe adverse. Chaque joueur contrôle un seul personnage, un héros qui présente des capacités et des pouvoirs particuliers. Au cours de la partie, les héros évoluent, devenant de plus en plus performants et débloquant de nouveaux pouvoirs. De très nombreux héros existent et chaque joueur commence par choisir le sien parmi les différentes possibilités, l’aspect stratégique commencent donc avant même le début de la partie. En effet, certains héros permettent de contrer d’autres héros et ainsi de suite. Le jeu se déroulant en 5 joueurs contre 5 joueurs, les possibilités sont énormes.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/25heur4.png" title="hand_real" style="width:800px;"/> 
 <figcaption> <br/> Choix des héros en début de partie
</figcaption>
</figure>
<br/>

<b>La complexité du jeu</b>   
Si l’on compare Dota2 avec le mode CTF de Quake III, la complexité est bien plus importante. En effet, là où le nombre d’actions possible à chaque instant avait été réduit à 540 sur Quake III, ici le nombre d’actions possible est de 170000 (même si en pratique à chaque instant, toutes les actions ne sont pas exécutable, l’ordre de grandeur est donc plutôt du millier d’actions).
Comme pour Quake III, il s’agit d’un jeu ou l'information est imparfaite (contrairement au Go) puisque seules les zones proches de l'équipe sont visibles. On ne sait donc pas à chaque instant ce que fait l’adversaire. De plus, le déroulement du jeu se fait en temps réel et une partie dure en moyenne 45 minutes (contre 5 minutes pour Quake III). Et le dernier point, Dota 2 est un jeu hautement stratégique, pour gagner il faut être capable d’être coordonné entre les différents membres de l’équipe et de prévoir ses actions sur le long terme.

L’ensemble de ces facteurs fait de Dota 2 un jeu très complexe pour une IA, c’est donc un bon challenge pour améliorer la recherche dans le domaine.

<b>L’approche itérative D’openAI</b>   
Devant la complexité de la tâche, OpenAI a pris la décision de partir sur une approche itérative, en proposant un agent pour une version très simplifiée et restreinte du jeu, puis en enlevant au fur et à mesure les restrictions pour arriver au final jusqu’au jeu complet.

Ainsi, ils ont commencé par proposer un agent pour le mode de jeu 1v1. Il s’agit d’un mode où chaque équipe n’est composée que d’un seul joueur, ce qui réduit grandement les possibilités du jeu. Il s’agit d’un mode de jeu moins populaire que le 5v5 mais il existe quand même des compétitions en 1v1, le mode est donc joué par des humains.

À la compétition The International 2017, leur agent a battu un joueur professionnel en 1v1 sur scène, devant de nombreux spectateurs. Les jours précédents leur agent avait aussi battu d’autres joueurs professionnels dont les meilleurs du monde. Ceux-ci décrivant l’agent comme imbattable.

À cette époque, OpenAI n’avait pas encore détaillé son approche (voulant dévoiler les informations seulement une fois l’agent prêt pour le jeu en 5v5). La seule information disponible étant que l’agent est appris entièrement en jouant contre lui-même. L’approche semble donc similaire à celle pour Quake III.

Au final, il s’avéra que l’agent n’était pas imbattable. Tous les joueurs professionnels ont évidemment voulu se mesurer à l’IA et des failles furent trouvées. En effet, l’agent était extrêmement fort face à un adversaire jouant de manière conventionnelle, mais il se retrouvait rapidement confus si celui-ci jouait de façon complètement anormale. Ainsi, avec les bonnes stratégie (non conventionnelles) tous les joueurs professionnels furent capables de battre cette version de l’agent.

OpenAI pouvant corriger ces problèmes rapidement en considérant ces stratégies durant la phase d’apprentissage de l’agent contre lui-même décidèrent d’en rester là pour l’agent en 1v1 et de commencer à travailler sur la version 5v5. La raison principale est qu’en 5v5, le nombre de stratégies imprévues comme celle trouvée par les joueurs est forcément bien plus important. Apprendre ces stratégies en les implémentant une à une durant la phase d’apprentissage n’est donc pas une solution viable. Il faut un agent capable d’apprendre à réagir de lui-même face à ces situations non conventionnelles.


<h4>OpenAI Five</h4>   
OpenAI a donc continué son approche itérative de développement de son IA en enlevant des restrictions de jeu au fur et à mesure de leur succès. Chaque restriction enlevée augmente la complexité du jeu et se rapproche des règles officielles des grands tournois. L’ascension de leur agent en 5v5 - nommé OpenAI Five - est assez impressionnante. En effet, c’est seulement fin avril 2018 qu’ils ont réussi à battre une équipe de bots dont les règles sont manuelles. Ce genre de bot est très loin du niveau des bons joueurs humains. Ils étaient donc encore assez loin de l’objectif à ce moment là. Et pourtant, en juin 2018, leur agent a battu une équipe de joueurs semi-professionnels. Et finalement en août ont eu lieu les matchs contre deux équipes de joueurs professionnels. OpenAI Five a perdu les deux fois, mais les matchs étaient très serrés. Leurs agents sont donc très proches du niveau des meilleures équipes professionnelles. Les matchs en août étaient aussi les premiers avec les règles officielles. En effet, ceux de juin étaient encore joués sur une version du jeu avec des règles restreintes. 

Voyons donc comment ils ont réussi cette impressionnante progression. OpenAI n’a pas encore fourni tous les détails de son implémentation mais plusieurs [articles](https://blog.openai.com/openai-five/) sur leur [blog](https://blog.openai.com) décrivent quand même assez précisément l’approche utilisée.

<b>Les données</b>   
OpenAI Five utilise l’[API](https://developer.valvesoftware.com/wiki/Dota_Bot_Scripting) fournie par Valve le développeur de Dota2. Ainsi, à chaque instant, toutes les informations visibles à l’écran pour un joueur humain sont accessibles pour les agents. C’est une grosse différence avec la solution pour Quake III qui elle regardait et analysait les images à l’écran. Ici, il n’y a pas cette étape de reconnaissance d’image pour obtenir les informations. Les agents ont ainsi accès à toutes les informations d’un coup (en pratique cela représente 20 000 valeurs à chaque état), contrairement aux humains qui ne peuvent pas tout regarder en même temps. Il peut y avoir débat ici sur le fait que cela soit équitable ou non par rapport aux humains, mais l’apprentissage avec les images du jeu à analyser aurait nécessité des milliers de GPUs supplémentaires.

Comme l’agent Quake III, OpenAI Five observe le jeu toutes les 4 images (parce qu’un état est une séquence de 4 images). Dota 2 tourne à 30 images par seconde donc au maximum l’agent pourrait effectuer 7.5 actions par seconde ou 450 actions par minute. En pratique, un agent effectue en moyenne entre 150 et 170 actions par minute ce qui est dans les cordes d’un joueur humain. Cependant, le temps de réaction moyen d’un agent est de 80 ms ce qui est plus rapide que le temps de réaction d’un humain.


<b>L’architecture des agents</b>   
Chacun des cinq héros de l’équipe d’OpenAI Five est contrôlé par un agent indépendant, comme pour une équipe d’humains. Ce n’est donc pas un super agent qui contrôle tous les héros en même temps. Ainsi, chaque agent contient un modèle qui est initialement le même pour tous, mais qui peut apprendre différemment des autres en fonction des expériences encourues durant l'entraînement. Les modèles des agents sont des réseaux de neurones. Ceux-ci reçoivent à chaque étape les données fournies par l’API.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/dota22.png" title="hand_real" style="width:1000px;"/> 
 <figcaption> <br/> Les différentes couches de neurones traitent les informations récupérées depuis l’API.

</figcaption>
</figure>
<br/>

Les réseaux sont constitués tout d’abord de couches de neurones classiques dont l’objectif est de représenter les informations de façon pertinente pour que le cœur des agents puissent prendre des décisions. Les 20000 valeurs fournies par l’API sont donc agrégés et transformés par ces couches afin de ne garder que ce qui est pertinent pour l’agent.

Les cœurs des agents qui reçoivent ces données transformées sont de simples réseaux récurrents de type LSTM. Le LSTM analyse la séquence de données et contextualise ainsi le présent grâce aux évènements du passé. Grâce aux données contextualisées par le LSTM différentes “têtes” de classification estiment les actions à accomplir. Ainsi, on peut voir qu’une tête a pour objectif de choisir l’action la plus pertinente, une autre doit estimer les coordonnées en X de l'exécution de l'action, une autre les coordonnées en Y et ainsi de suite.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/dota23.png" title="hand_real" style="width:1000px;"/> 
</figure>


Le LTSM contextualise la séquence de données et les 8 têtes de classification prennent la décision de quoi faire. Le diagramme complet et non retouché se trouve [ici](https://d4mucfpksywv.cloudfront.net/research-covers/openai-five/network-architecture.pdf). Dans [cet article](https://blog.openai.com/openai-five/), une interface dynamique permet de faire le lien entre ce qui est affiché à l’écran et les différentes têtes.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/dota5.png" title="hand_real" style="width:800px;"/> 
 <figcaption> <br/> Interface interactive sur le blog OpenAI qui permet de visualiser les différentes actions </figcaption>
</figure>
<br/>

Certains choix dans la modélisation (notamment au niveau des têtes d’actions) ont été faits en analysant les comportements des agents durant des parties. Si un certain comportement ne correspondait pas à ce qui était attendu, l’architecture du réseau était modifiée pour faciliter l’apprentissage de ce comportement.
Un point intéressant, si l’on compare cette solution avec celle pour Quake III, on constate qu’il n’y a pas de hiérarchie de LSTM à différentes temporalités pour gérer les actions à court et long terme. Il semble qu’avec un seul LSTM les agents d’OpenAI Five arrivent à gérer de la planification sur le long terme. Les chercheurs d’OpenAI eux-mêmes expliquent qu’ils pensaient cela impossible avec les approches classiques. L’apprentissage par renforcement hiérarchique (décrit pour la première fois [ici](http://www.cs.toronto.edu/~fritz/absps/dh93.pdf)) et utilisé pour Quake III leur semblait par exemple être une nécessité. Mais ce n’était visiblement pas le cas.


<b> L’algorithme d’apprentissage </b>   
L’algorithme d’apprentissage par renforcement utilisé s’appelle Proximal Policy Optimisation (PPO). Il ne s’agit pas d’une variante du DQN comme tous les autres algorithme que nous avons vu jusqu'ici. La différence est qu’ici ce n’est pas la Q-Value qui est optimisée mais directement la politique de choix des actions. L’algorithme PPO a été [proposé par OpenAI](https://blog.openai.com/openai-baselines-ppo/) en 2017 et a depuis démontré de bonnes performances, notamment durant le concours Retro sur le jeu Sonic ou sur Montezuma’s Revenge.

Pour tout algorithme de renforcement, l’objectif est de maximiser les récompenses futures. En générale, on essaie de maximiser la somme des récompenses futures pondérées par des valeurs décroissantes. L’idée est de dire que l’ensemble des récompenses du futur sont importantes, mais que celles dans un futur proche le sont plus que celles dans un futur lointain car celui-ci est trop incertain. 

En général, on prend souvent des valeurs qui décroissent exponentiellement sur 100 valeurs, ainsi à chaque instant on considère les récompenses des 100 prochaines étapes. Suivant la durée entre les étapes cela peut être une durée plus ou moins longue, mais en général cela n'excède pas quelques secondes. 
Au début de l’apprentissage d'OpenAI Five, le nombre de récompenses futures considérées par l’agent est assez restreint mais au fur et à mesure le nombre augmente jusqu'à prendre en considération l’ensemble des récompenses.
Ainsi, une fois appris Dota Five essaie à chaque instant d’optimiser les récompenses qu’il estime obtenir jusqu'à la fin de la partie, ce qui permet de mettre en place des stratégies à l'échelle d'une partie entière. C’est probablement la première fois qu’un apprentissage par renforcement sur si long terme fonctionne.


<b>L’apprentissage</b>   
Comment cela peut-il donc fonctionner si l’approche utilisée est un algorithme classique et connu de tous ? OpenAI discute de deux raisons de ce succès : l’apprentissage à très grande échelle et la présence de bons moyens d’exploration.

L’infrastructure pour faire l’apprentissage est impressionnante : 256 GPU par agent et 128 000 CPU. Avec cela, il est possible pour les agents de jouer à Dota chaque jour l’équivalent de 180 années pour un humain.

Les agents apprennent à jouer intégralement en faisant des matchs contre eux-mêmes. Durant les premières parties, les héros font un peu n’importe quoi, errant sans but dans la carte. Puis, au fur et à mesure, ils commencent à présenter des comportements plus proches de ceux des humains. Pour éviter ce qu’ils nomment “l’effondrement de stratégies”, les agents jouent 80% des parties contre eux-mêmes et 20% contre des versions d’eux même du passé. Il s’agit d’un problème similaire à la deadly triad du DQN. Ainsi en prenant des version du passé, on diminue le risque d’avoir des données d’apprentissage trop corrélées.

Avec cette approche d’apprentissage, OpenAI Five a pu devenir assez bon pour battre un bot avec des règles manuelles (en mars 2017) mais il devenait confus face à des humains. Ceux-ci jouaient de façons trop variées, présentant toujours de nouvelles situations non vues pendant l’apprentissage. On l’avait vu avec Quake III, le fait de jouer contre soi-même n’apporte pas assez de variété dans les situations, même en jouant contre des versions du passé.

Pour mieux explorer durant l’apprentissage, c’est-à-dire tester de nouvelles configurations de jeu pour voir les résultats des différentes actions, OpenAI a décidé d’ajouter de l’aléatoire dans les parties. Ainsi, dans certaines parties, les propriétés des différentes unités comme la vie, la vitesse ou encore le niveau de départ ont été modifiés aléatoirement. Ainsi, les agents se sont retrouvés dans des situations bien plus variées qu’en faisant simplement des parties normales.

Cet aléatoire forcé permit aux agents d’atteindre pour la première fois le niveau des humains. En apprenant plus longtemps et avec encore plus d’aléatoire, le niveau de Dota Five n’a fait qu'augmenter.


<b> La récompense </b>   
Comme pour Quake III, utiliser une seule récompense en fin de partie n’est pas suffisant pour entraîner correctement les agents. Une récompense plus fréquente a donc été construite manuellement par OpenAI. Elle comprend les différents indicateurs que les humains considèrent pour connaître l’état d’une partie, c’est-à-dire le nombre de héros tués, le nombre de morts, le nombre de PNJs tués etc.. Cette récompense est interne à chaque agent mais il y a aussi une récompense globale liée à l’équipe qui correspond en gros au fait de gagner ou perdre la partie.

Les agents n’ont pas de moyen explicite pour communiquer entre eux. Pour gérer le travail d’équipe durant l’apprentissage, un paramètre permet de définir l’importance des récompenses propres à l’agent par rapport aux récompenses liées à l’équipe. Au début de l’apprentissage, les agents s'intéressent seulement à leurs propres récompenses. Cela permet aux agents d’apprendre les règles et les principes importants du jeu. Puis au fur et à mesure de plus en plus d’importance est mise sur les récompenses d’équipe pour que les agents développent des stratégie tous ensembles. Ce système est très performant puisque le travail d’équipe des différents agents est ce qui a le plus impressionné les experts observant Dota Five jouer.

<b> Les derniers composants manuels </b>   
Les choix stratégiques en terme de combinaisons d’objets et de compétences des héros (ce qu’on appelle les builds des héros) sont pour l’instant définis manuellement. Ils ont été codés en amont et à chaque partie ils sont choisis aléatoirement. Il est probable qu’OpenAI essaie d’enlever dans le futur ces dernières étapes manuelles pour apprendre automatiquement les builds les plus adaptés à chaque situation. Il reste encore dans leur approche quelques autres fonctionnalités qui sont définies en dur. Peut-être qu'à l’été prochain à The International 2019, Dota Five sera un agent complètement automatique dont tous les paramètres seront appris automatiquement. Dans tous les cas, si OpenAI a continué à travailler sur cet agent et qu’ils organisent un match contre une équipe professionnel durant cet évènement, tout porte à croire que l’agent remportera cette fois-ci la victoire face aux humains.


<br/>
<h3> Starcraft II</h3>

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/StarCraft-II-intelligence-artificielle-DeepMind.jpg" title="hand_real" style="width:800px;"/> 
</figure>
<br/>

Starcraft II  un jeu de stratégie en temps réel (RTS) dans lequel deux joueurs s’affrontent en développant une base afin d’obtenir des ressources qui leur permettent de construire différents types d’unités pour attaquer l’adversaire. Starcraft II est depuis longtemps considéré comme un grand challenge pour la recherche en IA voir le challenge ultime dans le cadre des jeux vidéo. Les joueurs de Dota diront probablement le contraire, mais quoi qu’il en soit les deux jeux sont très complexes et présentent probablement un challenge assez similaire pour une IA.

En effet, Starcraft 2 est aussi un jeu où l’information est imparfaite puisque seules les zones proches des unités du joueur sont visibles. Le déroulement du jeu se fait en temps réel et le nombre d’actions possibles à chaque instant est énorme. Il n’y a pas de stratégies toujours gagnantes dans Starcraft II. Un peu comme au jeu pierre-papier-ciseau, il y aura toujours une approche pour en contrer une autre.

De plus, pour bien jouer il faut pouvoir faire preuve de stratégie à deux niveaux de hiérarchie :

* La micro-gestion c’est-à-dire gérer de façon intelligente, rapide et précise les différentes unités que l’on a à disposition lors des combats.
* La macro-gestion c’est-à-dire gérer la stratégie globale de la partie en construisant les bonnes unités, en décidant quand attaquer, comment gérer ses ressources etc..

Pour bien jouer à Starcraft II, il faut donc être capable de prévoir à long terme puisque les décisions prises à un instant donné peuvent avoir des répercussions bien plus tard dans la partie, mais aussi de prendre des décisions très rapidement et d’agir précisément. Voir les joueurs professionnels jouer est assez [impressionnant](https://www.youtube.com/watch?v=MVEvwNbeK6I).


<b>La recherche sur Starcraft </b>   
Bien qu’il y ait eu de nombreux succès en IA dans les jeux vidéo comme on a pu le voir (Atari, Quake III, Dota2,..), jusqu’ici les différents algorithmes n’arrivaient pas à gérer la complexité de Starcraft. Aucun agent basé sur une IA ne pouvait rivaliser avec des joueurs professionnels. Ce n’est pas pour autant qu’il n’y avait pas de recherche sur le jeu. Plusieurs compétitions ont eu lieu, parfois en restreignant le tâche à une sous-partie du jeu complet.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/DxshcieX0AAhdKO.jpg" title="hand_real" style="width:800px;"/> 
<figcaption> <br/> Historique de la recherche sur Starcraft présenté par DeepMind </figcaption>
</figure>
<br/>


En 2018 à la [AIIDE Starcraft AI competition](https://www.cs.mun.ca/~dchurchill/starcraftaicomp/index.shtml) c’est un agent avec des règles manuelles qui a [remporté la compétition](https://www.cs.mun.ca/~dchurchill/starcraftaicomp/2018/) (devant un agent de Facebook appris par renforcement).

En 2016 et 2017 Blizzard et DeepMind ont travaillé ensemble pour fournir un environnement appelé [PySc2](https://github.com/deepmind/pysc2) avec différents outils pour simplifier la recherche et l’apprentissage d’algorithmes sur Starcraft II.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/sc2-1.png" title="hand_real" style="width:800px;"/> 
<figcaption> <br/> L’environnement PySc2 </figcaption>
</figure>
<br/>

Grâce à cet environnement, quelques approches récentes (comme [celle-ci](https://arxiv.org/pdf/1809.07193.pdf) ou [celle-ci](https://arxiv.org/pdf/1809.09095.pdf)) commencent à proposer des agents avec apprentissage capables de battre les meilleurs bots de Starcraft II (qui trichent en ayant plus de ressources ou en voyant tout le jeu par exemple) mais pas encore du niveau des humains. 


<h4>AlphaStar</h4>
Toujours grâce à PySc2, DeepMind a pu mettre au point AlphaStar, une IA capable de battre des joueurs professionnels sur le jeu complet (avec quand même quelques restriction : le jeu est pour l’instant limité à une seule race et une seule carte).

AlphaStar à joué jusqu'ici contre deux joueurs professionnels est à pour l’instant (en janvier 2019) engrangé dix victoires pour une défaite. Les résultats sont donc bien supérieurs aux approches antérieures.

<b>L’approche utilisée</b>   
Tous les détails d’AlphaStar ne sont pas pour l’instant accessibles puisque DeepMind n’a pas encore fourni le papier de recherche décrivant en détail la solution. Un [article de blog](https://deepmind.com/blog/alphastar-mastering-real-time-strategy-game-starcraft-ii/) nous donne cependant les informations principales sur le fonctionnement de l’agent. 

La méthode semble être une amélioration de celle utilisée pour jouer au mode CTF sur quake III. En effet, on retrouve l’idée d’un apprentissage à deux niveaux : une population d’agent au sein de laquelle chaque agent fait lui-même son apprentissage par renforcement mais qui au niveau global est gérée par un algorithme génétique qui ne garde que les meilleurs agents pour améliorer au fur et à mesure le niveau de la population entière.

<b>Les différentes phases de l’apprentissage</b>   
Une différence importante est que Starcraft II est bien plus complexe que le mode CTF, il semble donc quasiment impossible d’apprendre le fonctionnement basique du jeux seulement par renforcement. En effet, au début si les agents ne savent pas du tout jouer, ils auront beau faire des matchs les uns contre les autres, ils n’apprendront rien. C’est pourquoi l’apprentissage initial des agents est fait de façon supervisé grâce à ce que l’on appelle l’Imitation Learning. De façon assez similaire aux approches discutées pour Montezuma’s Revenge, les agents ont accès à de très nombreuses parties de joueurs humains et ils apprennent les bases du jeu à partir de ces parties. C’est seulement après cette phase que les agents commencent à jouer les uns contre les autres dans ce que DeepMind a nommé l’AlphaStar League. Dans cette league, la population d’agent fait un très grand nombre de matchs les uns contre les autres pour s’améliorer. 

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/SCII-BlogPost-Fig03.width-1500.png" title="hand_real" style="width:1000px;"/> 
<figcaption> <br/> Principe général de l’apprentissage des agents d’AlphaStar
 </figcaption>
</figure>
<br/>

Pour les matches en cinq manches contre les joueurs professionnels, les cinq meilleurs agents de la League ont été sélectionnés. L’algorithme génétique qui gère la population force une certaine variété entre les agents, ce qui fait que les cinq agents choisis par DeepMind jouaient de façons différentes, ce qui a étonné et perturbé les joueurs professionnels.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/SCII-BlogPost-Fig04.width-1500.png" title="hand_real" style="width:1000px;"/> 
</figure>
<br/>

On peut voir ici l’évolution du niveau estimé des agents au cours de l'entraînement dans la league. Les points TLO et MaNa correspondent au niveau des deux joueurs professionnels rencontrés. Le point Supervised Learning correspond au niveau atteint par les agents après la phase initiale d’apprentissage en imitant la manière de jouer des humains sur un grand nombre de parties.

<b>Détails techniques de l’apprentissage</b>   
Pour le premier match contre un joueur professionnel, les agents se sont entraînés durant 7 jours complets. L’environnement PySc2 permet d'accélérer le jeu et de lancer de nombreuses instances en parallèle. Les 7 jours correspondent donc au final à 200 ans de jeu pour les agents. Pour le deuxième match, les agents ont eu 7 jours d’entraînement de plus. Pour chaque agent, 16 [TPUs](https://cloud.google.com/tpu/) ont été utilisés durant l’apprentissage ce qui représente une puissance de calcul assez énorme. Cependant, une fois l’agent entraîné, le faire jouer ne nécessite qu’une machine classique dotée d’un GPU.


<b>L’algorithme d’apprentissage</b>   
L’algorithme de renforcement utilisé est [IMPALA](https://arxiv.org/abs/1802.01561) (à ne pas confondre avec [Apache Impala](https://impala.apache.org/) le moteur de requête SQL sur Hadoop présent dans [Saagie](https://www.saagie.com/product/technologies/).
Il s’agit d’une amélioration de A3C optimisée pour la parallélisation massive. De plus de nombreuses astuces d’apprentissage sont utilisées comme par exemple le [self-imitation learning](http://proceedings.mlr.press/v80/oh18b/oh18b.pdf) qui incite l’agent à répéter plus souvent les bonnes actions qu’il a pu faire dans le passé.

<b>L’architecture des agents</b>   
Pour le mode CTF de Quake III, le cœur des agents étaient une architecture avec deux niveau de réseaux LSTMs. Ici, l’agent est basé sur un Transformer combiné avec un LSTM (avec en plus d’autres approches récentes comme les [pointer networks](https://papers.nips.cc/paper/5866-pointer-networks.pdf)).

Le [Transformer](https://arxiv.org/abs/1706.03762) est un modèle de réseau de neurones qui a fait beaucoup parler de lui dans le monde du traitement du langage (NLP). Il s’agit d’ailleurs de l’architecture sur laquelle beaucoup de solutions de l’état de l’art en NLP sont basées (comme la traduction automatique par exemple). Cette architecture est pensée pour gérer les données sous formes séquentielles. En général, on l’utilise sur des phrases mais ici les actions à effectuer dans le jeu sont aussi des données séquentielles. C’est un choix assez intéressant parce que le Transformer est connu pour avoir des difficultés à gérer les séquences très longues. Or, les séquences d’actions à effectuer dans un jeu comme Starcraft II sont bien plus longues que n’importe quelle séquence de mots dans une phrase. DeepMind a probablement trouvé une approche pour contrer ce phénomène, peut-être créer une hiérarchie de séquences ou limiter les séquences temporellement par exemple. On aura probablement les détails une fois l’article de recherche paru.

Les pointer networks sont une variante des architectures de type seq2seq (l’état de l’art en traduction avant l’arrivée du Transformer) dont l’objectif est de trier d’une certaine façon une séquence en entrée. Par exemple, ces réseaux peuvent servir à résoudre [le problème du voyageur de commerce](https://fr.wikipedia.org/wiki/Probl%C3%A8me_du_voyageur_de_commerce) en indiquant dans quel ordre se déplacer. DeepMind ne détaille pas encore dans quel cadre ces réseaux sont utilisés, mais cela pourrait servir à gérer l’ordre dans lequel les actions doivent être exécutés. Par exemple dans une bataille, choisir quelles unités attaquer en priorité, lesquelles il faut protéger, etc..


<b>Les prédictions de l’agent</b>
L’architecture de l’agent prédit à chaque instant du jeu la séquence d’actions attendue jusqu'à la fin du jeu. Évidemment, cette séquence d’action est continuellement mise à jour et modifiée en fonction de ce que fait réellement l’adversaire dans la partie.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/sc2-agent.gif" title="hand_real" style="width:900px;"/> 
</figure>
<br/>

DeepMind propose ici une interface qui montre comment se comporte l’agent durant une phase de jeu. Dans cette version, l’agent avait accès à l’ensemble des informations de la carte à chaque instant. 

Le Transformer est ce que l’on appelle un modèle à attention, c’est-à-dire qu’il peut en quelque sorte se focaliser sur seulement certaines parties de l’information qu’il considère importantes. On peut voir sur la minicarte à droite que l’agent à chaque instant se focalise sur une seule zone et qu’en une minute, il change sa zone d’attention une trentaine de fois (ce qui est similaire au comportement des joueurs professionnels humains).

Dans l’interface proposée par Deepmind, on voit qu'à chaque instant, le modèle considère s’il doit construire de nouveaux bâtiments ou de nouvelles unités et surtout, il estime s’il est en train de gagner ou de perdre la partie. Cet indicateur de son état dans la partie lui permet d’agir en fonction. Par exemple, s’il sent qu’il est en train de perdre, il va peut-être se replier pour essayer de mieux se défendre dans sa base.

Un des points importants durant les parties contre les joueurs professionnels est que l’agent semblait toujours capable d’estimer quand il pouvait attaquer ou quand, au contraire il fallait plutôt ne pas prendre de risque. Le modèle semble donc capable de prédire à chaque instant s’il est en train de gagner la partie, mais à plus petite échelle, il semble aussi capable de prédire s’il peut remporter une escarmouche ou non.


<b>Pertinence de l’architecture</b>   
DeepMind pense que leur architecture pourra aussi servir dans d’autres tâches où il est important de modéliser des séquences sur le long terme (comme la traduction automatique par exemple).

Une des avancées majeures à propos de AlphaStar (et de OpenAI Five) et qu’il semble que ces modèles continuent d’apprendre et de s’améliorer plus on ajoute de puissance de calcul. Ce n’était clairement pas le cas avec du Machine Learning classique où on atteignait souvent un palier de performance difficile à dépasser même en ajoutant plus de données. Cela signifie donc que les architectures choisies sont pertinentes et permettent de bien encoder les différentes problématiques de ces jeux.

<b>Remarques sur les restrictions</b>   
À propos des restrictions du jeu, le fait de pouvoir jouer avec les trois races augmente encore beaucoup la complexité du jeu. Cependant, l’architecture proposée semble capable d’apprendre cela avec un temps et une puissance de calcul suffisant surtout en commençant l’apprentissage en imitant des parties humaines. L’autre grande restriction est liée aux cartes de jeu. Actuellement, AlphaStar est appris sur seulement une carte alors que le jeu en propose bien plus et renouvelle régulièrement son panel. Il existe certaines stratégies très agressives viable sur seulement une carte par exemple, l’agent devra donc être capable de s’adapter à ces stratégies spécifiques et généraliser un comportement. Encore une fois, vu les résultats déjà accomplis, cela semble possible avec l’architecture actuelle.

<b>La dextérité de l’agent</b>   
Un point important à considérer lorsque l’on parle d’IA qui joue a Starcraft II est en quelque sorte la “dextérité” de l’agent. En effet, Starcraft étant un jeu où il faut contrôler beaucoup d’unités en même temps, un humain ne pourra jamais rivaliser avec un agent pouvant effectuer plusieurs milliers d’actions par seconde. DeepMind a donc volontairement ralenti ses agents pour que cela soit plus juste vis-à-vis des joueurs humains et donc que ce soit les stratégies proposées par l’agent qui fassent la différence et non son exécution parfaite.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/SCII-BlogPost-Fig09.width-1500.png" title="hand_real" style="width:900px;"/> 
</figure>
<br/>

On peut voir ci-dessus le nombre moyen d’actions par minute (APM) de l’agent et des joueurs professionnels. L’agent semble effectuer moins d’actions en moyenne. Il faut aussi prendre en considération le temps de réaction. En effet, un agent qui réagit instantanément aux différentes situations aura aussi un avantage considérable sur un humain même s’il ne fait pas beaucoup d’actions. On peut voir à droite le temps de réaction de l’agent qui a été réduit à celui du niveau d’un humain. 

Ce graphique présente la théorie. En pratique, il y a quand mêmes beaucoup de [questionnements](https://medium.com/@aleksipietikinen/an-analysis-on-how-deepminds-starcraft-2-ai-s-superhuman-speed-could-be-a-band-aid-fix-for-the-1702fb8344d6) au niveau de la dextérité réelle d’AlphaStar. Il est clair que l’IA a montré par moment une dextérité non-humaine durant les parties. 

En effet, l’agent était initialement limité en terme d’APM. Avec cette limitation, l’agent n’arrivait visiblement pas à apprendre à micro-gérer ses unités pendant les affrontements. Pour faciliter l’apprentissage, certains pics d’APM ont été autorisés. Par exemple, pendant une séquence de cinq secondes AlphaStar à la possibilité de monter à 600 APM, pendant quinze secondes, il peut faire 400 APM etc.. Grâce à cela, AlphaStar a pu apprendre à microgérer durant les affrontements. 
Ces valeurs de pics d’actions sont basées sur les APMs des joueurs professionnels. Le problème est que les joueurs humains n’ont pas une précision parfaite donc pour effectuer une seule action, en général ils effectuent plusieurs clics pour être sur de cliquer au moins une fois au bon endroit. On appelle cela le spam cliking. Ainsi les actions par minute d’un humain ne sont pas toutes des actions effectives. La courbe d’actions par minutes de TLO (en jaune) en est l’exemple extrême, probablement autour de seulement un dixième de ces actions ne sont pas du spam clicking. Les actions effectives par minutes (EPM) d’un humain représentent donc mieux façon de jouer d’AlphaStar qui ne fait pas ou très peu d’actions inutiles. Ainsi, il aurait probablement mieux valu utiliser les valeurs d’EPM des humains pour calculer les seuils des pics. Actuellement AlphaStar durant les affrontement présente une vitesse et une précision inhumaine. 

Du coup, les victoires d’AlphaStar deviennent quelque peu questionnables. L’agent a-t-il vraiment gagné parce qu’il a mis en place de bonnes stratégies ou simplement parce qu’il contrôlait mieux ses unités que les joueurs professionnels ? Comme chacune des parties a été jouée par un agent différent, AlphaStar s’adapte t-il vraiment aux actions de l’adversaire ou a-t-il juste une stratégie bien rodée en tête dès le début qu’il applique suffisamment bien pour gagner la plupart des parties ?

L’objectif de DeepMind est de battre les joueurs professionnels à Starcraft II, mais surtout de le faire “bien”. C’est-à-dire que l’IA doit gagner sans que l’on ait l’impression qu’elle triche ou que le match ne soit pas équitable. Pour l’instant, il semble que leur solution n’ait pas encore atteint ce stade, mais ils sont clairement sur la bonne voie. Leur solution donne l’impression qu’un apprentissage plus long et plus poussé résoudra la plupart des problèmes et questionnements à propos de la version actuelle. Le futur nous dira si c’est bien le cas.


<h2> En conclusion </h2>

La recherche évolue très vite dans le domaine des jeux vidéo et la deuxième moitié de 2018 a été très importante avec le développement de plusieurs systèmes très impressionnants. 

Un des points que la fin d’année nous à montré est que le fait de faire jouer un agent contre lui-même (self-play) donne de très bons résultats. C’est visiblement la meilleure façon (ou la plus simple) pour créer des gros volumes de données d’apprentissage. Cette approche, complétée par une bonne architecture de réseau de neurones pour un agent, est suffisante pour résoudre de nombreuses tâches si le domaine est relativement restreint (comme pour Quake III). Par contre, on observe que lorsque la complexité augmente (comme pour Dota 2 et Starcraft 2) cela ne devient plus suffisant et il faut trouver d’autres approches complémentaires.

Pour Dota2, l’approche a été de restreindre le jeu en simplifiant les règles et en codant manuellement les concepts les plus difficiles, puis au cours de l’apprentissage d’enlever au fur et à mesure les restrictions et les règles manuelles. L’exploration des différentes possibilités du jeu a été gérée principalement en ajoutant de l’aléatoire dans les parties durant l’apprentissage.

Pour Starcraft 2, l’approche a été d’utiliser ce que l’on appelle de l’imitation learning, c’est-à-dire copier le comportement des humains pour apprendre les règles fondamentales, puis apprendre à mieux jouer ensuite en self-play. L’exploration a été ici gérée par un algorithme génétique haut niveau et la League AlphaStar ce qui permet aux agents de trouver régulièrement de nouvelles stratégies.


<b>Le “bug” d’AlphaStar</b>   
Durant la seule partie en live de l’affrontement entre AlphaStar et MaNa (un des joueurs professionnels), celui-ci a remporté le match contre l’IA en exploitant une faiblesse de celle-ci. 

MaNa a réussi à faire tourner en rond AlphaStar pendant plusieurs minutes grâce à une seule unité (un Warp Prism), alors que la simple création de l'unité contre aurait résolu le problème (C’est visible dans [cette vidéo de l'événement](https://www.youtube.com/watch?v=PFMRDm_H9Sg) vers 2h39 minutes). Grâce à ce petit jeu MaNa a pu gagner la partie.

N’importe quel joueur humain (même de niveau très faible) aurait créé l’unité capable de détruire le Warp Prism ce qui aurait tout de suite stoppé la stratégie de MaNa. Seulement AlphaStar ne l'a pas fait. À ses réactions, on pouvait voir que l’agent considérait le Warp Prism comme étant important, il le surveillait, mais il n’a pas eu la réaction évidente que tout joueur humain aurait eu. Un des commentateurs a décrit cet échange comme : “C’est ce que je suis habitué à voir quand un humain joue contre une IA”. L’humain détecte une faille dans le comportement de l’IA et l’exploite à fond, l’IA étant incapable de réagir.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/sc2-warpprism.png" title="hand_real" style="width:1000px;"/> 
<figcaption> <br/> Le Warp Prism ayant fait perdre AlphaStar
 </figcaption>
</figure>
<br/>

Les développeurs d’AlphaStar considèrent qu’un des grands challenges en IA est le nombre important de possibilités qu’un système a de mal tourner. En effet, une IA classique est facile à exploiter puisqu’elle présente de nombreuses failles visibles.  Les systèmes complexes d’apprentissage pensée par OpenAI et DeepMind permettent de limiter beaucoup ces failles en trouvant les approches et les stratégies les plus fiables, mais le match en live contre MaNa nous a prouvé qu’il y en a toujours. Il semble que durant l'entraînement de l’agent ses adversaires n’ont pas utilisé cette stratégie à base du Warp Prism. En augmentant la durée de l'AlphaStar Training League et donc du temps d’apprentissage, il est probable que ce genre de faille disparaisse. 

AlphaStar ne comprend pas du tout le jeu comme les humains et des concepts évidents pour nous lui sont inconnus. Ainsi, si durant l’apprentissage, l’agent n’a jamais eu à contrer un Warp Prism présentant une telle stratégie, il ne pourra pas comprendre comment contrer cette stratégie alors qu’un humain en aura probablement l’intuition même sans connaître le jeu en particulier. En effet, les humains sont capables de tirer parti de leurs expériences passées, de les agréger comme concepts et de les généraliser à de nouveaux problèmes, ce que ne font pas encore bien les IA.

<b>Les concepts dans Montezuma’s Revenge</b>   
Quand une personne voit pour la première fois le premier niveau de Montezuma’s Revenge, même si elle ne va pas forcément savoir exactement quoi faire, certains concepts vont lui être familiers. Par exemple, la clé semble être un objet important. Il est probable qu’elle permette d’ouvrir une porte. Le crâne semble être un élément à éviter. Les échelles permettent de monter et de descendre. Le fait de tomber de haut risque d'entraîner la mort du personnage etc… Juste en observant cela, la personne va pouvoir planifier une suite d’actions pour sortir de la salle. Ces concepts généraux sont applicables à quasiment l’ensemble des jeux de plateforme de ce style.

C’est ce genre de raisonnement haut niveau basé sur une agrégation de concepts qui semblent être la base de l’intelligence humaine et qui semblent donc important à implémenter dans des systèmes d’apprentissage.

Le problème est que ces raisonnements et ces compétences sont très difficiles à mettre sous formes algorithmiques puisque l’on ne les comprend déjà pas bien chez l’humain. Quand on apprend de nouveaux concepts, on utilise en général en tant qu’humain des connaissances générale extérieures que l’on met en relation avec ces concepts. Ainsi, si l’on n’a pas accès à nos connaissances préalables (innées ou apprises), les jeux que l’on considère très simples deviennent d’un coup beaucoup plus complexes.

C’est ce qu’a voulu étudier une équipe de chercheurs de Berkeley dans [cet article](https://rach0012.github.io/humanRL_website/).

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie4/random2.gif" title="hand_real" style="width:700px;"/> 
<figcaption> <br/> Sans nos connaissances de base pour interpréter visuellement une scène, le premier niveau de Montezuma's Revenge pourrait ressembler à cela.
 </figcaption>
</figure>
<br/>

Ils ont pris un jeu de plateforme classique et ont enlevé successivement les concepts visuels que nous utilisons en temps qu’humains pour jouer à ce genre de jeu. Ainsi, cette [page interactive](https://high-level-4.herokuapp.com/experiment) permet de jouer au jeu dans une version où toutes nos connaissances antérieures sont supprimées. Le jeu s’avère relativement injouable. On peut considérer qu’un algorithme d’apprentissage par renforcement est mis dans une situation similaire au début d’un apprentissage. Cela peut expliquer en partie le manque d’efficacité de ces algorithmes par rapport aux humains en terme d’apprentissage (par exemple les 200 ans de Starcraft pour présenter le niveau d’un joueur professionnel). Comme les algorithmes n’ont pas les connaissances des bases que nous humains avons, la première étape de l’apprentissage consiste à créer ces connaissances depuis zéro grâce aux récompenses obtenues en réaction aux différentes actions, ce qui prend nécessairement du temps.
Un algorithme d’apprentissage par renforcement (A3C) a été appris sur cette version du jeu et il s’avère que l’algorithme met autant de temps que sur le jeu initial, cela ne lui pose pas de problème particulier, contrairement à nous humains.


<b>L’apprentissage des concepts</b>   
L’objectif est donc de trouver comment faire apprendre à un agent ces connaissances de bases pour lui permettre de “comprendre” le jeu et comment faire en sorte que ces connaissances s’appliquent à l’ensemble des jeu de ce style et pas seulement à un seul. 

Les deux façons d’aborder ce problème proposées par OpenAI et DeepMind à savoir la définition manuelle des concepts et l’apprentissage par imitation semblent permettre de résoudre en surface le problème, mais probablement pas suffisamment pour pouvoir bien généraliser les concepts à d'autres domaines. Il reste encore donc du travail en recherche pour atteindre ces objectifs

D’un autre côté, si on regarde les avancés liées au jeu de Go, la toute première version de l’agent AlphaGo présentait un apprentissage très similaire à celui d’AlphaStar. En effet, l’agent était initialisé avec de l’Imitation Learning puis la suite de l’apprentissage était faite en self-play. Cette version a été capable de battre les meilleurs joueurs du monde. Cependant, DeepMind en continuant à travailler sur le sujet a sorti une nouvelle version appelée AlphaGo Zero apprise intégralement en self-play. Cette version à battu AlpaGo 100 parties à zéro. Cela a montré que le fait d’imiter la façon de jouer des humains limitait en pratique l’algorithme. Les humains ne sont donc visiblement pas si bon que ça au jeu de Go et les biais induits en copiant leur façon de jouer n’étaient pas optimaux pour jouer.

Ainsi, essayer d’inculquer des notions et des concepts humains à des agents et se baser sur notre façon de réfléchir pour inventer des algorithmes d’apprentissage n’est peut-être pas la meilleure approche.
Il va être intéressant de voir si AlphaStar peut être appris de la même façon qu’Alphago Zero et présenter aussi des performances surhumaines en terme de stratégie sur Starcraft II.


<h3><U><b>Ressources : </b></U></h3>  
<p style="line-height:0.8" > <font size="-1">
http://incompleteideas.net/book/the-book.html<br>
https://www.youtube.com/watch?v=2pWv7GOvuf0&list=PLqYmG7hTraZDM-OYHWgPebj2MfCFzFObQ<br>
https://aiandgames.com <br>
http://karpathy.github.io/2016/05/31/rl/<br>
https://spinningup.openai.com/en/latest/index.html<br>
https://qz.com/1348177/why-are-ai-researchers-so-obsessed-with-games/    <br>
https://thenewstack.io/reinforcement-learning-ready-real-world/   <br> 
https://deepmind.com/research/dqn/<br> 
https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf<br> 
https://blog.openai.com/<br> 
https://gist.github.com/dfarhi/66ec9d760ae0c49a5c492c9fae93984a<br> 
https://github.com/mwydmuch/ViZDoom<br> 
https://blog.openai.com/learning-montezumas-revenge-from-a-single-demonstration/<br> 
https://medium.com/@awjuliani/on-solving-montezumas-revenge-2146d83f0bc3<br> 
https://deepmind.com/research/publications/playing-atari-deep-reinforcement-learning/<br> 
https://deepmind.com/blog/capture-the-flag/<br> 
https://arxiv.org/abs/1807.01281<br> 
https://www.youtube.com/watch?v=dltN4MxV1RI&feature=youtu.be<br> 
https://www.theverge.com/2018/7/4/17533898/deepmind-ai-agent-video-game-quake-iii-capture-the-flag<br> 
https://github.com/deepmind/pysc2<br> 
https://arxiv.org/pdf/1708.04782.pdf<br> 
https://arxiv.org/pdf/1809.07193.pdf<br> 
https://arxiv.org/pdf/1809.09095.pdf<br> 
https://arxiv.org/pdf/1708.07902.pdf<br> 
https://aiandgames.com/gvgai-part1<br> 
http://gvgai.net/<br> 
http://web.archive.org/web/20170111195314/https://openai.com/blog/GTA-V-plus-Universe/<br> 
https://www.forbes.com/sites/aarontilley/2017/10/04/grand-theft-auto-v-the-rise-and-fall-of-the-diy-self-driving-car-lab/#1d8cf3c7d7a4<br> 
https://towardsdatascience.com/reinforcement-learning-towards-general-ai-1bd68256c72d<br> 
http://web.archive.org/web/20170128070041/https://openai.com/blog/universe/<br> 
https://www.intel.ai/demystifying-deep-reinforcement-learning/#gs.hNB7y4bQ<br> 
https://towardsdatascience.com/reinforcement-learning-towards-general-ai-1bd68256c72d<br> 
https://deepmind.com/blog/deep-reinforcement-learning/<br> <font> 

---
layout: post
title:  "L'IA dans les jeux vidéo - Partie 1"
date:   2018-10-02
lang: fr
ref: jv1
categories: Vulgarisation
---


Voici les résultats lorsque l’on recherche "Intelligence artificielle dans les jeux vidéo" dans Google.

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie1/1-Google.png" title="google" style="width:650px;"/> 
</figure>
<br/>

</div>
Les premiers résultats sur de la page parlent d'eux-mêmes : l'Intelligence Artificielle (IA) dans les jeux vidéo n'est souvent pas satisfaisante. En tant que joueur, il est d’ailleurs fréquent de se retrouver face à des situations qui perdent en crédibilité du fait du comportement de l’IA.
<p align="justify">Est-ce un vrai problème ? Pourquoi l'IA semble stagner dans les jeux vidéo alors que le reste (graphismes, complexité, gameplay.....) s'améliore continuellement ? Alors que de plus en plus d’IAs sont capables de se mesurer à l’Homme sur des jeux de plateau (échecs, Go) mais aussi plus récemment de stratégie (Dota 2 en août dernier), pourquoi semblent-elles inlassablement se coincer dans le décor ou nous répéter les mêmes tirades lorsque nous jouons ? C'est ce que nous allons essayer d'étudier dans cette série d'articles.</p>

<h2>État des lieux et historique</h2>
<p align="justify">Intelligence artificielle et jeux de plateaux comme les échecs ou le Go ont toujours été liés depuis l'émergence de la discipline. En effet, ceux-ci fournissent un terrain propice afin d’évaluer les différentes méthodes et algorithmes d’IA développés. Quand les premiers jeux vidéo ont fait leur apparition, la recherche en IA battait son plein. C’est donc logiquement que l’intérêt a été porté à ce nouveau support. Cependant et pendant longtemps, la recherche a surtout permis l’amélioration des jeux vidéo et non l’inverse.</p>
<p align="justify">Le but principal de l’IA dans un jeu vidéo est de rendre le monde dépeint par le jeu le plus cohérent et le plus humain possible afin d’améliorer le plaisir et l’immersion du joueur. Cet objectif de recréer un monde au plus proche du réel peut passer par beaucoup d’approches différentes comme améliorer le comportement des <b>personnages non joueurs (PNJs)</b> ou encore générer du contenu de façon automatique.</p>
<p align="justify">A l’instar des jeux de plateau, les premiers jeux vidéo présentaient souvent une confrontation entre deux joueurs (comme Pong en 1972). Puisque deux joueurs s’affrontaient, aucune IA n’était donc nécessaire dans ce type de jeu. Mais rapidement, les jeux se complexifient et de nombreux éléments commencent à présenter des comportements indépendants des actions du joueur rendant le jeu plus interactif, comme les fantômes dans Pac Man.</p>


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie1/2-pac-man-300x294.jpg" title="google" style="width:400px;"/> 
 <figcaption> <br/> Dans Pac Man, chaque fantôme présente un comportement spécifique, qui peut être dépendant ou non des actions du joueur </figcaption>
</figure>
<br/>

<p align="justify">Il devient donc rapidement nécessaire d'implémenter de l’IA dans les jeux vidéo pour être capable de générer ce genre de comportements. Depuis, IA et jeux vidéo sont irrémédiablement liés, l’IA ayant pris une place de plus en plus importante dans les systèmes de jeu.</p>
<p align="justify">Désormais, quel que soit le type de jeux vidéo (jeux de course, jeux de stratégie, jeux de rôle, jeux de plateforme, etc ..), il y a de grandes chances pour que de nombreux éléments du jeu soient gérés par des algorithmes d’IA. Cependant cette forte imbrication entre IA et système de jeu ne s’est pas toujours faite sans accroc et, même aujourd'hui, certaines intégrations sont déficientes.</p>

<h2>IA et Jeux vidéo, faux frères ?</h2>
<p align="justify">Au commencement du domaine, il y a longtemps eu un fossé entre la recherche en IA classique et l’IA effectivement implémentée par les développeurs dans les jeux vidéo. En effet, il existait entre les deux des différences majeures dans les connaissances, les problématiques rencontrées mais aussi les façons de résoudre ces problématiques. La principale raison derrière ces différences provient sans doute du fait que ces deux approches de l’IA n’ont pas vraiment les mêmes objectifs.</p>
<p align="justify"><b>La recherche en IA classique</b> aspire en général à améliorer ou créer de nouveaux algorithmes pour faire avancer l’état de l’art. En revanche, <b>le développement d’une IA dans un jeu vidéo</b> a pour objectif de créer un système cohérent qui s’intègre le mieux possible dans le design du jeu afin d’être amusant pour le joueur. Ainsi, une IA très performante qui n’est pas bien intégrée au gameplay peut davantage desservir le jeu qu’elle ne va l’améliorer.</p>
<p align="justify">Développer une IA pour un jeu vidéo requiert donc souvent de trouver des solutions d’ingénierie à des problèmes peu ou pas du tout adressés par la recherche classique en IA. Par exemple, <b>un algorithme d’IA dans un jeu est très fortement contraint en matière de puissance de calcul, de mémoire et de temps d'exécution</b>. En effet, le jeu doit tourner par le biais d’une console ou d’un ordinateur “ordinaire” et il ne doit pas être ralenti par l’IA. C’est pourquoi certaines solutions de l’état de l’art en IA gourmandes en ressources n’ont pu être implémentées dans les jeux vidéo que plusieurs années après leur utilisation en IA classique.</p>
<p align="justify">Les solutions possibles pour résoudre un problème donné sont aussi une distinction entre les deux domaines. Par exemple, il est souvent possible de contourner une problématique difficile d’IA en modifiant légèrement la conception du jeu. De plus, dans un jeu vidéo, <b>une IA peut se permettre de tricher</b> (en ayant accès à des informations qu’elle n’est pas censée avoir, ou en ayant plus de possibilités que le joueur par exemple) afin de compenser son manque de performance. La triche d’une IA en soi n’est pas un problème tant qu’elle permet d’améliorer l'expérience du joueur. Cependant, en général, il est difficile de bien dissimuler le fait que l’IA triche et cela peut entraîner de la frustration pour le joueur.</p>


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie1/3-mario-1024x576.jpg" title="mario" style="width:800px;"/> 
 <figcaption> <br/> L’IA dans Mario kart est connue pour tricher. Il s’agit cependant dans ce jeu d’un choix assumé de conception afin de maintenir constamment une pression sur le joueur </figcaption>
</figure>
<br/>


<p align="justify">On peut noter que la plupart des grands concepts de jeux vidéo (Jeux de course, de plateforme, de stratégie, de tir, etc…) ont été créés autour des années 80 et 90. À cette époque, le développement d’une IA complexe dans un jeu était quelque chose de difficilement réalisable au vu des ressources et méthodes existantes. Les concepteurs de jeux de l’époque ont donc souvent dû composer avec le manque d’IA en faisant des choix adaptés de Game Design. Certains jeux ont même été pensés pour ne pas avoir besoin d’IA. Ces conceptions basiques ont été héritées par les différentes générations de jeux vidéo qui, pour beaucoup, restent assez fidèles aux canons du genre qui fonctionnent. Ceci peut donc aussi expliquer pourquoi les systèmes d’IA dans les jeux vidéo sont en général assez basiques quand on les compare aux approches de la recherche classique.</p>
<p align="justify">Ainsi, les méthodes que nous allons présenter pourraient surprendre par leur relative simplicité. En effet, lorsque l'on entend parler d'IA aujourd'hui, cela fait référence au <a href="https://www.saagie.com/fr/blog/qu-est-ce-que-le-deep-learning">Deep Learning</a> et donc aux réseaux de neurones très complexes et abstraits. Cependant, le Deep Learning n'est qu'un sous domaine de l'IA, et les méthodes symboliques ont été les approches communément utilisées pendant longtemps. On fait référence aujourd'hui à ces approches avec le nom <b>GOFAI ("Good Old-Fashioned Artificial Intelligence" ou “bonne vieille IA démodée” en français)</b>. Comme son surnom l'indique, l'IA symbolique n'est clairement plus l'approche la plus populaire mais elle permet cependant de résoudre de nombreux problèmes, notamment dans le cadre du jeu vidéo.</p>

<h2>L’IA pour les jeux vidéo</h2>
<p align="justify">Le critère principal de succès d’une IA dans un jeu classique est probablement son niveau d'intégration et d'imbrication dans le design du jeu. Par exemple, des PNJs ayant un comportement injustifiable peuvent briser l'expérience de jeu prévue et donc l’immersion du joueur.</p>
<p align="justify">L'un des exemples les plus classiques dans les vieux jeux est le cas où les Personnages Non Joueurs (PNJs) se retrouvent coincés dans le décor. À l’inverse, une IA qui participe pleinement à l'expérience de jeu aura forcément un impact positif sur le ressenti du joueur, en parti parce que les joueurs sont plus ou moins habitués aux comportements parfois incohérents des IA.</p>


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie1/4-fallout-1024x576.jpg" title="fallout" style="width:800px;"/> 
 <figcaption> <br/> PNJ coincés dans le décor dans Fallout 4 (2015) </figcaption>
</figure>
<br/>

<p align="justify">Suivant le type de jeu, une IA peut avoir des tâches très variées à résoudre. Nous n’allons donc pas nous pencher sur l’ensemble des cas d’utilisation possibles d’une IA dans un jeu mais plutôt sur les principaux. Il s’agira donc notamment de la <b>gestion du comportement des PNJs</b> (alliés ou ennemis) dans les jeux de tir ou les jeux de rôle, ainsi que de la gestion plus haut niveau d’un agent qui doit jouer à un jeu de stratégie.</p>

<h3>Le contrôle des PNJs</h3>
<p align="justify">Il existe un grand nombre d’approches permettant de développer des comportements réalistes dans un jeu vidéo. Cependant, le côté réaliste ne suffit pas à rendre un jeu amusant. En effet, il ne faut pas oublier que la finalité d’un ennemi dans un jeu reste en général de se faire éliminer par le joueur. Un jeu avec des adversaires trop réalistes ne sera pas forcément agréable à jouer. Par exemple, des PNJs qui passent leur temps à fuir risquent d’agacer le joueur plus qu’autre chose. Il y a donc un compromis à trouver dans le comportement des PNJs qu’il n’est pas forcément facile à balancer.</p>
Dans cette partie, nous allons faire un tour d’horizon des solutions principales pour essayer de résoudre cette problématique. Mais pour commencer, faisons le point sur quelques notions importantes.
<h4><u>Les agents</u></h4>
<p align="justify">Probablement la notion première lorsque l’on parle d’Intelligence artificielle pour les jeux vidéo, <b>un agent est une entité qui peut obtenir des informations sur son environnement et prendre des décisions en fonction de ces informations dans le but d’atteindre un objectif</b>. Dans un jeu vidéo, <b>un agent représente souvent un PNJ, mais il peut aussi représenter un système plus complet comme un adversaire dans un jeu de stratégie</b>. Il peut donc y avoir plusieurs niveaux d’agents qui communiquent entre eux dans un même jeu.</p>

<h4><u>Les états</u></h4>
<p align="justify"><b>Un état est une configuration unique de l’environnement dans lequel un agent se trouve</b>. L’état peut changer quand un agent (ou le joueur) effectue une action. Pour un agent, <b>l’ensemble des états possibles s'appelle l’espace des états</b> (state space en anglais). C’est une notion importante puisque l’idée de base de la plupart des méthodes d’IA est de parcourir ou d’explorer l’espace des états pour trouver la meilleure façon d’agir en fonction de la situation présente. Les caractéristiques de l’espace des états impactent donc la nature des méthodes d'IA utilisables.</p>
<p align="justify">Si l’on considère par exemple un agent qui définit le comportement d’un PNJ, l’espace des états peut être défini de façon assez simple : il s’agit de l’ensemble des situations dans lequel le PNJ peut se trouver. On peut ainsi mettre en place un état dans lequel le PNJ ne voit pas le joueur, un état dans lequel il voit le joueur, un état lorsque le joueur tire sur le PNJ et un état quand le PNJ est blessé. En considérant ainsi l’ensemble des situations possibles pour le PNJ, on peut déterminer les actions qu’il peut entreprendre ainsi que les conséquences de ces actions en terme de changement d’état (on parcourt l’espace des états facilement). On peut donc intégralement définir le comportement de l’agent et choisir les actions les plus pertinentes à chaque instant en fonction de ce qui se passe.</p>
<p align="justify">A l’inverse, dans le cas d’un agent qui joue à un jeu comme les échecs, l’espace des états sera l’ensemble des configurations possibles des pièces sur le plateau de jeu. Cela représente un nombre de situations extrêmement grand (10^47 états pour les échecs). Dans ces conditions, Il n’est plus possible d’explorer toutes les possibilités. Par conséquent, on ne peut plus déterminer les conséquences des actions de l’agent et donc de juger de la pertinence de ses actions. On est donc forcé d’oublier les approches manuelles et de s’orienter sur d’autres méthodes plus complexes (que l’on abordera plus tard).</p>

<h3>La recherche de chemin</h3>
<p align="justify">Avant de pouvoir modéliser le comportement d’un PNJ en explorant l’espace des états, il faut définir comment celui ci peut interagir avec son environnement et notamment, comment il peut se déplacer dans le monde du jeu. <b>La recherche de chemin</b> (pathfinding), qui est le fait de trouver le plus court chemin entre un point A et un point B, est donc souvent l’une des briques de base d’un système d’IA complexe. Si cette brique est défaillante, tout le système en pâtira. En effet, des PNJs ayant un pathfinding défaillant risquent de se coincer dans le décor et donc d’impacter négativement l’immersion du joueur.</p>

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie1/5-pathfinding.gif" title="pathfinding" style="width:500px;"/> 
 <figcaption> <br/> Pathfinding chez Skynet </figcaption>
</figure>
<br/>


<p align="justify"><b>L’algorithme le plus utilisé pour le pathfinding est l’algorithme A*</b>. Il s’agit d’une version plus rapide d’un algorithme plus ancien, <b>l’algorithme de Dijkstra</b>. Tous deux sont ce que l’on nomme des algorithmes de parcours de graphe. Pour utiliser ces algorithmes dans un jeu vidéo, le terrain de jeu (qui prend en compte les éventuels obstacles et parties cachées) est modélisé sur une grille en 2 dimensions (une grille est une forme de graphe). L’algorithme va s'exécuter dans cette grille 2D.</p>
Le principe de Dijkstra est relativement simple, il va parcourir dans l’ordre chaque case de la grille en fonction de sa distance avec la case de départ jusqu'à trouver la case de destination.


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie1/6-djikstra.png" title="dijkstra" style="width:500px;"/> 
 <figcaption> <br/> Cases explorées et solution trouvée par l’algorithme Dijkstra </figcaption>
</figure>
<br/>


<p align="justify">On peut voir avec le schéma ci-dessus que l’algorithme a parcouru toutes les cases bleues avant de trouver la case violette de destination. Cet algorithme trouvera toujours le meilleur chemin mais il est lent puisqu’il parcourt un grand nombre de cases.</p>
<p align="justify">Là où Dijkstra trouve toujours la solution optimale, A* peut ne trouver qu’une solution approchée. Cependant, il le fera beaucoup plus rapidement, ce qui est un point critique dans un jeu vidéo. En plus d’avoir l’information de distance entre chaque case avec la case de départ, l’algorithme calcule approximativement la direction générale dans laquelle il doit aller pour se rapprocher de la destination. Il va ainsi chercher à parcourir le graphe en se rapprochant toujours de l’objectif, ce qui permet de trouver une solution bien plus rapidement.</p>


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie1/7-A.png" title="dijkstra" style="width:500px;"/> 
 <figcaption> <br/> Cases explorées et solution trouvée par l’algorithme A* </figcaption>
</figure>
<br/>


Dans des cas plus complexes où l’algorithme rencontre un obstacle, il repartira du début pour trouver un autre chemin qui se rapproche de la destination mais en évitant l’obstacle.
<p align="justify">Pour les jeux plus récents en trois dimensions, le monde n’est pas représenté par une grille mais par un équivalent en 3D que l’on appelle un maillage de navigation. Un maillage de navigation est une simplification du monde qui ne considère que les zones dans lesquels il est possible de se déplacer afin de faciliter le travail de l’algorithme de pathfinding. Le principe de recherche de chemin reste le même.</p>


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie1/8-3D.png" title="3d" style="width:700px;"/> 
 <figcaption> <br/> Recherche de chemin dans un maillage de navigation 3D </figcaption>
</figure>
<br/>


<p align="justify">Ces algorithmes de parcours de graphe peuvent sembler simples et l’on peut se demander s’il s’agit vraiment d’IA. Il faut savoir qu’une bonne partie de l’IA peut se réduire finalement à des algorithmes de recherche. Cette sensation qu’un problème résolu par IA n’était finalement pas si compliqué s’appelle <b>l’effet IA</b>.</p>
<p align="justify">Mais pour ce qui est de la recherche de chemin, ce n’est pas un problème si simple, et des chercheurs s’y intéressent toujours. Par exemple en 2012, une alternative à l’algorithme A* a été développée : <b>la méthode Jump Point Search (JPS)</b>. Elle permet, lors de la recherche dans certaines conditions, de sauter plusieurs cases d’un coup et ainsi de gagner du temps par rapport à A* qui ne peut chercher son chemin que case par case.</p>
Les implémentations de pathfinding dans les jeux vidéo sont aujourd'hui souvent des variations de A* ou de JPS, adaptées aux problématiques spécifiques de chaque jeu.
<p align="justify">Le pathfinding est une composante importante d’un système comportemental des PNJs. Il y en a d’autres comme par exemple la gestion de la ligne de vue (Les PNJs ne doivent pas voir dans leur dos, ni à travers les murs) ou encore les interactions avec l’environnement qui sont nécessaires avant de pouvoir implémenter un comportement cohérent. Mais puisqu’elles ne sont, en général, pas gérées par de l’IA, nous n’allons pas nous attarder davantage dessus. Il ne faut cependant pas oublier que le système final nécessite toutes ces briques pour fonctionner. Une fois que notre PNJ est capable de se déplacer et d’interagir, on peut développer son comportement.</p>

<h2>La création de comportements Ad-hoc</h2>
<p align="justify"><b>La création de comportements Ad-hoc </b>(Ad hoc behaviour authoring en anglais) est probablement la classe de méthode la plus courante pour implémenter de l’IA dans un jeu vidéo. Le terme même d’IA dans les jeux vidéo fait encore aujourd'hui surtout référence à cette approche. Les méthodes Ad Hoc sont des systèmes experts, c’est-à-dire des systèmes où l’on doit définir manuellement un ensemble de règles qui vont servir à définir le comportement de l’IA. Ce sont donc des méthodes manuelles de parcours de l’espace des états. Leur application est donc limitée aux agents confrontés à un nombre de situations possibles assez restreint, ce qui est en général le cas pour les PNJs. Contrairement aux algorithmes de recherche comme A*, les méthodes ad-hoc ne peuvent peut-être pas réellement être définies comme de l’IA classique, mais elles sont considérées comme telles par l’industrie du jeu vidéo depuis son commencement.</p>

<h3>Les automates finis (Finite State Machine)</h3>
<p align="justify"><b>Un automate fini permet de manuellement définir les objectifs et les stimuli d’un agent afin de dicter son comportement</b>. Pour chaque objectif, on définit un ou des états et chaque état dicte une ou des actions pour le PNJ. En fonction d'événements extérieurs ou de stimuli, l’objectif du PNJ peut changer et donc l’automate peut transitionner d’un état à un autre.</p>
<p align="justify">Un automate fini est donc simplement un moyen de représenter l’espace des états d’un agent ainsi que l’ensemble des transitions entre ses différents états. Si les états et les transitions sont bien définis, l’agent présentera un comportement pertinent dans toutes les situations. Les automates finis sont en général représentés sous la forme d’un diagramme de flux comme l’exemple ci-dessous.</p>


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie1/9-automate-fini-1024x854.jpg" title="automate" style="width:700px;"/> 
 <figcaption> <br/> Un exemple d’automate fini qui reprend l’exemple précédent avec 4 états ainsi que les déclencheurs des transitions possibles entre ces états </figcaption>
</figure>
<br/>



<p align="justify">L’avantage principal des automates finis est qu’ils permettent de modéliser un comportement pertinent assez simplement et rapidement puisqu’il suffit de définir manuellement les règles qui définissent les différents états et transitions. Ils sont aussi pratiques puisqu’ils permettent de voir visuellement comment peut se comporter un PNJ.</p>
<p align="justify">Cependant, un automate fini ne présente aucune adaptabilité, puisque une fois l’automate défini et implémenté, le comportement de l’IA ne pourra pas évoluer ou s’adapter. Pour un même objectif, le PNJ effectuera toujours les mêmes actions. Il présentera donc souvent un comportement relativement simple et prévisible (même s’il est toujours possible de présenter de l'imprévisibilité en ajoutant un peu d’aléatoire dans les transitions par exemple).</p>
<p align="justify">Les automates finis, par leur conception simple, permettent de compléter, de modifier ou de debugger un système d’IA relativement facilement. Il est ainsi possible de travailler sous forme itérative afin de pouvoir rapidement vérifier les comportements implémentés.</p>
<p align="justify">Cependant, lorsque l’on veut mettre en place un comportement plus complexe avec un automate fini, cela devient vite compliqué. Il faut définir manuellement un grand nombre d’états et de transitions et la taille de l’automate peut très vite impacter la facilité de débuggage et de modification.</p>


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie1/10-arbre-comportement-1024x576.png" title="arbre" style="width:700px;"/> 
</figure>
<br/>

<p align="justify">Une évolution des automates finis essaie d’adresser ce problème : <b>les automates finis hiérarchiques</b>. Cette approche groupe des ensembles d’états similaires afin de limiter le nombre de transitions entre les états possibles. L’objectif est de garder la complexité de ce qu’on souhaite modéliser, tout en simplifiant le travail de création et de maintenance du modèle en structurant les comportements.</p>

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie1/11-automate-fini-hiérarchique-1024x328.png" title="automate_hierarchique" style="width:800px;"/> 
 <figcaption> <br/> Un exemple d’automate fini qui reprend l’exemple précédent avec 4 états ainsi que les déclencheurs des transitions possibles entre ces états </figcaption>
</figure>
<br/>

<p align="justify">Les automates finis ont été la méthode la plus populaire pour construire des comportements simples dans les jeux vidéo jusqu’au milieu des années 2000. Ils sont encore utilisés sur certains jeux récents comme la série des Batman: Arkham ou DOOM (qui utilise des automates finis hiérarchiques pour modéliser le comportement des ennemis). Cependant, ils ne sont plus les algorithmes les plus fréquemment utilisés sur le marché.</p>

<h3>Les arbres de comportements (Behaviour Tree)</h3>
<p align="justify"><b>Les arbres de comportements sont assez proches des automates finis, à la différence qu’ils se basent directement sur les actions</b> (et non les états), et qu’ils représentent les différentes transitions entre actions sous la forme d’un arbre. La structure de représentation sous forme d’arbre permet d’implémenter beaucoup plus simplement des comportements complexes. C’est aussi plus simple à maintenir, car on obtient une meilleure idée des possibilités d’action de l’agent en parcourant l’arbre qu’avec un diagramme de flux.</p>


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie1/12-arbre-comportement.png" title="automate_hierarchique" style="width:600px;"/> 
 <figcaption> <br/> Un exemple d’arbre de comportement </figcaption>
</figure>
<br/>


Un arbre de comportement est constitué de différents types de noeuds :
<ul>
 	<li>Les noeuds feuilles (ci dessus en bleu) qui n’ont aucun descendant et qui représentent des actions</li>
 	<li>Les noeuds sélecteurs (en rouge) qui ont plusieurs descendants et qui permettent de choisir le plus pertinent en fonction du contexte</li>
 	<li>Les noeuds séquences (en jaune) qui exécutent tous leurs noeuds descendants dans l’ordre et permettent donc de faire des séquences d’actions</li>
</ul>
<p align="justify"><b>Un arbre de comportement est exécuté de haut en bas et de gauche à droite</b> On commence du noeud racine (le tout premier noeud) jusqu'à la feuille la plus à droite. Une fois arrivé à la feuille et l’action exécutée, on retourne au noeud racine et on parcourt jusqu'à la feuille suivante.</p>
Ainsi, dans l’arbre ci-dessus:
<p align="justify">Le PNJ va aller jusqu'à la porte, ensuite suivant le type de porte et les objets qu’il a sur lui il va soit ouvrir la porte, soit la déverrouiller puis l’ouvrir, soit la détruire. Il va ensuite passer la porte et la refermer. On voit que cet arbre permet de définir différentes séquences d’actions qui permettent d’atteindre un même objectif : passer de l’autre côté d’une porte.</p>
<p align="justify">Il est bien sûr possible de construire des arbres beaucoup plus complets qui peuvent représenter l’ensemble des informations de comportement du PNJ. Par exemple ci-dessous un arbre de comportement qui permet de passer par une porte ou par une fenêtre suivant le contexte.</p>


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie1/13-arbre-comportement-1024x309.png" title="arbre_big" style="width:1000px;"/> 
 <figcaption> <br/> Un exemple d’arbre de comportement </figcaption>
</figure>
<br/>


<p align="justify">Les arbres de comportements présentent globalement les mêmes limitations que les automates finis. Principalement, ils décrivent un comportement fixe et prédictible puisque toutes les règles et les actions sont définies en amont manuellement. Cependant, leur architecture sous forme d’arbre permet de faciliter le développement et de limiter les erreurs permettant ainsi de créer des comportements plus complexes.</p>
Les arbres de comportements ont été utilisés pour la première fois avec Halo 2 en 2004. Ils ont depuis été utilisés dans un certain nombre de licences à succès comme Bioshock en 2007 ou Spore en 2008 par exemple.
<h3>Les approches basées sur l’utilité (utility based AI)</h3>
<p align="justify">Avec cette approche, plutôt que de transitionner d’un état à un autre en fonction d’évènements extérieurs, <b>un agent va constamment évaluer les différentes actions possibles qu’il peut effectuer à un instant donné et choisir l’action qui a la plus forte utilité pour lui dans les conditions présentes</b>. Pour chaque action on définit en amont une courbe d’utilité en fonction des conditions. On peut par exemple définir une courbe d’utilité sur le fait de tirer sur le joueur en fonction de la distance avec celui-ci. Plus le joueur est proche plus il semble utile de tirer dessus pour éviter de se faire éliminer. En choisissant différents types de courbes (linéaires, logarithmiques, exponentielles, etc..) pour les différentes actions, on peut prioriser quelle action effectuer dans quelles conditions sans avoir à détailler manuellement tous les cas possibles.</p>


<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie1/14-courbe-utilité.png" title="arbre_big" style="width:650px;"/> 
 <figcaption> <br/> Un exemple d’approche avec trois actions possibles ainsi que leur courbe d’utilité respective en fonction d’un même paramètre </figcaption>
</figure>
<br/>


<p align="justify">Cette approche permet donc de développer des comportements complexes et beaucoup plus modulaires sans avoir à définir un très grand nombre d’états. La liste des actions possibles peut facilement être complétée ou modifiée avec ce type d’approche, ce qui n’était pas le cas avec des automates finis ou des arbres de comportements. Cependant, il est quand même nécessaire de définir toutes les courbes d’utilité et de bien les paramétrer pour obtenir les comportements voulus.</p>
Cette approche, grâce à ses avantages, est de plus en plus utilisée dans les jeux vidéo. On peut citer notamment Red Dead Redemption (2010) et Killzone 2 (2009).
<p align="justify">Dans ce premier article, nous avons principalement parcouru les méthodes classiques ad hoc. Comme on a pu le constater, ces différentes méthodes permettant de modéliser des comportements ont chacune leurs avantages et inconvénients. Voici donc un petit tableau récapitulatifs des différentes approches abordées jusqu’ici.</p>

<br/>
<figure align="center">
	<img src="{{ site.baseurl }}/assets/Posts/IA_JV/Partie1/tab_jeux.png" title="tableau" style="width:650px;"/> 
</figure>
<br/>




<p align="justify">On peut remarquer que toutes ces approches présentent un inconvénient commun : les comportements définis ne peuvent pas du tout s’adapter à la façon de se comporter du joueur. Dans le deuxième article nous allons donc nous intéresser à des méthodes plus poussées commes la planification ou les approches basées sur du Machine Learning pour essayer de corriger cet inconvénient.</p>
&nbsp;
<h3 align="center"><u>Références :</u></h3>
Stuart Russell and Peter Norvig. 2009. Artificial Intelligence: A Modern Approach (3rd ed.). Prentice Hall Press, Upper Saddle River, NJ, USA.  
Yannakakis, Georgios N., and Julian Togelius. Artificial Intelligence and Games. Springer, 2018.  
http://theory.stanford.edu/~amitp/GameProgramming/AStarComparison.html  
http://sitn.hms.harvard.edu/flash/2017/ai-video-games-toward-intelligent-game/  
https://aiandgames.com/  
http://www.gamasutra.com/blogs/ChrisSimpson/20140717/221339/Behavior_trees_for_AI_How_they_work.php  
http://apexgametools.com/products/apex-utility-ai-2/   
https://alastaira.wordpress.com/2013/01/25/at-a-glance-functions-for-modelling-utility-based-game-ai/  
<h3 align="center"><u>Images:</u></h3>
http://www.todayifoundout.com/wp-content/uploads/2013/08/pacman.jpg   
https://www.youtube.com/watch?v=DOwHStswpIE.   
https://www.youtube.com/watch?v=M7TicvLXrQo.   
https://knowyourmeme.com/photos/573514-dafuq  
http://theory.stanford.edu/~amitp/game-programming/a-star/dijkstra.png  
http://theory.stanford.edu/~amitp/game-programming/a-star/best-first-search.png  
http://masagroup.github.io/recastdetour/recast_intro.png  
https://i0.wp.com/sitn.hms.harvard.edu/wp-content/uploads/2017/08/Slide01.jpg?resize=768%2C576  
https://i1.wp.com/aiandgames.com/wp-content/uploads/2018/08/DoomFSM5.png?fit=711%2C400&amp;ssl=1  
https://i1.wp.com/aiandgames.com/wp-content/uploads/2018/08/DoomHFSM2-1.png?fit=711%2C400&amp;ssl=1  
http://outforafight.files.wordpress.com/2014/07/selector1.png  
http://outforafight.files.wordpress.com/2014/07/selector3.png
http://apexgametools.com/wp-content/uploads/2016/02/xUtilityCurves.png.pagespeed.ic.YlCW8ubCi0.png

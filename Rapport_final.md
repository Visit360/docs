BERNERD - Clara  
FAGHLOUMI - Ayman  
NGUYEN - Justin  


<h1 align="center">Rapport final - Visit360</h1>

# Table of Contents
1. [Abstract](#abstract)
2. [Résumé](#résumé)
3. [Contexte](#contexte)
4. [Technologies employées](#tech)
5. [Architecture technique](#archi)
6. [Réalisations techniques](#realisation)
7. [Gestion de projet](#gestion)
8. [Outils](#outils)
9. [Métriques logicielles](#metriques)
10. [Conclusion](#conclusion)
11. [Annexes](#annexe)



# Abstract
Virtual tour creation tools are not a new technology, the many existing solutions are proof of this.  
However, most of them are under a license that is not free of rights.  
Our project, visit360, will allow the creation and visualisation of virtual tours using panoramic photos.  
We will use the Pannellum library, which is open source, to create a web demonstration tool.

# Résumé
Les outils de création de visite virtuelle ne sont pas une nouvelle technologie, les nombreuses solutions existantes en sont la preuve.  
Cependant, la plupart sont sous license payante non libre de droits.  
Notre projet, visit360 permettra de réaliser et visualiser des visites virtuelles à l'aide de photos panoramiques.  
On utilisera pour cela la bibliothèque Pannellum, qui est open source pour réaliser un outil de démonstration web.
# Contexte <a id="contexte"></a>

### **Rappel du sujet** 

L'objectif du projet est de développer un outil (web) facilitant la construction de visites virtuelles.  
 
Une visite virtuelle est un moyen de simuler la visite d'un site à 360°. Plusieurs images panoramiques se succèderont au moyen d'interaction avec l'utilisateur. La visite virtuelle permet également à l'utilisateur de naviguer dans chacune des scènes, de lire des informations et de se repérer sur une minimap (ou plan de la visite) ainsi que de garder une trace de sa navigation dans la visite grâce à un historique.  

L'outil web que nous avons conçus contient plusieurs modes qui sont : 
* **Le mode visualisation** : il nous permet d'avoir un aperçu de la visite créée ou modifiée dans le mode édition. Nous pouvons également observer la mini map qui correspond au plan de la visite. 
* **Le mode édition** : permettant de créer les visites ou de modifier des visites importées
* **Le mode édition minimap** : permet de réaliser une minimap correpondante à la visite.

### **Cahier des charges**

Lors des premières semaines de notre projet, nous avons réalisé un cahier des charges à la suite d'une réunion avec notre tuteur et porteur de projet, monsieur Didier DONSEZ. Nous avons ainsi défini les fonctionnalités suivantes pour chaque mode.

**Mode visualisation**
* Visualiser les panoramas
* Passer d’un panorama à un autre (par les portes)
* Lire les points d’information
* Avoir accès à la console d’historique et pouvoir la réduire et faire défiler.
* Pouvoir supprimer l’historique via un bouton
* Se repérer sur la Minimap avec un changement de couleur par exemple
* Pouvoir se déplacer dans les panoramas de la Minimap en sélectionnant des points d’intérêt.  
  

**Mode édition**
* Sélectionner les panoramas à ajouter/modifier
* Ajouter des hotspot pour chaque panorama
    * Porte : permet de naviguer d’une panorma à l’autre
    * Fenêtre contextuelle d’information : affiche des renseignements statiques

**Mode édition minimap**
* Modifier le MiniMap en fonction du plan d’étage :
    * Ajouter des points d’intérêt
    * Associer des panorama au point d'intérêt précédement ajoutés

Nous avons également définit des fonctionnalités facultatives 

**Fonctionnalités facultatives du mode visualisation**

* Donner la possibilité à l'utilisateur d'ajouter des sons aux hotspots
* Couper ou ajuster le son
* Pouvoir cliquer sur les sorties affichées dans l’historique pour accéder au panorama correspondant.
* Adapter l’outil à l’appareil de l’utilisateur (comme un casque VR, un téléphone ou un ordinateur).
    * Sur le téléphone par exemple, ouverture automatique de popup pendant le centrage (en utilisant un accéléromètre)

**Fonctionnalités facultatives du mode édition**

* Importer des panoramas
* Importer le plan de masse de la visite
* Ajouter d'autres hotspots 
    * Fenêtre contextuelle d’information dynamique : affiche l’information dynamique (en temps réel)
    * Son spacial : ajouter du son au panorama
    Modifier un MiniMap :
* Créer sa propre minimap (création de plan)
* AI pour détection de portes, capteurs...


# Technologies employées <a id="tech"></a>

Pour réaliser notre projet, nous avons utilisé différentes technologies.
### **Caméra insta360 one RS**

Nous avons tout d'abord réalisé plusieurs photographies panoramiques de différents bâtiments :
* Polytech Grenoble (14 Place du Conseil National de la Résistance, 38400 Saint-Martin-d'Hères)
* Fablab MASTIC (740 Rue de la Piscine)
* Appartement connecté DOMUS (au sein de la MACI - 339 Av. Centrale, 38400 Saint-Martin-d'Hères)
* La Casemate Grenoble (2 Pl. Saint-Laurent, 38000 Grenoble)

Pour réaliser ces différentes photos, nous avons eu accès à une caméra insta 360 oneRS. Elle nous a permis de prendre des photo facilement grâce à l'application smartphone insta360. Nous disposions alors d'une prévisualisation des photo directement sur notre écran ce qui nous a permis d'être efficace.

<img src="https://github.com/Visit360/docs/blob/main/insta360-one-rs-1.jpg" width="300" height="300">

### **Bibliothèque Pannellum**
Pour réaliser, visualiser et modifier les visites, on utilise la bibliothèque Pannellum.  
Pannellum est une bibliothèque *open source* pour la visualisation panoramique pour le web.
C'est également grâce à cette bibliothèque que nous avons pu gérer le zoom au sein de l'image panoramique, l'ajout d'hotspot (portes et informations), et la sauvegarde des visites sous formats JSON.  
Même si cette bibliothèque offre plusieurs fonctionnalités très interessantes en terme de visualisation d'image panoramique, elle ne contenait pas tout les éléments dont nous avions besoin. Par exemple, Pannellum ne permet pas à l'utilisateur de supprimer des hotspot. L'essentiel de notre travail de développement s'est donc porté sur ces fonctionnalités non disponibles.  

<img src="https://github.com/Visit360/docs/blob/main/Pannellum.jpeg" width="300" height="300">

### **HTML - JAVASCRIPT - CSS**
Pour coder le site web, nous avons choisi d'utiliser ces trois technologies très classique. Nous n'avons pas utilisé d'autres outils de frontend tel que React ou Angular car cela nous a semblé innutile étant donné la simplicité des pages web à programmer.  


<img src="https://github.com/Visit360/docs/blob/main/html_js_css.png" width="300" height="300">


# Architecture technique <a id="archi"></a>
L'outil repose sur une architecture client serveur et on utilise une Github page pour le déploiement. Selon le site doc.GitHub.com : "GitHub Pages est un service d'hébergement de site statique qui récupère les fichiers HTML, CSS et JavaScript directement à partir d'un référentiel sur GitHub, exécute éventuellement les fichiers via un processus de construction et publie un site Web."  
En effet, étant donnée que le projet est encore dans une phase de démonstration, nous n'avons pas besoin de base de données, ni d'une architecture très poussée.Les panoramas sont déjà importés dans le dépôt et l'utilisateur n'a pas les moyens pour l'instant d'importer ses propres images. Les visites seront réalisées sous format JSON. 

# Réalisations techniques <a id="realisation"></a>

Afin de répondre aux différents besoins exprimés en termes de fonctionnalités dans le cahier de charge, nous avons séparé trois modes d'utilisation de VISIT360 : 
* **Le mode édition** : il nous permet de créer une visite virtuelle d'un bâtiment à partir des images panoramiques disponibles ou de modifier une visite importée. Dans ce mode, l'utilisateur peut choisir les scènes à ajouter à sa visite tout en spécifiant le panorama initiale de celle-ci. Il est libre d'ajouter des hotspots (portes/passerelles) pour créer un chemin entre les scènes. Il peut aussi ajouter des points d'information qui peuvent être une description d'un objet ou d'un endroit par exemple. Les points d'information et les portes peuvent être supprimés dans ce mode d'utilisation. Quand l'utilisateur finit son édition de la visite, il peut l'exporter et celle-ci sera téléchargée sous format Json. Cette même visite pourra être importée par la suite sous le même format pour lui appliquer de nouvelles modifications.  
Quelques détails techniques ont éte pris en considération pour limiter les erreurs de l'utilisateur tels que le renvoi des avertissements en cas de tentatives d'ajout de scènes avant d'en sélectionner une ou en cas de duplication du nom de la scène.

* **Le mode édition minimap** : ce mode permet de réaliser une mini map correpondante à la visite en associant chaque point d'intérêt à la scène qu'il représente. Ainsi nous pouvons permettre le déplacement dans la visite à partir de la mini map et l'utilisateur peut se repérer facilement, grâce au changement de couleur, dans la mini carte qui dans notre exemple représente le plan de masse du bâtiment.  
Pour aider l'utilisateur à associer les scènes aux points d'intérêt, on lui propose une liste déroulante avec les noms de scènes de la visite editée. Aussi, la suppression de ces est possible avec un simple clic droit.  

* **Le mode visualisation** : il nous permet d'avoir un aperçu de la visite créée ou modifiée dans le mode édition. Nous pouvons également observer la mini map qui correspond au plan de la visite. L'utilisateur peut naviguer dans la visite à travers les portes figurantes dans chaque scène, ou en sélectionnant sa prochaine destination directement de la mini map. Pour revenir sur ces pas, il suffit de sélectionner l'une des scènes présentes dans l'historique.  

Pour la réalisation de ces fonctionalités, on s'est basé sur la bibliothèque Pannellum v2.5.6 pour avoir les fonctionnalités de base, notamment la navigation entre les scènes, mais on a aussi profité de son API Open Source afin d'implémenter d'autres fonctionnalités telles que la suppression des différents hotspots, la configuration des visites ainsi que l'import et l'export de celles-ci.

# Gestion de projet <a id="gestion"></a>

Gestion de projet (méthode, planning prévisionnel et effectif, gestion des risques, rôles des membres ...)  

Dans cette partie, nous allons aborder notre gestion de projet. 

Tout d'abord, nous avons défini les rôles de chaque membre du groupe. Etant donné que nous somme une petite équipe de développement de seulement 3 personnes, nous avons décidé qu'il fallait seulement désigner un chef de projet : Justin NGUYEN. C'est lui qui s'est occupé de la communication avec notre tuteur et qui a organisé les réunions de groupes. Le fait qu'on se connaissait tous depuis déjà un certain temps à grandement aidé au bon déroulement du projet, nous n'avons pas eu de soucis de communication particulier. 

Nous avons mis en place un planning prévisionnel au départ de notre projet sur une plateforme appellée Monday.com. C'est une plate-forme Web et une application mobile dédiée à la gestion de tâches, notamment le suivi de projets, du temps et de la collaboration en équipe. Elle se présente sous la forme d'un tabeau avec différentes tâches à effectuer, auxquelles on peut y associer des dates de début et de fin, des niveau de criticité, et des membre de l'équipe affectés à celles-ci. Au bout de quelques jours seulement, nous nous sommes rendu compte que cet outil très complet était plus déstiné à des équipes plus conséquentes que la notre. En effet, comme nous nous sommes rejoint pour travailler quasiment tout les jours du projet, nous avons constaté qu'un journal de bord était suffisant pour notre groupe. Chaque jours, on pouvait indiquer les tâches que nous avions réalisées tout en ajoutant les tâches que nous voulions réaliser la prochaine séance.

Notre méthode de travail se divise en plusieurs partie : 
-Lors des premières semaines du projet, nous avons principalement réalisé les tâches suivantes : définir le cahier des charges avec le plus de précision possible, réaliser une maquette de notre site web, choisir les technologies que nous allions utiliser tout au long du projet. Lors de cette première phase, nous avions tous le même rôle et nous avons travaillé de manière synchronisée sur chaque tâche.  
-Dans une seconde phase, nous avons commencé le développement. Lors de cette phase, nous nous somme divisé le travail en terme de fonctionnalité. Ayman et Clara codaient les différentes fonctionnalités précédemment énnoncés dans le cahier des charges, sans se soucier du "style" où de l'affichage. Justin reprennait les différentes fonctionnalités, les ajoutaient ensembe et réalisait le CSS associé.   
-A chaque ajout de fonctionnalité, nous retestions l'ensemble du code afin qu'il soit le plus stable possible.  
-Entre temps, nous sommes allé prendre des photos dans différents bâtiment et nous avons créé des visite pour chaqu'un d'entre eux  
-Lors des dernières semaines, nous nous sommes concentré sur les test finaux, la correction de bugs, la promotion de notre projet (réalisation de poster et de flyer), mais également la documentation et le commentaire de code. Il est essenteil pour nous que notre code soit bien commenté, pour nous même et pour les futurs étudiants qui reprendront le projet après nous.    

Nous avons finalement pu réaliser toutes les fonctionnalités se trouvant dans le cahier des charges initial, plus quelques fonctionnalités bonus que nous avons évidement définies avec notre tuteur de projet. Nous considérons alors que nous avons eu une gestion de projet efficace et adaptée à notre groupe.


# Outils <a id="outils"></a>
Utilisation de Github pour l'organisation contenant le dépôt du code et la documentation mais aussi l'hébergement de la Github page.


# Métriques logicielles <a id="metriques"></a>
Métriques logiciels : lignes de code, langages, performance, temps ingénieur (d'après vos journaux), la répartition des lignes de code et des commits en pourcentage entre les membres du projet ...)

nombre de commit par personne :  
Clara = 33 
Justin = 21
Ayman = 42

nombre de ligne de code : 



# Conclusion <a id="conclusion"></a>
Travailler sur ce projet à temps plein durant plusieurs mois nous à permis de développer nos compétences de développement, de gestion de projet, de prise en main de nouvelles technologies (caméra 360/pannellum) et de communication (aussi bien au sein de notre groupe qu’avec des acteurs extérieurs au projet comme les responsables de différents bâtiments). Ce fut une expérience très enrichissante pour nous et nous avons apprécié travailler sur ce projet innovant.

Nous avons réussit à développer toutes les fonctionnalitées attendues dans le cahier des charge, avec quelques fonctionnalités supplémentaires : 
* L’import de visites déjà préchargées dans le dépôt git (Polytech, Domus, FabLab et Casemate)
* L’ajout d’un bouton “Clear Visit” permettant à l’utilisateur de revenir à l’état initial (ouverture de la fenêtre)
* L’ajout d’une barre de recherche pour aider l’utilisateur à trouver les scènes déjà ajoutées 

La suite de notre projet consistera à réaliser les fonctionnalités optionnelles précédemment énoncées. 


# Annexes <a id="annexe"></a>
### **Références** 
* Définition d'une GitHub Page : "https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages"
* Petroff, Matthew A. "Pannellum: a lightweight web-based panorama viewer." Journal of Open Source Software 4, no. 40 (2019): "https://doi.org/10.21105/joss.01628"
* Documentation Pannellum : "https://pannellum.org/documentation/overview/"







 

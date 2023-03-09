BERNERD - Clara  
FAGHLOUMI - Ayman  
NGUYEN - Justin  


<h1 align="center">Rapport final - Visit360</h1>

# Table of Contents
1. [Abstract](#abstract)
2. [Résumé](#résumé)
3. [Contexte](#contexte)
4. [Technologies employées](#tech)
5. [Architecture techniques](#archi)
6. [Réalisations techniques](#realisation)
7. [Gestion de projet](#gestion)
8. [Outils](#outils)
9. [Métriques logicielles](#metriques)
10. [Conclusion](#conclusion)



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

L'outil web contient plusieurs modes qui sont : 
* **Le mode visualisation** : il nous permet d'avoir un aperçu de la visite créée dans le mode édition. Nous pouvons également observer la minimap qui correspond au plan de la visite.
* **Le mode édition** : permettant de créer les visites
* **Le mode édition minimap** : permet de réaliser une minimap correpondant à la visite.



### **Cahier des charges**

Lors des premières semaines de notre projet, nous avons réalisé un cahier des charges à la suite d'une réunion avec notre tuteur et porteur de projet, monsieur Didier DONSEZ. Nous avons ainsi défini les fonctionnalités suivantes pour chaque mode.

**Mode visualisation**
* Visualiser les panoramas
* Passer d’un panorama à un autre (par les portes)
* Lire les points d’information
* Avoir accès à la console d’historique et pouvoir la réduire et faire défiler.
* Pouvoir supprimer l’historique via un bouton
* Se repérer sur la Minimap avec un changement de couleur par exemple
* Pour se déplacer dans les panoramas de la Minimap en sélectionnant des points d’intérêt.  
  

**Mode édition**
* Sélectionnez les panoramas à ajouter/modifier
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

Pour réaliser ces différentes photos, nous avons eu accès à 


### **Bibliothèque Pannellum**
Pour réaliser, visualiser et modifier les visites, on utilise la bibliothèque Pannellum.  
Pannellum est une bibliothèque *open source* pour la visualisation panoramique pour le web. 


# Architecture technique <a id="archi"></a>
L'outil repose sur une architecture client serveur et on utilise une Github page pour le déploiement car nous n'avons pas besoin de base de données.
Les panoramas sont déjà importés dans le dépôt et la visite est stockée sous un format JSON.

# Réalisations techniques <a id="realisation"></a>

# Gestion de projet <a id="gestion"></a>

Gestion de projet (méthode, planning prévisionnel et effectif, gestion des risques, rôles des membres ...)  

Au départ nous utilisions Monday pour planifier les tâches de chacun mais au fur et à mesure de l'avancement du projet, l'utilisation d'un journal de bord était devenue suffisante pour notre groupe: on pouvait indiquer les tâches que nous avions réalisé chaque jour tout en ajoutant les tâches que nous voulions réaliser la prochaine séance.


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
Conclusion (Retour d'expérience)







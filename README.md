# Analyse multivariée de données ouvertes choisies librement

Ce projet s'étale sur plusieurs modules du cours de Science des Données Biologiques 2. Il nécessite d'avoir assimilé l'ensemble des notions des modules 6 à 10. Il correspond au dépôt GitHub <https://github.com/BioDataScience-Course/B06Ga_open_data>.

## Introduction 

La science est de plus en plus *ouverte* (le terme en anglais est **Open Science**). Il s'agit ici de rendre les analyses accessibles et de documenter tout le processus qui mène aux résultats obtenus. Les publications sont aussi librement accessibles en Open Science. Cette volonté de rendre la science plus transparente va de pair avec l'*Open Data*, données ouvertes (que nous verrons lors du module 10). Cela signifie que les données sont également rendues publiques et accessibles.

Lors de la publication d'articles scientifiques, il est de plus en plus courant que les revues demandent aux auteurs de rendre leurs données disponibles en Open Data. Il est même conseillé de fournir le code employé pour réaliser les analyses statistiques. On peut mettre en avant quelques avantages de ces bonnes pratiques :

-   Reproductibilité : en fournissant les données et le code, les autres scientifiques peuvent reproduire les analyses et les résultats. Cela contribue à renforcer la transparence et la confiance dans les conclusions de l'étude.

-   Vérification des résultats : les données et le code peuvent être utilisés pour vérifier les résultats de l'étude et détecter les erreurs ou les biais. Cela permet d'améliorer la qualité de la recherche scientifique et d'éviter, ou du moins, limiter fortement les erreurs.

-   Réutilisation des données : les données peuvent être réutilisées pour d'autres analyses, ce qui permet de maximiser l'utilisation des ressources.

-   Accélération de la recherche : en partageant les données et le code, les autres scientifiques peuvent construire sur les résultats antérieurs plus rapidement et plus efficacement. Cela aide à trouver des solutions plus rapidement.

-   Meilleure collaboration : en partageant les données et le code, les scientifiques peuvent collaborer plus facilement pour résoudre des problèmes complexes.

Comme expliqué dans le module 10 du cours de Science des Données II, la mise à disposition des données (et du code) doit respecter certains critères que l'on peut regrouper sous l'acronyme FAIR pour **Findable**, **Accessible**, **Interoperable**, **Reusable**. Les données qui ne se conforment pas à ces critères peuvent être partiellement ou même totalement inutilisables.

## Objectifs

Ce projet est **libre** et sera réalisé en **groupes de quatre étudiants**. Répartissez-vous le travail. Il permettra de démontrer que vous avez acquis les compétences suivantes :

-   choix des données ouvertes

    -   trouver des données ouvertes qui se prêtent à une analyse multivariée d'ordination et de classification (tout le monde cherche et vous choisissez de manière collégiale le jeu de données à retenir au final)

    -   récupérer les données de la meilleure manière possible, tout en respectant les contraintes d'un dépôt GitHub

-  gestion de base de données et principe FAIR

    -   présenter ses données dans une base de données relationnelle SQLite, en respectant les bonnes pratiques de gestion des données (tables 3NF, clés primaires et étrangères correctement définies)

    -   critiquer les données trouvées selon le principe FAIR (chaque étudiant rédige la partie relative à un des critères)

-  réalisation d'analyses multivariées d'ordination et de classification

    -   réaliser une analyse de type CAH ou k-moyennes sur ces données et l'interpréter

    -   réaliser une analyse de type ACP ou AFC ou MFA ou MDS sur ces données et l'interpréter

    -   réaliser une SOM sur ces données et l'interpréter (tous les étudiants doivent rédiger une partie du rapport, répartissez-vous les tâches au départ)

## Consignes

### Module 6

La première étape consiste en la recherche de données ouvertes. Vous suivrez les instructions du fichier `data/README` pour récupérer vos données depuis une URL de téléchargement direct avec mise en cache dans `data/cache`. Si ce n'est pas possible, il faudra le justifier dans le document `open_data.qmd`(à compléter lors du module 10) et placer les données manuellement dans le sous-dossier `data` (max 50Mo).

**Attention, il est impératif que vos enseignants valident les données choisies.**

Il est préférable d'avoir plusieurs tableaux connectables entre eux. Voici quelques conseils dans le choix de vos données : 

-   avec au **minimum 100 lignes**
-   avec au moins huit variables quantitatives continues
-   avec au moins deux variables qualitatives

Voici plusieurs sites que vous pouvez utiliser pour rechercher vos données :

-   [Zenodo](https://zenodo.org/)

-   [Dryad](https://datadryad.org/)

-   [Free and open access to biodiversity data](https://www.gbif.org/)

-   [The Knowledge Network for Biocomplexity](https://knb.ecoinformatics.org/data)

-   [EDI Data Portal](https://portal.edirepository.org/nis/home.jsp)


### Module 7 & 8

Dans le script R nommé `explo.R`, vous explorez vos données afin de réaliser des analyses multivariées de classification réalisée au module 6 et d'ordination vue au module 7 et 8. 


### Module 9

Vous allez retravailler les données pour les placer dans une base de données sqlite nommée `data.sqlite` dans le sous-dossier `data`. Vos données doivent être 3NF et les clés primaires et étrangères doivent être définies à l'aide du package {dm}. Vous expliquez ce que vous avez fait et en quoi le schéma de votre base de données est correct, selon vous, dans le fichier `database.qmd`.

Dans le script nommé `explo.R`, vous réalisez une MDS métrique ou non métrique sur vos données selon ce qui s'applique le mieux.

Enfin, vous commencez à compléter le document `report.qmd` et vous sélectionnez vos meilleures analyses de classification et d'ordination réalisées sur vos données. Attention, vos analyses dans le report doivent se baser sur les données présentes dans la base de données `data.sqlite`.

### Module 10

Expliquez de manière détaillée en quoi les données choisies répondent (ou non) au principe FAIR. Il s'agit de formuler une critique des données sélectionnées sur base du principe FAIR dans le document `open_data.qmd`.

Enfin, terminez de compléter le rapport `report.qmd`. Vous réalisez et interprétez une analyse multivariée de type SOM sur les données choisies.

N'oubliez pas de réaliser un "Rendu" des documents en HTML à la fin pour vérifier que tout fonctionne bien. Corrigez les erreurs éventuelles rencontrées à ce stade avant de clôturer votre projet. Vérifiez également que votre dernier commit a bien été pushé sur GitHub avant la deadline.

## Utilisation de l’IA

Dans le cadre de votre travail, vous pouvez utiliser l’intelligence artificielle. Il est toutefois impératif de préciser, dans la section « Matériel et méthodes » du projet, que l’IA a été utilisée, en indiquant le contexte et la manière dont elle a été employée. Voici un exemple de formulation :

```
La relecture (orthographe et syntaxe) a été réalisée à l’aide de Microsoft Copilot (basé sur GPT-5), consulté le 12 janvier 2026.
```
Attention, vous devez néanmoins employer le dialecte SciViews-R afin de garantir votre compréhension du cours de Science des données biologiques 2 lors de la production de code R dans votre projet.

Un chatbot SciViews est également disponible dans RStudio (Saturn Cloud), via l’addin Help. Il répond aux questions relatives au langage R, aux statistiques et à la science des données.

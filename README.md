# Projet Économétrie : Performances et Salaires en NBA (2024-2025)

## 📌 Présentation du projet
Ce projet a été réalisé dans le cadre d'un cours de Science des Données / Économétrie. L'objectif principal est d'analyser un jeu de données réelles de la NBA pour répondre à la problématique suivante : **Les statistiques permettent-elles réellement de refléter la valeur (le salaire) d'un joueur NBA ?**

Nous même amateurs de la NBA, nous allons essayer ici de démontrer que la NBA fonctionne sur deux économies parallèles : si les statistiques expliquent le salaire des joueurs de rotation, d'autres facteurs (statut, expérience) prennent le relais pour les superstars.

## 🎯 Objectifs et Méthodes Statistiques
Ce projet valide la maîtrise d'un pipeline complet en Data Science sous **R**, allant du nettoyage des données jusqu'à la modélisation mathématique avancée. 

Les méthodes suivantes ont été implémentées et interprétées :
* **Analyses Univariées :** Étude des distributions (histogrammes, boxplots, valeurs atypiques) des salaires et de l'origine des joueurs.
* **Analyses Bivariées & Tests d'hypothèses :** 
  * Corrélation et Régression Linéaire Multiple (Salaire ~ Performance + Âge + Disponibilité) avec analyse des résidus (normalité, homoscédasticité).
  * Test du Chi-2 simulé par Monte-Carlo.
  * Analyse de la Variance (ANOVA).
* **Réduction de dimensionnalité :** Analyse en Composantes Principales (ACP) pour identifier les profils de jeu.
* **Machine Learning (Non supervisé) :** Classification Ascendante Hiérarchique (CAH) et Algorithme des K-Means pour segmenter la ligue en clusters de profils de joueurs.

## 🛠️ Technologies Utilisées
* **Langage :** R
* **Environnement :** RStudio / R Markdown (Génération de rapport PDF automatisé).
* **Packages principaux :** `tidyverse` (manipulation de données), `ggplot2` (dataviz), `factoextra` (clustering), `broom` et `vtable` (formatage statistique).

## 📂 Structure du dépôt
* `Projet_Econometrie_Remy_Enzo24.Rmd` : Le script source contenant l'intégralité du code commenté.
* `Projet_Sans_Code.pdf` : Le rapport final généré, mis en page et interprété.
* `base_stats_NBA_24_25.csv` & `NBA Player Salaries_2024-25_1.csv` : Les jeux de données bruts (statistiques officielles et salaires Kaggle).

## 🚀 Comment reproduire l'analyse ?
1. Clonez ce dépôt sur votre machine locale.
2. Assurez-vous d'avoir installé R et RStudio.
3. Ouvrez le fichier `.Rmd`. Le package `pacman` se chargera d'installer et de charger automatiquement les dépendances nécessaires.
4. Pour l'export il vous faudra rentrer ça dans la **Console** directement selon si vous voulez avoir ou non le code :
   * rmarkdown::render("Projet_Econometrie_Remy_Enzo24.Rmd", params = list(afficher_code = TRUE), output_file = "Projet_Avec_Code.pdf")
   * rmarkdown::render("Projet_Econometrie_Remy_Enzo24.Rmd", params = list(afficher_code = FALSE), output_file = "Projet_Sans_Code.pdf")

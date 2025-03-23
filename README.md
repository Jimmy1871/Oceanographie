# Oceanographie
Ce projet consiste en une analyse de données océanographiques à l'aide de techniques de machine learning pour prédire la température de l'eau (`T_degC`) en fonction de diverses caractéristiques mesurées. Voici les étapes principales du projet :

1. **Importation des bibliothèques** : Les bibliothèques nécessaires pour le traitement des données, la visualisation et les modèles de machine learning sont importées, notamment `pandas`, `numpy`, `matplotlib`, `scikit-learn`, etc.

2. **Chargement des données** : Les données sont chargées à partir d'un fichier CSV nommé `bottle.csv`. Le fichier contient des données océanographiques, mais certaines colonnes ont des types de données mixtes, ce qui génère un avertissement.

3. **Prétraitement des données** :
   - Les colonnes avec trop de valeurs manquantes sont supprimées (colonnes avec moins de 50 000 valeurs non manquantes).
   - Les colonnes `Depth_ID` et `Sta_ID` sont supprimées car elles ne sont pas nécessaires pour l'analyse.
   - Les valeurs manquantes sont remplacées par 0.0.

4. **Séparation des données** :
   - La variable cible `T_degC` (température en degrés Celsius) est séparée des autres caractéristiques.
   - Les données sont divisées en ensembles d'entraînement, de validation et de test.

5. **Normalisation des caractéristiques** : Les caractéristiques sont normalisées à l'aide de `StandardScaler` pour améliorer les performances des modèles de machine learning.

6. **Modélisation et évaluation** :
   - **Régression linéaire** : Un modèle de régression linéaire est entraîné et évalué sur l'ensemble de validation. Les métriques d'évaluation (MSE, MAE, R²) sont calculées.
   - **Validation croisée** : Une validation croisée est effectuée pour évaluer la robustesse du modèle de régression linéaire.
   - **K-Nearest Neighbors (KNN)** : Un modèle KNN est entraîné et évalué sur l'ensemble de test. Les métriques d'évaluation sont calculées et une validation croisée est également effectuée.
   - **Forêt aléatoire** : Un modèle de forêt aléatoire est entraîné et évalué sur l'ensemble de test. Les métriques d'évaluation sont calculées et une validation croisée est également effectuée.

7. **Résultats** : Les performances des différents modèles sont comparées en fonction des métriques d'évaluation (MSE, MAE, R²). Le modèle de forêt aléatoire semble offrir les meilleures performances avec un R² très proche de 1 et un MSE très faible.

En résumé, ce projet vise à prédire la température de l'eau à partir de données océanographiques en utilisant plusieurs modèles de machine learning, et à évaluer leurs performances respectives.

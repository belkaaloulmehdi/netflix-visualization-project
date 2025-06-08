# Rapport d’analyse – Projet Netflix Content Analysis

---

## 1. Contexte du projet

Ce projet vise à analyser le catalogue Netflix afin de mieux comprendre la répartition des genres, la disponibilité des contenus par pays, ainsi que la saisonnalité des ajouts.  
L’outil principal utilisé est Power BI, permettant la création d’un dashboard interactif et visuel.

---

## 2. Description du dataset

- 8 807 titres Netflix (films et séries)  
- Colonnes clés : `type` (Film, Série), `title`, `listed_in` (genres), `country`, `date_added`, `release_year`, `rating`, `duration`  
- Présence de valeurs manquantes dans certaines colonnes (`director`, `cast`, `country`)  
- Données brutes importées au format CSV dans Power BI

---

## 3. Préparation et nettoyage des données dans Power BI

- Import du fichier CSV brut dans Power BI Desktop  
- Conversion de la colonne `date_added` en type Date  
- Création de deux colonnes calculées :  
  - `added_year` = année d’ajout  
  - `added_month` = mois d’ajout  
- Fractionnement de la colonne `listed_in` pour séparer les genres multiples en lignes distinctes (splitting par délimiteur `,` puis en lignes)  
- Fractionnement de la colonne `country` pour gérer les titres disponibles dans plusieurs pays  
- Nettoyage des espaces et valeurs nulles dans les colonnes clés  
- Gestion des décalages de données dus aux retours à la ligne dans le CSV (exemple : correction manuelle dans Power Query)

---

## 4. Visualisations réalisées

### Page 1 – Vue d’ensemble

- **Top Genres (Graphique en barres)** : Visualisation des genres les plus présents dans le catalogue, triés par nombre de titres.  
- **Nombre de pays (Carte KPI)** : Nombre distinct de pays dans lesquels Netflix est disponible.  
- **Pays avec le plus de contenu (Graphique en barres)** : Classement des pays selon le nombre de contenus disponibles.  
- **Proportion Films vs Séries (Graphique circulaire)** : Répartition des types de contenus.

### Page 2 – Genre dominant par pays

- **Heatmap ou Matrice** : Présentation du genre le plus fréquent dans chaque pays, permettant d’identifier les préférences régionales.

### Page 3 – Saisonnière des sorties

- **Graphique en barres groupées ou en ligne** : Nombre de titres ajoutés par mois, avec distinction par année (`added_year` et `added_month`) pour détecter les tendances saisonnières.

### Pages Bonus

- **Classification par type de contenu (Graphique en barres empilées)** : Comparaison des films et séries selon les genres, montrant les dominances par catégorie.  
- **Répartition géographique (Carte Bing)** : Visualisation interactive montrant la distribution des contenus Netflix par pays et leur volume.  
- **Évolution des ajouts par pays et année (Graphique en ligne)** : Analyse temporelle des volumes de contenus ajoutés par pays, mettant en lumière les tendances et pics d’activité.

---

## 5. Insights clés

- Les genres « Drame », « Comédie » et « Documentaire » dominent largement le catalogue Netflix.  
- Netflix est disponible dans plus de 70 pays, avec une forte concentration de contenus aux États-Unis.  
- Les préférences de genre varient nettement selon les régions, ce qui est exploitable pour la stratégie locale.  
- Les ajouts de contenus suivent des schémas saisonniers avec des pics identifiables.  
- Les analyses bonus apportent une compréhension approfondie de la typologie des contenus et de leur dynamique géographique.

---

## 6. Branding Netflix et design

- Utilisation des couleurs officielles : rouge (#E50914) et noir pour respecter l’identité visuelle Netflix.  
- Intégration du logo Netflix dans le dashboard.  
- Choix de polices simples et lisibles (Segoe UI, Arial).  
- Mise en place de filtres et segments interactifs pour une expérience utilisateur fluide.

---

## 7. Navigation et recommandations

- Utiliser les segments (slicers) pour filtrer par genre, pays, année ou rating.  
- Explorer les heatmaps pour comprendre les dynamiques par pays et genre.  
- Visualiser la saisonnalité pour planifier les sorties et stratégies marketing.

---

## 8. Conclusion

Ce projet illustre une exploitation complète des données Netflix avec Power BI, alliant nettoyage des données, visualisations avancées et analyses stratégiques.  
Il démontre la capacité à transformer un dataset complexe en insights business actionnables.

---

*Fin du rapport*
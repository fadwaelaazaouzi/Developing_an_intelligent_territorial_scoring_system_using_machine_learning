# FEVI — Vulnérabilité économique des femmes (RGPH 2024)

Analyse multi-niveaux du RGPH 2024 pour caractériser et prédire la vulnérabilité économique des femmes au Maroc.
Le projet est structuré en 4 notebooks, du chargement des données à la modélisation prédictive et au suivi expérimental.

## Contenu

- `01_Data_Loading_and_Cleaning.ipynb` — Chargement des Excel RGPH, harmonisation, fusion et nettoyage des données. Production du dataset consolidé `df_final_dataset.csv`.
- `02_eda_regional.ipynb` — Analyse exploratoire régionale (statistiques, CV, corrélations) et construction de scores composites par ACP.
- `03_fevi_target_and_communal_features.ipynb` — Construction de l'indice FEVI au niveau communal (ACP), distribution et préparation des variables explicatives.
- `04_modeling_with_prediction.ipynb` — Régression linéaire vs Forêt aléatoire (split 80/20), importance des variables, clustering KMeans et suivi MLflow.

## Données attendues

Placez les fichiers sources dans un dossier `data/` (ou adaptez les chemins dans les notebooks) :
- `data/Indicateurs_demographiques_socioeconomiques_RGPH_2024.xlsx` (nom indicatif)
- `data/codegeographique.xlsx`

Les notebooks produisent :
- `outputs/df_final_dataset.csv`
- Figures dans `outputs/figures/` (cartes, heatmaps, distributions, feature importances, etc.)

Créez les dossiers au besoin :
```bash
mkdir -p data outputs/figures

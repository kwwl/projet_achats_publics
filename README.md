# Projet Achats Publics - Analyse DECP

![Python](https://img.shields.io/badge/python-3.11-blue) ![Pandas](https://img.shields.io/badge/pandas-1.6-green) ![Seaborn](https://img.shields.io/badge/seaborn-0.12-orange) 

## Description

Ce projet vise à analyser les **marchés publics français** à partir du dataset **DECP 2022**. L'objectif est de produire des **KPIs financiers et qualitatifs**, des visualisations, et des insights pour identifier les tendances des marchés publics, les principaux acheteurs et les secteurs les plus actifs.

Le projet comprend :
- Nettoyage et préparation des données
- Transformation des identifiants SIRET en SIREN
- Sélection des colonnes pertinentes
- Analyse financière et qualitative
- Mini-dashboard visuel avec des graphiques
- Analyse temporelle et par secteur (Code CPV)

---

## Dataset

Le dataset utilisé est : `decp-2022-marches-valides.csv` (DECP 2022). https://drive.google.com/file/d/1oJuOt5KtBZ2Pkdhw_jXzTA2RJehB9e5j/view?usp=drive_link  
- Format CSV, séparateur `;`
- 358 017 lignes et 56 colonnes
- Colonnes clés : `acheteur_id`, `titulaire_id`, `montant`, `dureeMois`, `dateNotification`, `procedure`, `codeCPV`, `objet`, `marcheInnovant`, `considerationsSociales`, `considerationsEnvironnementales`

---

## Installation

1. Cloner le repository :
```bash
git clone https://github.com/kwwl/projet_achats_publics.git
cd projet_achats_publics
Créer un environnement virtuel et l’activer :

bash
Copier le code
python -m venv venv
source venv/bin/activate  # macOS / Linux
venv\Scripts\activate     # Windows
Installer les dépendances :

bash
Copier le code
pip install -r requirements.txt
Utilisation
Importer les bibliothèques et charger le dataset :

python
Copier le code
import pandas as pd

decp = pd.read_csv("data/raw/decp-2022-marches-valides.csv", sep=";", low_memory=False, on_bad_lines='skip')
Nettoyage et préparation des données :

Transformation des identifiants SIRET en SIREN

Sélection des colonnes pertinentes

Conversion de dateNotification en datetime

Calcul des KPIs :

Montant total par acheteur

Nombre de marchés par type de procédure

Durée moyenne des marchés

Proportion de marchés innovants, sociaux et environnementaux

Top 10 secteurs par Code CPV

Visualisations (mini-dashboard) :

Barplots pour top acheteurs et top secteurs

Graphiques temporels (évolution par année)

KPIs qualitatifs par année

Distribution de la durée des marchés

Résultats principaux
Top acheteurs par montant : identification des principaux acteurs des marchés publics

Top secteurs (Code CPV) : identification des secteurs les plus actifs et lucratifs

Analyse temporelle : suivi des montants et du nombre de marchés par année

KPIs qualitatifs : proportion de marchés innovants, sociaux et environnementaux

Technologies utilisées
Python 3.11

Pandas : manipulation et nettoyage de données

Matplotlib & Seaborn : visualisation des données

Jupyter Notebook : environnement d’analyse

Structure du projet
bash
Copier le code
projet_achats_publics/
│
├─ data/
│  └─ raw/decp-2022-marches-valides.csv
│
├─ notebooks/
│  └─ analyse_decp.ipynb
│
├─ src/
│  └─ data_cleaning.py
│
├─ requirements.txt
└─ README.md
Auteur
Kemil Lamouri
Data Analyst / Future Data Scientist
GitHub

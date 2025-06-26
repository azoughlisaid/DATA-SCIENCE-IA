# DATA-SCIENCE-IA
En parallèle de mes missions d’Analyste de données achats, je mène actuellement un projet IA visant à prédire d’abord les indices des matières premières, puis les prix des matériaux de construction à un an.
Il s’appuie sur nos historiques internes et ces indices pour alimenter le processus achats, aider à négocier avec les fournisseurs sur des bases chiffrées et accélérer les décisions.

Principales responsabilités & technologies : 

🗄️ ETL & centralisation : extraction depuis SharePoint et/ou SAP ERP internes.

🧹 Préparation des données : nettoyage, imputation et enrichissement via Python & Excel

🤖 Modélisation : conception et entraînement de XGBoost (multivarié) et SARIMA (univarié)

🚀 Déploiement : API Flask/FastAPI pour le scoring et application Streamlit pour l’exploration

📊 Visualisation : tableau de bord final sous PowerBI

🔍 Interprétabilité & suivi : rapports SHAP et tracking des expériences avec MLflow.

              [Données historiques]
          (indices matières + prix ERP)
                     │
                     ▼
         [Modèle LSTM pour chaque matière]
      (Prévision des indices mensuels 2026)
                     │
                     ▼
     [Calcul des indices pondérés par article]
     (pondération selon la composition article)
                     │
                     ▼
    [Construction du jeu de données tabulaire]
  (prix 2022–2025, fournisseur, région, indice)
                     │
                     ▼
     [Modèle XGBoost (entraînement sur 2022–2024)]
     (validation sur 2025, tuning, MAE < 2 €)
                     │
                     ▼
         [Prédiction des prix unitaires 2026]
                     │
                     ▼
   [Intégration dans Power BI – tableaux de bord]
(filtres dynamiques, alertes, visualisation achat)

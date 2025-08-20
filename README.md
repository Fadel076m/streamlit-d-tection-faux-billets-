# Détection des Faux Billets - Interface Streamlit

Cette application Streamlit permet d'analyser des fichiers CSV contenant les caractéristiques géométriques des billets pour détecter les faux billets à l'aide d'un modèle de machine learning.

## Fonctionnalités

- **Upload de fichiers CSV** : Interface intuitive pour charger les données
- **Validation des données** : Vérification automatique du format et des colonnes
- **Prédictions ML** : Envoi des données à une API FastAPI pour analyse
- **Visualisations interactives** : Graphiques et statistiques détaillées
- **Export des résultats** : Téléchargement des prédictions au format CSV

## Format des données requis

Le fichier CSV doit contenir les colonnes suivantes :
- `diagonal` : Mesure diagonale du billet
- `height_left` : Hauteur du côté gauche
- `height_right` : Hauteur du côté droit
- `margin_low` : Marge inférieure
- `margin_up` : Marge supérieure
- `length` : Longueur du billet

## Installation

1. Installer les dépendances :
```bash
pip install -r requirements.txt
```

2. Lancer l'application :
```bash
streamlit run app.py
```

## Configuration

- **URL de l'API** : Configurable via la sidebar (par défaut : http://127.0.0.1:8000)
- L'API FastAPI doit être en cours d'exécution avec un endpoint `/predict-file`

## Déploiement

Cette application est prête pour le déploiement sur Streamlit Cloud.

## Technologies utilisées

- **Streamlit** : Interface utilisateur
- **Pandas** : Manipulation des données
- **Plotly** : Visualisations interactives
- **Requests** : Communication avec l'API
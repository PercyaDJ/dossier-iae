# Big Data – M2 CMSI

Ce dépôt contient les travaux réalisés dans le cadre du module Big Data du Master 2 CMSI. Il regroupe deux projets distincts d'analyse de données sur le marché Airbnb, allant de l'exploration (EDA) à la modélisation.

## 📌 Organisation du dépôt

*   **`oslo_airbnb_EDA.ipynb`** : Projet de groupe (Oslo) – EDA & Régression.
*   **`amsterdam_airbnb_EDA.ipynb`** : Projet individuel (Amsterdam) – EDA approfondie.
*   **`listings-oslo.csv`** : Dataset brut pour Oslo.
*   **`listings-amsterdam.csv`** : Dataset brut pour Amsterdam.
*   **`interaction_IA.md`** : Journal complet des échanges avec l'assistant IA (prompts, itérations, corrections).

---

## 🚀 Ouvrir dans Google Colab

| Projet | Lien |
| :--- | :--- |
| **Oslo (Groupe)** | <a href="https://colab.research.google.com/github/PercyaDJ/dossier-iae/blob/main/oslo_airbnb_EDA.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |
| **Amsterdam (Individuel)** | <a href="https://colab.research.google.com/github/PercyaDJ/dossier-iae/blob/main/amsterdam_airbnb_EDA.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> |

---

## 👥 1. Projet de groupe : Oslo

### Objectifs
L'objectif de ce projet est d'analyser le marché Airbnb à Oslo pour comprendre la formation des prix et la structure de l'offre. Il répond aux questions clés du cahier des charges : distribution des prix, identification des quartiers valorisés, rôle des "Superhosts" et des professionnels.

### Analyse Exploratoire (EDA)
*   **Marché concentré** : L'offre est majoritairement constituée de logements entiers et se concentre dans quelques quartiers centraux.
*   **Prix** : Forte disparité selon les quartiers (Centre vs Périphérie) et le type de logement.
*   **Professionnalisation** : Présence significative d'hôtes multi-listings (investisseurs ou agences).

### Modélisation (Régression Linéaire)
Une régression linéaire a été mise en œuvre pour expliquer le prix des nuitées.
*   **Performance** : Le modèle obtient un **R² d'environ 0.18**.
*   **Limites** : Ce score modéré indique que le prix dépend de nombreux facteurs non présents dans le jeu de données simplifié (surface, standing, équipements, étage...).
*   **Insights Business** :
    *   Le *Room Type* est le déterminant majeur (logement entier >> chambre privée).
    *   La localisation (quartier) joue un rôle clé mais secondaire par rapport au type de bien.
    *   Les contraintes (durée minimum) et le volume d'avis tendent à être corrélés à des prix légèrement inférieurs (stratégie de volume).

---

## 👤 2. Projet individuel : Amsterdam

### Objectifs
Ce projet individuel applique la méthodologie d'analyse exploratoire au marché d'Amsterdam, avec une attention particulière à la segmentation et aux spécificités locales.

### Analyses clés
*   **EDA** : Analyse de la distribution des prix, cartographie des quartiers les plus chers, et étude de la disponibilité.
*   **Comparaison** : Mise en évidence des différences structurelles avec Oslo (tourisme plus intense, saturation potentielle).
*   **Choix méthodologique** : Contrairement au projet de groupe, **aucune régression n'a été effectuée** ici, conformément au cahier des charges qui réservait la modélisation complexe au travail d'équipe.
*   **Insights** : Identification de segments "Luxe" vs "Budget" très marqués géographiquement.

---

## 🤖 Interactions IA

Le fichier **`interaction_IA.md`** documente la collaboration avec l'assistant IA. Il contient :
*   Les **prompts** structurants (rôle, contexte, contraintes).
*   Les **itérations** pour affiner le nettoyage des données et les choix méthodologiques (gestion des outliers, définition des seuils).
*   La **critique** des résultats par l'IA (limites, biais).

Ce fichier témoigne de la démarche de *Prompt Engineering* et de la réflexivité demandée dans l'évaluation.

---

## ⚙️ Exécution locale

Pour exécuter les notebooks localement, installez les dépendances suivantes :

```bash
pip install pandas numpy seaborn matplotlib scikit-learn
jupyter notebook
```

## 📋 Critères d’évaluation

Ce dépôt reflète les compétences évaluées :
*   **Prompt Engineering** : Qualité et structure des demandes à l'IA.
*   **Analyse critique** : Capacité à questionner les données et les résultats (limites, biais).
*   **Qualité analytique** : Rigueur du code, pertinence des visualisations et clarté des interprétations.
*   **Intégrité** : Le projet est livré tel quel, sans modification artificielle des résultats générés par l'IA.

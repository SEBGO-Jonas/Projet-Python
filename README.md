# 📊 Projet Python — Analyse de données de ventes

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-DataFrame-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualisation-11557C)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualisation-4c72b0)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)

Ce dépôt regroupe deux mini-projets Python réalisés dans le cadre d'une formation **Data Analyst**. Les deux notebooks exploitent des jeux de données de ventes en magasin pour illustrer un pipeline complet : chargement, nettoyage, agrégation, visualisation et export des résultats.

## 📁 Contenu du dépôt

| Fichier | Description |
|---|---|
| [`Mini Projet Finalisé 1.ipynb`](./Mini%20Projet%20Finalis%C3%A9%201.ipynb) | Exploration et nettoyage d'un jeu de données de ventes, calculs dérivés, analyses par magasin/produit/catégorie, visualisations et export automatique en rapport Word (`.docx`). |
| [`Etude de cas.ipynb`](./Etude%20de%20cas.ipynb) | Étude de cas orientée visualisation : évolution des revenus mensuels, comparaison des performances par catégorie et heatmap croisée catégorie/mois. |
| `README.md` | Ce fichier. |

---

## 1️⃣ Mini Projet Finalisé — Analyse des ventes en magasin

**Objectif :** partir d'un fichier CSV brut de ventes et produire une analyse complète, du nettoyage des données jusqu'à un rapport Word illustré.

**Étapes couvertes :**
- Chargement du CSV et exploration initiale (`shape`, `info`, `columns`)
- Création de colonnes calculées : `Total_Vente` (Prix × Quantité), `Prix_net` (après remise)
- Traitement des valeurs manquantes (remplacement par 0 puis par la moyenne)
- Export des données nettoyées vers Excel (`Ventes_magasin.xlsx`)
- Analyses agrégées : magasin le plus performant, chiffre d'affaires par magasin, produit le plus vendu par ville
- `groupby` avancé : moyenne des prix par catégorie, ventes par mois, volumes par produit
- Visualisations : diagrammes en barres (verticaux/horizontaux), diagramme circulaire (top 5 produits), répartition par mois
- Génération automatique d'un rapport **Word** (`Analyse_Graphique_Ventes.docx`) intégrant graphiques et commentaires via `python-docx`

**Bibliothèques utilisées :** `pandas`, `numpy`, `matplotlib`, `seaborn`, `python-docx`, `openpyxl`

---

## 2️⃣ Étude de cas — Visualisation des ventes

**Objectif :** illustrer des techniques de visualisation de données sur un second jeu de ventes.

**Étapes couvertes :**
- Chargement et aperçu du jeu de données
- Conversion et agrégation temporelle (revenus mensuels)
- Courbe d'évolution des revenus mensuels (`sns.lineplot`)
- Comparaison des revenus par catégorie de produits (`sns.barplot`)
- Heatmap croisée Catégorie × Mois (`sns.heatmap`)

**Bibliothèques utilisées :** `pandas`, `matplotlib`, `seaborn`

---

## 🛠️ Installation

```bash
git clone https://github.com/<votre-utilisateur>/Projet-Python.git
cd Projet-Python
pip install pandas numpy matplotlib seaborn python-docx openpyxl jupyter
```

## ▶️ Utilisation

```bash
jupyter notebook
```

Ouvrez ensuite le notebook souhaité (`Mini Projet Finalisé 1.ipynb` ou `Etude de cas.ipynb`) et exécutez les cellules dans l'ordre.

> ⚠️ **Données requises** : les notebooks pointent actuellement vers des chemins locaux (`C:/Users/HP/Desktop/...`) et vers des fichiers CSV qui ne sont pas inclus dans ce dépôt. Pour reproduire l'analyse, placez vos propres fichiers `ventes_magasin.csv` / `visualisation_ventes_magasin.csv` dans le dossier du projet et mettez à jour le chemin dans la cellule de chargement (`pd.read_csv(...)`).

## 🧰 Technologies

- **Python 3**
- **Pandas** — manipulation et agrégation de données
- **Matplotlib / Seaborn** — visualisation de données
- **python-docx** — génération de rapports Word
- **openpyxl** — export Excel
- **Jupyter Notebook** — environnement d'exécution

## 📄 Licence

Projet personnel réalisé à des fins d'apprentissage (Data Analyst).

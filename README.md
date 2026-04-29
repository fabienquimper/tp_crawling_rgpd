# TP — Ingénierie des données : conformité, scraping responsable & audit qualité

**Public :** Chefs de projet IA | **Durée :** ~3h45 | **Niveau :** Débutant/Intermédiaire

---

## Structure du TP

| Notebook | Phase | Durée | Objectif |
|---|---|---|---|
| `01_compliance.ipynb` | Conformité | 30 min | Analyser les robots.txt et évaluer les risques juridiques |
| `02_collecte.ipynb` | Collecte | 1h15 | Scraper de façon responsable et exporter un CSV |
| `03_audit.ipynb` | Audit qualité | 1h15 | Mesurer la qualité du dataset sur 6 dimensions |
| `04_synthese.ipynb` | Synthèse | 45 min | Rédiger une note de chef de projet (Go/No-go) |

> **Dataset de secours :** Si vous êtes bloqué au bout de 45 min sur la phase collecte, utilisez `data/dataset_secours.csv` et passez directement au notebook `03_audit.ipynb`.

---

## Installation (5 min)

### Option A — En local (Jupyter)

**Prérequis :** Python 3.10 ou 3.11 installé sur votre machine.

```bash
# 1. Cloner ou télécharger ce dossier, puis se placer dedans
cd tp_web_scraping

# 2. Créer un environnement virtuel (recommandé)
python -m venv .venv

# Sur Windows :
.venv\Scripts\activate

# Sur Mac/Linux :
source .venv/bin/activate

# 3. Installer les dépendances
pip install -r requirements.txt

# 4. Lancer Jupyter
jupyter notebook
```

Ouvrez ensuite les notebooks dans l'ordre : `01_compliance.ipynb`, puis `02_collecte.ipynb`, etc.

---

### Option B — Google Colab (aucune installation)

1. Aller sur [colab.research.google.com](https://colab.research.google.com)
2. `Fichier` → `Ouvrir un notebook` → `GitHub` ou uploader le fichier `.ipynb`
3. Dans la première cellule du notebook, les packages s'installent automatiquement (cellule `# COLAB`).

---

## Livrables attendus

- `export.csv` — votre dataset collecté (ou le dataset de secours annoté)
- `rapport_audit.html` — rapport ydata-profiling (généré par le notebook 03)
- `04_synthese.ipynb` complété — votre note de chef de projet

---

## En cas de problème

| Problème | Solution |
|---|---|
| `ModuleNotFoundError` | Relancer `pip install -r requirements.txt` dans le bon environnement |
| Le site bloque le scraping | Passez au dataset de secours `data/dataset_secours.csv` |
| `ydata-profiling` trop lent | Utilisez `minimal=True` dans le notebook 03 |
| Jupyter ne démarre pas | Essayez `jupyter lab` à la place, ou Google Colab |

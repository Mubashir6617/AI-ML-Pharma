# AI, Machine Learning & Python for Pharmaceutical Sciences

A beginner-friendly Jupyter notebook that introduces Python fundamentals, a small drug-activity classification workflow, dose-response curves, and model comparison. It is designed for teaching and self-study—not for scientific, clinical, or regulatory decision-making.

## What you will learn

- Python variables, lists, dictionaries, functions, loops, and conditions
- How to load and inspect a small compound dataset with pandas
- The standard machine-learning flow: features, train/test split, training, evaluation, and prediction
- How to plot Hill-equation dose-response curves
- Why tiny teaching datasets cannot validate a production model

## Repository layout

```text
.
├── data/raw/compound_activity.csv  # Small tracked teaching dataset
├── notebooks/ai_ml_pharma.ipynb     # Refactored tutorial notebook
├── src/                                 # Reusable Python modules as the project grows
├── tests/                               # Automated tests for reusable code
├── requirements.txt                     # Notebook dependencies
├── pyproject.toml                       # Project metadata and test configuration
└── .gitignore                           # Files that should stay local
```

## Quick start

Use Python 3.10 or newer. From the repository root:

```bash
python -m venv .venv
```

Activate the environment:

```bash
# Windows PowerShell
.venv\Scripts\Activate.ps1

# macOS/Linux
source .venv/bin/activate
```

Install dependencies and open JupyterLab:

```bash
pip install -r requirements.txt
jupyter lab
```

Open `notebooks/ai_ml_pharma.ipynb` and run cells from top to bottom. Start JupyterLab from the repository root so the notebook can find `data/raw/compound_activity_demo.csv`.

## Reproducibility

The notebook fixes its random seed at `42`, reads a version-controlled CSV, and validates required columns before training. It is intentionally small so that beginners can inspect every step. The resulting metrics are illustrative only and should not be interpreted as predictive performance for real drug discovery.

## Growing this project

When the notebook develops reusable functions, move them to `src/` and add tests in `tests/`. Keep raw source data in `data/raw/`, derived data in ignored `data/processed/`, and large trained models in ignored `models/` or an external artifact store. Add a license before accepting contributions or distributing the project.

## License

Choose and add a license appropriate for your intended use (MIT is a common permissive choice). Do not add a license file until you have decided the legal terms you want to grant.

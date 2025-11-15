# DS223 Homework 3 – Survival Analysis

Quick repo for the churn-survival assignment.

## What’s here
- `marketing_hw3_survival.ipynb`: the whole workflow—data prep, AFT fit/compare (Weibull, Log-Logistic, Log-Normal), significant-feature refit, CLV + segment analysis, retention budget, and the short write-up.
- `telco.csv`: data used in the notebook.
- `requirements.txt`: exact package versions.
- `Homework-3-Survival-Analysis.pdf`: assignment pdf for reference.

## How to run it
```bash
pip install -r requirements.txt
jupyter notebook
```
Open the notebook and “Restart & Run All”. The current `lifelines` release (0.30) only exposes those three AFT fitters, so that’s what I compare.

## Extra notes
- CLV is computed with a $1 monthly margin, 60‑month horizon, 10% annual discount.
- Retention budget = 15% of the CLV tied to subscribers with >50% churn odds inside 12 months.
- If `lifelines` adds more AFT models in the future, just drop them into the `aft_models` dict and re-run.


# Credit Risk Prediction System

> End-to-end machine learning system that predicts loan default risk, with a focus on handling class imbalance, model interpretability, and production deployment.

**Status:** 🚧 In Progress (Started: June 2026)

---

## Problem Statement

Lenders need to estimate the probability that a loan applicant will default *before* approving the loan. Misjudging this risk is costly in both directions: approving a loan that defaults causes direct financial loss, while rejecting a creditworthy applicant means lost revenue and a missed customer.

This project builds a supervised classification system that predicts loan default probability from applicant and loan data, and wraps it in a deployable API with an interpretable risk-scoring interface — similar to systems used in real fintech credit underwriting.

## Why This Project

Most tutorial-level classification projects stop at "train a model, report accuracy." Real credit risk modeling requires going further:

- **Severe class imbalance** (most loans don't default) — accuracy is a misleading metric here
- **Regulatory-grade interpretability** — credit decisions legally require explanations, so black-box predictions aren't enough
- **Business-aware evaluation** — the cost of a false negative (approving a bad loan) is very different from a false positive (rejecting a good applicant), so the right threshold isn't 0.5

This project is built to learn and demonstrate the *full* applied ML workflow, not just model fitting.

## Dataset

[Lending Club Loan Data](https://www.kaggle.com/datasets/wordsforthewise/lending-club) (Kaggle) — historical loan-level data from a real peer-to-peer lending platform, including applicant financials, loan terms, and final loan status (fully paid vs. charged off/default).

*(Update this section once you've finalized which dataset version/subset you're using.)*

## Project Plan

| Phase | Focus | Status |
|---|---|---|
| 1. EDA & Feature Engineering | Understand data, handle missingness, engineer features (DTI, credit utilization, etc.) | 🔲 Not started |
| 2. Baseline & Model Building | Logistic Regression baseline → Random Forest → XGBoost/LightGBM | 🔲 Not started |
| 3. Imbalance Handling & Tuning | SMOTE, class weighting, threshold tuning, Optuna hyperparameter search | 🔲 Not started |
| 4. Evaluation & Interpretability | ROC-AUC, PR-AUC, calibration, SHAP explanations | 🔲 Not started |
| 5. API & Frontend | FastAPI scoring endpoint + Streamlit demo UI | 🔲 Not started |
| 6. MLOps | MLflow experiment tracking, GitHub Actions CI | 🔲 Not started |
| 7. Documentation | Final write-up, architecture diagram, results | 🔲 Not started |

*(Tick these off as you finish each phase — this table is the first thing recruiters will scan.)*

## Tech Stack

- **Language:** Python 3.11
- **Data & ML:** pandas, NumPy, scikit-learn, XGBoost, LightGBM, imbalanced-learn
- **Tuning:** Optuna
- **Interpretability:** SHAP
- **Experiment Tracking:** MLflow
- **API:** FastAPI + Uvicorn
- **Frontend:** Streamlit
- **CI/CD:** GitHub Actions
- **Deployment:** Render / Railway *(TBD)*

## Project Structure

```
credit-risk-prediction/
├── data/
│   ├── raw/              # Original, unmodified dataset
│   └── processed/        # Cleaned, feature-engineered data
├── notebooks/            # Exploratory analysis & experimentation
├── src/
│   ├── data/              # Data loading & cleaning scripts
│   ├── features/          # Feature engineering pipeline
│   ├── models/             # Training, tuning, evaluation scripts
│   └── api/                # FastAPI app for serving predictions
├── tests/                # Unit tests
├── .github/workflows/     # CI pipeline
├── requirements.txt
└── README.md
```

## Setup & Installation

```bash
# Clone the repository
git clone https://github.com/<your-username>/credit-risk-prediction.git
cd credit-risk-prediction

# Create and activate a virtual environment
python -m venv venv
source venv/bin/activate      # Mac/Linux
venv\Scripts\activate         # Windows

# Install dependencies
pip install -r requirements.txt
```


## Author

**Abdul Basit** [LinkedIn](#) · [GitHub](#)

## License

This project is licensed under the MIT License.
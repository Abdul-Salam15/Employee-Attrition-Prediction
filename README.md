# Employee Attrition Prediction

Predicting employee attrition using exploratory data analysis and a baseline machine learning model built in Jupyter.

## Why this project?

Employee attrition can increase hiring/training costs and affect team productivity. This project analyzes HR records to identify patterns linked to attrition and trains a aseline classifier that predicts whether an employee is likely to leave.

## Project at a Glance

- **Goal:** Binary classification of employee attrition (`Yes` / `No`).
- **Dataset:** `Employee Attrition Prediction/Employee-Attrition.csv`
- **Main notebook:** `Employee Attrition Prediction/Employee_Attrition.ipynb`
- **Baseline model:** Logistic Regression
- **Imbalance strategy:** Random oversampling (`RandomOverSampler`)

## Repository Structure

```text
.
├── README.md
└── Employee Attrition Prediction/
    ├── Employee-Attrition.csv
    └── Employee_Attrition.ipynb
```

## Workflow

The notebook follows this flow:

1. **Load and inspect data**
   - Uses `head()`, `info()`, `describe()`, duplicate checks, and null checks.

2. **Exploratory Data Analysis (EDA)**
   - Visual analysis of attrition by:
     - Department
     - Gender
     - Education Field
     - Business Travel
     - Job Role
     - Age distribution and ordinal satisfaction/performance features

3. **Preprocessing**
   - Converts target `Attrition` from `Yes/No` to `1/0`.
   - Encodes `OverTime` as binary.
   - Label-encodes selected categorical features.
   - Creates `X` and `y` for modeling.

4. **Handle class imbalance**
   - Applies random oversampling before train/test split.
     
5. **Train and evaluate model**
   - Splits data into train/test sets.
   - Trains Logistic Regression.
   - Reports Accuracy, Precision, Recall, and F1-score.
   - Plots confusion matrix and ROC/AUC.

## Baseline Performance

From the current notebook run:

- **Accuracy:** 0.6498
- **Precision:** 63.00%
- **Recall:** 70.49%
- **F1-score:** 66.54%

> Metrics may vary slightly across environments and package versions.

## Tech Stack

- Python
- Jupyter Notebook
- pandas, numpy
- matplotlib, seaborn
- scikit-learn
- imbalanced-learn

## Quick Start

### 1) Clone the repository

```bash
git clone <repo-url>
cd Employee-Attrition-Prediction
```

### 2) Create a virtual environment

```bash
python -m venv .venv
source .venv/bin/activate
# Windows (PowerShell): .venv\Scripts\Activate.ps1
```

### 3) Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn jupyter
```

### 4) Run the notebook

```bash
jupyter notebook "Employee Attrition Prediction/Employee_Attrition.ipynb"
```

Run all cells to reproduce the analysis and model output.

## Recommended Next Improvements

- Compare multiple models (e.g., Random Forest, XGBoost, LightGBM).
- Add cross-validation and hyperparameter tuning.
- Build a reproducible sklearn pipeline for preprocessing + modeling.
- Add feature-importance/explainability (e.g., SHAP).
- Export model and create a simple API or dashboard for inference.



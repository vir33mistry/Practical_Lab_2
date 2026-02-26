# Diabetes Progression Model Comparison (Scikit-Learn)

This repository/notebook builds and compares multiple models to predict **diabetes disease progression one year after baseline** using the **Scikit-Learn Diabetes dataset**.

## Dataset
- Source: `sklearn.datasets.load_diabetes`
- Target (`y`): Disease progression one year after baseline (continuous regression target)

## Models Covered
### Part 2 (Univariate — BMI only)
- Polynomial Regression (degree **0 to 5**) using BMI feature

### Part 3 (Multivariate)
- Polynomial Regression (two choices of degree > 1)
- Decision Trees (two configurations)
- kNN Regression (two configurations)
- Logistic Regression (two configurations) for **binary risk classification** (high-risk vs low-risk derived from target)

## Evaluation Metrics
### Regression
- R² (coefficient of determination)
- MAE (Mean Absolute Error)
- MAPE (Mean Absolute Percentage Error)

### Classification (Logistic Regression section)
- Accuracy, Precision, Recall
- ROC-AUC
- Log Loss
- Confusion Matrix and ROC Curve

## Project Structure
- `Diabetes_Progression_Model_Comparison_Report.ipynb` — main notebook
- `requirements.txt` — Python dependencies
- `README.md` — this file

## Setup Instructions

### 1) Create and activate a virtual environment (recommended)
**Windows (PowerShell):**
```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

**macOS / Linux:**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 2) Install dependencies
```bash
pip install -r requirements.txt
```

### 3) Run the notebook
```bash
jupyter notebook
```
Then open:
- `Diabetes_Progression_Model_Comparison_Report.ipynb`

## Notes / Assumptions
- The Diabetes dataset is pre-cleaned and typically has **no missing values**; the notebook still verifies this.
- Logistic Regression is included as a **classification** exercise by converting the continuous target into a binary “high-risk” label (e.g., based on a threshold like the median). Regression metrics (R²/MAE/MAPE) are not appropriate for classification and are not used in that section.

## Author
Created for an academic lab/report comparing classical ML models on the Diabetes dataset.

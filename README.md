# Practical Lab 2 — Diabetes Progression Risk Prediction (CSCN8010)

## Objective
Build models to predict **diabetes disease progression one year after baseline** using the Scikit-Learn Diabetes dataset.
The model is framed as a **screening-support tool** to help physicians identify higher-risk patients early.

## Dataset
- Source: Scikit-Learn Diabetes dataset
- Size: 442 rows, 10 features, 1 continuous target

## Models Implemented
### Part 2 (Univariate: BMI only)
- Polynomial Regression: degree 0 to 5 (6 models)

### Part 3 (Multivariate)
- 2 Polynomial models (degrees > 1)
- 2 Decision Trees (different `max_depth`)
- 2 kNN Regressors (different `k`, with scaling)
- 2 Logistic Regression models (screening classification: high-risk vs low-risk)

## Metrics
### Regression (required)
- R²
- MAE
- MAPE

### Logistic Regression (screening classification)
- ROC-AUC
- Log-Loss
- Accuracy
- Confusion Matrix  
(Plus a transparent probability→score mapping for optional regression-metric interpretation.)

## Notebook Structure
The notebook follows a clear report format:
1) Problem framing  
2) EDA (stats, histograms, scatter plots, correlation)  
3) Cleaning decision  
4) Train/validation/test split (75/10/15)  
5) Model training + validation selection  
6) Final test evaluation  
7) Failure analysis + limitations + conclusion  

## Setup (Windows PowerShell)
```bash
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
python -m ipykernel install --user --name diabetes-venv --display-name "Python (diabetes-venv)"
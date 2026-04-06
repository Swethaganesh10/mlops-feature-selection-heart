# Lab Assignment 6: Feature Selection on Heart Disease Dataset
**Course:** IE-7374 Machine Learning Operations  
**Dataset:** Heart Disease Dataset (UCI)  
**Original Lab:** Feature Selection (Model_Development/Feature_Selection)

## Modification
The original lab uses the Breast Cancer Dataset. This lab uses the **Heart Disease Dataset** instead — a binary classification problem predicting whether a patient has heart disease (1) or not (0) based on 13 clinical features.

Duplicate rows were removed from the dataset (1025 → 302 rows) to ensure realistic model evaluation.

## Feature Selection Methods Covered
1. **Filter Method** — Correlation with target variable (Pearson)
2. **Filter Method** — Correlation among features (removes redundant features)
3. **Filter Method** — Univariate Selection using SelectKBest (ANOVA F-test, k=10)
4. **Wrapper Method** — Recursive Feature Elimination (RFE, n=8)
5. **Embedded Method** — Feature Importances from RandomForestClassifier
6. **Embedded Method** — L1 Regularization using LinearSVC

## Results Summary
| Method | Accuracy | F1 Score | Feature Count |
|---|---|---|---|
| All features | 0.8689 | 0.8788 | 13 |
| Strong features | 0.8525 | 0.8657 | 9 |
| Subset features | 0.8033 | 0.8286 | 7 |
| F-test | 0.8361 | 0.8485 | 10 |
| RFE | 0.8361 | 0.8485 | 8 |
| Feature Importance | 0.8361 | 0.8485 | 10 |
| L1 Reg | 0.8689 | 0.8788 | 13 |

## Tech Stack
- Python, scikit-learn, pandas, numpy, seaborn, matplotlib

## How to Run
1. Clone the repo
2. Install dependencies: `pip install pandas numpy scikit-learn seaborn matplotlib`
3. Open `feature_selection.ipynb` in Jupyter
4. Run all cells

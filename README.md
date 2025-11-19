Objective
This project aims to build a machine learning model to predict whether a student will pass or fail based on academic and demographic features. The goal is to explore model performance and interpretability using techniques like SHAP and LIME.
Dataset
Source: Student performance dataset (uploaded via HITCAP)

Features: Includes variables such as study time, attendance, parental education, test scores, etc.

Target: Binary classification — Pass or Fail
Methods
Data preprocessing: Handling missing values, encoding categorical variables, feature engineering

Model: Gradient Boosting (XGBoost or LightGBM)

Evaluation: AUC, F1-score, confusion matrix

Interpretability:

SHAP: Global feature importance

LIME: Local explanations for individual predictions
Results
Baseline AUC: 0.XX

Top 5 influential features (from SHAP):

Feature A — positively correlated with passing

Feature B — negatively correlated with passing

Feature C — ...

Feature D — ...

Feature E — ...
Case Analysis
High-risk student: LIME explanation shows low attendance and poor test scores as key factors

Low-risk student: Strong parental support and consistent study time

Borderline case: Mixed signals; SHAP and LIME show conflicting feature impacts
Fairness Check
Evaluated model bias across protected attributes (e.g., gender, socioeconomic status)

No significant disparity found in prediction outcomes
Deliverables
notebook.ipynb: Full code and visualizations

README.md: Project overview and interpretation summary

report.txt: Detailed analysis and fairness discussion

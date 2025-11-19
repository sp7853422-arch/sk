Student Pass/Fail Prediction Report
Project Overview
This project builds a machine learning model to predict student pass/fail outcomes using academic and demographic features. The focus is not only on performance but also on interpretability, using SHAP and LIME to explain predictions and assess fairness.
Model Performance
Model Used: XGBoost (Gradient Boosting)

Baseline Metrics:

AUC: 0.82

F1-score: 0.76

Validation Strategy: Stratified 5-fold cross-validation
Global Interpretability (SHAP)
Using SHAP summary plots, the top 10 features influencing the model were identified. The top 5 are:

Rank	Feature Name	Impact Direction
1	Study Time	↑ More study time → Higher pass probability
2	Absences	↓ More absences → Lower pass probability
3	Parental Education	↑ Higher education → Higher pass probability
4	Test Score	↑ Higher score → Higher pass probability
5	Internet Access	↓ No access → Lower pass probability
These features showed consistent directional influence across the dataset.
Local Interpretability (LIME)
Three individual cases were analyzed using LIME:

High-Risk Student:

Prediction: Fail

Key factors: Low study time, high absences, low test score

SHAP and LIME aligned well
Low-Risk Student:

Prediction: Pass

Key factors: High parental education, consistent attendance, good test scores

SHAP and LIME aligned well

Borderline Case:

Prediction: Uncertain

Conflicting signals: High test score but poor attendance

SHAP showed moderate influence from multiple features; LIME highlighted test score as dominant
Fairness Assessment
Protected attributes (e.g., gender, parental education) were reviewed for bias:

No significant disparity found in prediction outcomes across gender

Slight skew observed in predictions for students with low parental education — flagged for further review
Deliverables Summary
student_pass_fail.ipynb: Full code and visualizations

README.md: Project overview and instructions

report.md: This report

feature_summary.txt: Top 5 SHAP feature definitions

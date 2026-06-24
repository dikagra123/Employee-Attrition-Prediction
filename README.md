Employee Attrition Prediction — IBM HR Analytics

A machine learning project that predicts which employees are likely to leave a company, and translates those findings into actionable HR recommendations.



## What This Project Does

Every company loses employees — but losing the wrong people at the wrong time is expensive. Replacing a single mid-level employee can cost anywhere between 50% and 200% of their annual salary when you factor in hiring, training, and lost productivity.

This project builds a classification system trained on IBM HR data that learns the difference between employees who stayed and employees who left — then uses those patterns to flag at-risk employees before they resign.



 Dataset

IBM HR Analytics Employee Attrition Dataset  
Source: https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset
Size: 1,470 employees | 35 features  
Target column: `Attrition` (Yes / No)

> Download the CSV from Kaggle and place it in the project folder before running the notebook.


 

Tasks Covered

| # | Task |
|---|------|
| 1 | Data loading, shape check, attrition rate, column type breakdown |
| 2 | Null handling, dropping irrelevant columns, encoding, scaling |
| 3 | EDA — attrition by department, role, income, work-life balance, tenure |
| 4 | Train 3 models with class imbalance handling |
| 5 | Evaluate with Precision, Recall, F1, ROC-AUC, Confusion Matrix |
| 6 | 5 charts including ROC curve comparison (bonus) |
| 7 | Business insights and HR recommendations in plain English |



Models Trained

- **Logistic Regression** — baseline, most explainable
- **Random Forest** — ensemble, handles non-linear patterns
- **Gradient Boosting** — typically strongest on tabular data

All three use `class_weight='balanced'` to handle the imbalanced target (only ~16% of employees left).

 Key Findings

- **Overtime** was the single strongest predictor of attrition across all models
- **Sales Representatives** had the highest exit rate (~40%) of any job role
- **First-year employees** account for roughly one-third of all departures — pointing to onboarding gaps, not just salary
- Salary matters, but fixing pay without addressing overtime culture will only delay departures, not prevent them



Libraries Used

| Library | Purpose |
|---------|---------|
| `pandas` | Data loading and cleaning |
| `numpy` | Numeric operations |
| `scikit-learn` | Models, preprocessing, evaluation |
| `matplotlib` | Charts |
| `seaborn` | Styled visualizations |



HR Recommendations (From the Analysis)

1. **Have direct conversations with Sales Representatives** — this role has the highest attrition rate in the dataset and should be the first priority for any retention effort
2. **Introduce a structured 90-day check-in for new hires** — since most early departures happen within the first year, catching dissatisfaction at 90 days gives HR a real window to intervene



Limitations

This model learns from historical data and cannot account for personal life events, leadership changes, or competitor offers. It should be used as an early warning system — a starting point for HR conversations — not as a definitive prediction about any individual employee.



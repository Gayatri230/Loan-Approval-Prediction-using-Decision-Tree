Loan Approval Prediction using Decision Tree
* Problem Statement

Banks receive thousands of loan applications daily. Manually evaluating each application is time-consuming and prone to bias.
The goal of this project is to build a machine learning model that predicts whether a loan will be approved or rejected based on applicant financial and personal details.

This helps banks:

Reduce risk

Automate decision-making

Improve approval accuracy

* Dataset

Name: Loan Approval Dataset

Source: Public loan approval dataset

Target Variable: loan_status

1 → Approved

0 → Rejected

Key Features:

no_of_dependents

education

self_employed

income_annum

loan_amount

loan_term

cibil_score

residential_assets_value

commercial_assets_value

luxury_assets_value

bank_asset_value

* loan_id was removed as it is only an identifier and not useful for prediction.

* Preprocessing

The following preprocessing steps were applied:

Column names cleaned (lowercase, removed spaces)

Categorical variables encoded:

education: Graduate → 1, Not Graduate → 0

self_employed: Yes → 1, No → 0

loan_status: Approved → 1, Rejected → 0

Checked and handled missing values

Dataset split into 80% training and 20% testing

* Model Used

Decision Tree Classifier

Why Decision Tree?

Handles non-linear relationships

Easy to interpret and explain

Very popular in interviews and real-world applications

Model Configuration:

Criterion: gini

Max Depth: 5

Minimum Samples per Leaf: 10

Random State: 42

* Evaluation Metrics

The model was evaluated using:

Accuracy Score

Confusion Matrix

Classification Report (Precision, Recall, F1-Score)

These metrics help understand both overall performance and class-wise predictions.

* Feature Importance

Decision Trees provide built-in feature importance.

Important features influencing loan approval:

CIBIL Score

Annual Income

Loan Amount

Bank Asset Value

Residential Asset Value

This improves model explainability, which is crucial in finance-related applications.

* Results

The model successfully learned meaningful decision rules.

Achieved good accuracy without overfitting.

Predictions are interpretable and aligned with real-world logic.

Example:

Higher income + higher CIBIL score → higher approval probability

Low CIBIL score → high rejection probability

* Conclusion

This project demonstrates:

End-to-end ML workflow

Strong understanding of Decision Trees

Proper preprocessing and feature handling

Explainable AI for financial decision-making

* Future Improvements

Hyperparameter tuning using GridSearchCV

Replace Decision Tree with Random Forest / XGBoost

Deploy model using Flask or FastAPI

Add SHAP for deeper explainability

* Tech Stack

Python

Pandas, NumPy

Scikit-learn

Matplotlib / Seaborn (for visualization)

*Author

Gayatri
Aspiring Data Scientist | ML Enthusiast

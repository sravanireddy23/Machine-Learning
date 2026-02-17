🏦 Loan Default Prediction | Random Forest Classifier










End-to-End Machine Learning project to predict loan repayment behavior using Decision Tree and Random Forest algorithms.

📌 Project Summary

This project builds a classification model to predict whether a borrower will fully repay a loan.

It covers:

Exploratory Data Analysis (EDA)

Feature Engineering

Data Preprocessing

Model Training

Model Evaluation

Algorithm Comparison

The final model helps simulate how financial institutions evaluate credit risk.

🎯 Business Objective

Predict:

not.fully.paid

Value	Meaning
0	Loan Fully Paid
1	Loan Not Fully Paid

This classification helps reduce lending risk and improve credit approval decisions.

📊 Dataset Overview

File: loan_dataset.csv

Features include:

Credit Policy

FICO Score

Interest Rate

Installment Amount

Debt-to-Income Ratio

Revolving Balance

Loan Purpose (Categorical)

Repayment Status (Target)

🔍 Exploratory Data Analysis

Key insights explored through visualizations:

✔ FICO score distribution by credit policy
✔ FICO score distribution by repayment outcome
✔ Loan purpose vs default comparison
✔ Relationship between FICO score & interest rate
✔ Regression trends segmented by policy & repayment

EDA revealed strong relationships between credit score, interest rate, and repayment behavior.

🧹 Data Preparation

Checked data types & missing values

Encoded categorical feature (purpose) using one-hot encoding

Split dataset:

70% Training

30% Testing

Ensured reproducibility with random_state=101

🤖 Models Implemented
🌳 Decision Tree Classifier

Baseline model

Easy to interpret

Higher variance

🌲 Random Forest Classifier

600 trees

Reduced overfitting

Improved generalization

📈 Model Evaluation

Metrics used:

Confusion Matrix

Precision

Recall

F1 Score

Accuracy

🏆 Result

✅ Random Forest outperformed Decision Tree

Reason:

Ensemble averaging

Lower variance

Better performance on unseen data

🛠 Tech Stack
Tool	Purpose
Python	Programming Language
Pandas	Data Analysis
NumPy	Numerical Computation
Matplotlib & Seaborn	Data Visualization
Scikit-Learn	Machine Learning
🚀 How to Run
git clone https://github.com/your-username/loan-default-random-forest.git
cd loan-default-random-forest
python -m venv venv
venv\Scripts\activate   # Windows
pip install -r requirements.txt
python random_forest_project.py

📌 Key Skills Demonstrated

Supervised Machine Learning

Feature Engineering

Model Comparison

Data Visualization

Risk Modeling

Python ML Workflow

End-to-End Project Structuring

🔮 Future Improvements

Hyperparameter tuning (GridSearchCV)

Cross-validation

ROC Curve & AUC analysis

Feature importance visualization

Class imbalance handling

Model deployment (Flask / FastAPI)

👨‍💻 Author

Sravani Reddy Gavinolla
Machine Learning Enthusiast
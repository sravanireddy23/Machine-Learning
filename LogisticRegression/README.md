# 🖱️ Advertising Click Prediction | Logistic Regression  

**End-to-End Machine Learning Project** to predict whether a user clicks on an advertisement based on demographic and behavioral features.  

---

## 📌 Project Summary

This project builds a **binary classification model** to predict ad clicks (`Clicked on Ad`).  

**Includes:**  
- Exploratory Data Analysis (EDA)  
- Data Visualization  
- Feature Selection & Preprocessing  
- Logistic Regression Model Training  
- Model Evaluation  

The final model simulates how digital marketing platforms can target users more effectively.  

---

## 🎯 Business Objective

Predict `Clicked on Ad`:

| Value | Meaning               |
|-------|---------------------|
| 0     | Did Not Click Ad     |
| 1     | Clicked Ad           |

This helps optimize marketing campaigns and improve ad targeting efficiency.  

---

## 📊 Dataset Overview

- **File:** [`advertising.csv`](data/advertising.csv)  
- **External download link:** [Kaggle Dataset](https://www.kaggle.com/datasets/gauthamkadiyala/advertising)  
- **Features include:**  
  - Daily Time Spent on Site (minutes)  
  - Age  
  - Area Income  
  - Daily Internet Usage  
  - Ad Topic Line (text)  
  - City  
  - Male (gender)  
  - Country  
  - Timestamp  
  - Clicked on Ad (target)  

---

## 🔍 Exploratory Data Analysis

Key insights explored through visualizations:

- ✅ Histogram of Age  
- ✅ Area Income vs Age scatterplot  
- ✅ KDE plot of Daily Time Spent on Site vs Age  

**EDA revealed relationships between age, income, time on site, and likelihood of clicking ads.**

---

## 🧹 Data Preparation

- Checked data types & missing values  
- Selected relevant features for modeling (`Daily Time Spent on Site`, `Age`, `Area Income`, `Daily Internet Usage`, `Male`)  
- Split dataset: 70% Training / 30% Testing  
- Ensured reproducibility with `random_state=101`  

---

## 🤖 Model Implemented

### 📈 Logistic Regression
- Binary classifier for click prediction  
- Probabilistic interpretation of predictions  
- Easy to implement and interpret  

**Python Implementation Example:**
```python
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import classification_report, confusion_matrix, accuracy_score

# Features and target
X = ad_data[['Daily Time Spent on Site','Age','Area Income','Daily Internet Usage','Male']]
y = ad_data['Clicked on Ad']

# Split data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=101)

# Train model
logmodel = LogisticRegression()
logmodel.fit(X_train, y_train)

# Predictions
predictions = logmodel.predict(X_test)

# Evaluation
print(confusion_matrix(y_test, predictions))
print(classification_report(y_test, predictions))
print("Accuracy:", accuracy_score(y_test, predictions))

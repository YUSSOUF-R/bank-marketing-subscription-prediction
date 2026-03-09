# Bank Marketing Subscription Prediction

## Project Overview

This project builds a machine learning model to predict whether a bank customer will subscribe to a **term deposit** based on marketing campaign data.

Banks often run telemarketing campaigns to promote financial products. Predicting which customers are more likely to subscribe helps improve campaign efficiency and reduce marketing costs.

---

# Problem Statement

Given customer demographic, financial, and campaign interaction data, build a model to predict:

**Will the customer subscribe to a term deposit?**

Target variable:

```
y → yes / no
```

---

# Dataset Description

The dataset contains information collected during direct marketing campaigns conducted by a Portuguese banking institution.

Features include:

Customer information

* age
* job
* marital status
* education

Financial attributes

* balance
* housing loan
* personal loan

Campaign information

* contact type
* month
* duration
* campaign count

Previous campaign results

* previous contacts
* previous outcomes

Target variable:

```
y → term deposit subscription
```

---

# Project Workflow

## 1 Data Loading

The dataset was loaded using pandas and basic inspection was performed to understand data types and distributions.

---

## 2 Exploratory Data Analysis (EDA)

EDA was performed to understand customer behavior patterns.

Visualizations used:

* Distribution plots
* Count plots
* Correlation analysis
* Target variable distribution

Key observations:

* Most customers did not subscribe to term deposits
* Certain job categories had higher subscription rates
* Campaign duration strongly influenced subscription probability

---

## 3 Data Preprocessing

### Label Encoding

Categorical variables were converted to numerical format using LabelEncoder.

Example:

```
job
marital
education
contact
poutcome
```

---

## 4 Handling Class Imbalance

The dataset contained class imbalance where:

```
No subscription >> Yes subscription
```

To address this problem, **SMOTE (Synthetic Minority Oversampling Technique)** was applied.

This technique generates synthetic samples for the minority class to improve model learning.

---

## 5 Train Test Split

The dataset was split into training and testing sets using:

```
train_test_split()
```

Standardization was applied using **StandardScaler**.

---

# Machine Learning Models

Multiple classification algorithms were implemented and compared.

### Logistic Regression

Baseline linear classification model.

---

### Support Vector Machine (SVM)

Effective for high dimensional classification problems.

---

### K-Nearest Neighbors (KNN)

Distance-based classification algorithm.

---

### Decision Tree

Tree-based model capable of capturing nonlinear relationships.

---

### Random Forest

Ensemble learning method combining multiple decision trees to improve prediction accuracy.

---

### XGBoost

Gradient boosting algorithm that improves performance through sequential tree learning.

---

# Model Evaluation

Models were evaluated using:

* Accuracy Score
* Confusion Matrix
* Classification Report

Metrics used:

```
Precision
Recall
F1-score
```

These metrics help evaluate both overall accuracy and class-specific performance.

---

# Results

Among the tested models:

Random Forest and XGBoost produced the best performance due to their ability to capture nonlinear relationships and handle complex feature interactions.

These models significantly improved prediction accuracy compared to linear models.

---

# Technologies Used

Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
XGBoost
Imbalanced-learn (SMOTE)

---

# Project Structure

bank-marketing-subscription-prediction
│
├── portagese_bank_complete_project.ipynb
├── requirements.txt
├── README.md

---

# Author

Yussouf R
Machine Learning Project

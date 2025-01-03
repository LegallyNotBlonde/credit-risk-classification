# Loan Risk Classification

## Purpose
This analysis aims to develop a machine learning model to predict whether a loan is healthy (Class 0) or risky (Class 1). By identifying high-risk loans, the bank can mitigate credit risk and improve loan approval decisions.
___

## Data Overview
The dataset includes financial variables such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The target variable (loan_status) indicates loan health:

* **Class 0 (Healthy Loans):** 18,759 samples
* **Class 1 (Risky Loans):** 625 samples

**Key Observation:**
The dataset is highly imbalanced, with healthy loans dominating. While desirable for a bank, this imbalance can hinder the model's ability to detect risky loans accurately.
___

## Machine Learning Process
1. **Data Preprocessing:**

* Features (X) and labels (y) were separated.
* Data was split into training and testing sets, stratified to preserve class balance.

2. **Model Training:**

* A Logistic Regression model was implemented using the lbfgs solver.
* The model was trained on the stratified training dataset to ensure consistent results across imbalanced classes.
**
3. **Evaluation:**

* Performance was assessed using a confusion matrix and classification report, providing accuracy, precision, recall, and F1-score metrics.
___

## Results

### Key Metrics:
* **Overall Accuracy:** 99%
* **Precision:**
    * Class 0: 1.00 (Perfect precision)
    * Class 1: 0.87
* **Recall:**
    * Class 0: 1.00 (Perfect recall)
    * Class 1: 0.89
* **F1-Score:**
    * Class 0: 1.00
    * Class 1: 0.88

### Insights:
* The model excels at predicting healthy loans, achieving perfect precision and recall.
* Performance for risky loans is strong but slightly lower due to class imbalance.
___

## Recommendations
To improve the model's ability to predict risky loans:

1. **Oversample Risky Loans:** Increase the number of risky loan samples to balance the dataset.
2. **Adjust Class Weights:** Penalize misclassification of risky loans more heavily.
3. **Precision-Recall Tradeoff:** Focus on improving precision and recall for Class 1 (risky loans), as missing high-risk cases is costlier for the bank.

___

## Summary
The Logistic Regression model performs exceptionally well for healthy loans and reasonably well for risky loans. With targeted improvements, this model can provide reliable predictions, enabling better credit risk management and decision-making.
___

## Repo Structure
Notebook: credit_risk_classification.ipynb
Documentation: README.md (includes analysis summary)
License: Contains the public license information.
___

## Data Reference
This dataset is fictional and is used to showcase my machine learning skills in predicting healthy and risky loans, as well as applying data transformation techniques in a real-world context.
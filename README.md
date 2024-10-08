# Loan Risk Classification

## Overview of the Analysis

### Purpose:
The analysis aims to develop and evaluate a machine learning model that can predict whether a loan is healthy (Class 0) or risky (Class 1). This assists the bank in mitigating credit risk by identifying loans likely to default, improving decision-making in loan approvals or rejections.
___

### Present Data VS Predicted Information:
The data includes financial information such as loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. The target variable (loan_status) indicates whether the loan is healthy (0) or high-risk (1), which the model is designed to predict.
___

### Basic Information About the Predicted Variables:
The target variable, loan_status, is highly imbalanced, with far more healthy loans (Class 0) compared to risky loans (Class 1). While it is very good and desirable for a bank to have the absolute majority of loans be healthy, this imbalance impacts the model's ability to predict the minority class (risky loans). Here's the breakdown:

* Class 0 (healthy loans): 18,759 samples
* Class 1 (risky loans): 625 samples
___

### Stages of the Machine Learning Process:
1. Loading and preprocessing the data by separating the features (X) and labels (y).
2. Splitting the data into training and testing sets using train_test_split, with stratify=y to handle class imbalance.
3. Implementing a **Logistic Regression model** from 'Scikit-Learn', with the 'lbfgs solver' to fit the training data and predict the test data. Logistic Regression is a linear model for binary classification, making it suitable for predicting whether loans are healthy or risky. The random_state was set to 1 for reproducibility, and the model was trained on the training dataset before being evaluated on the test dataset.
4. Evaluating the model's performance using a confusion matrix and classification report to obtain precision, recall, and accuracy metrics.

___

### Results:

<p> Description of Accuracy, Machine Learning Model 1 (Logistic Regression):

* **Accuracy: 99%**
* **Precision:**
<p> - Class 0 (healthy loans): 1.00 (perfect precision)
<p> - Class 1 (risky loans): 0.87

* **Recall:** 
<p> - Class 0 (healthy loans): 1.00 (perfect recall)
<p> - Class 1 (risky loans): 0.89

* **F1-Score:**
<p> - Class 0: 1.00
<p> - Class 1: 0.88

___

### Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* **Which model performs best and how is it known?**
<p> The Logistic Regression model performed exceptionally well in predicting healthy loans, achieving perfect precision and recall (1.00). It also performed reasonably well in predicting risky loans, with a precision of 87% and a recall of 89%. These metrics show that the model effectively identifies both classes, though it is slightly less reliable in predicting high-risk loans.

* **Does performance depend on the problem being solved?**
<p> Yes, performance depends on the problem. In this case, accurately predicting high-risk loans (1's) is more important because failing to identify these loans could result in significant financial losses for the bank. The model does well in identifying risky loans, but there is still room for improvement due to the data imbalance.


* **Recommendation:** 
<p> The Logistic Regression model is a strong candidate for deployment, especially with adjustments to better handle the imbalance. Improvements can be made by oversampling risky loans, adjusting class weights, or focusing more on precision and recall for high-risk loans. These steps will enhance the model's ability to detect risky loans, thus better managing the bank's credit risk.

___

### Repo Structure:
* The Jupyter Notebook with the code, **'credit_risk_classification.ipynb'**, is located in the **'Credit_Risk' folder**.
* The **'Readme.md'** file includes the analysis of loan risks.
The **'License'** file contains the general public license.

___

### Data References:
Data for this dataset was generated by edX Boot Camps LLC, intended for educational purposes only, to demonstrate the ability to transform and analyze data using machine learning techniques.
___
### credit-risk-classification
## Overview of the Analysis
In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:
# Explain the purpose of the analysis.
Purpose of the Analysis: The purpose of this analysis was to develop machine learning models capable of predicting whether a loan is high-risk (1) or healthy (0) based on a set of financial features.
# Explain what financial information the data was on, and what you needed to predict.
The data included various financial attributes of loans such as income, loan amount, loan type, and other relevant features. The target variable was binary: 0 for a healthy loan (i.e., low-risk) and 1 for a high-risk loan. The goal was to predict this target based on the given features.
# Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
The target variable was highly imbalanced, with a larger proportion of healthy loans (0) than high-risk loans (1).
A value count of the target variable (y) might show something like:
0 (Healthy loan): 18,765 instances
1 (High-risk loan): 619 instances
# Describe the stages of the machine learning process you went through as part of this analysis.
Data Preprocessing: We loaded and explored the dataset, ensuring data quality by handling missing values and preparing it for modeling.
Feature Selection: We identified which financial attributes to use as features (X) for predicting the target.
Splitting the Data: We divided the data into training and testing sets to evaluate the model's performance.
Model Selection and Training: We used various machine learning models such as Logistic Regression (for binary classification) to predict the loan risk.
Model Evaluation: After training the model, we evaluated its performance using accuracy, precision, recall, and F1-score to understand how well the model predicted healthy vs. high-risk loans.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).
Logistic Regression: A popular classification algorithm used in binary classification problems. We used this to predict the likelihood of a loan being high-risk or healthy.
## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

Accuracy: 0.99 — The model correctly predicted 99% of the instances, showing its overall effectiveness.

Precision for 0 (Healthy Loan): 1.00 — Perfect precision for predicting healthy loans.

Recall for 0 (Healthy Loan): 0.99 — The model correctly identified 99% of healthy loans.

Precision for 1 (High-Risk Loan): 0.84 — The model predicted 84% of high-risk loans correctly.

Recall for 1 (High-Risk Loan): 0.94 — The model identified 94% of high-risk loans.

F1-score for 0 (Healthy Loan): 1.00 — The model performed flawlessly for healthy loans.

F1-score for 1 (High-Risk Loan): 0.89 — The model performed well for high-risk loans but could improve precision.
## Summary

# Which one seems to perform best? How do you know it performs best?
Best Model: Logistic Regression performed well overall, especially for predicting healthy loans (0). It showed very high precision and recall for class 0, with an accuracy of 99%. For high-risk loans (1), the model performed reasonably well with recall at 94% but slightly lower precision at 84%, indicating room for improvement.

# Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
Performance Considerations:
Predicting Class 1 (High-Risk Loan) is important, especially in financial applications where predicting high-risk loans can help mitigate financial losses. The model does a good job identifying most of the high-risk loans (94% recall), but its precision could be improved to reduce false positives.
Class 0 (Healthy Loan) prediction is easier because of the class imbalance, and the model performs almost perfectly in predicting healthy loans.
If you do not recommend any of the models, please justify your reasoning.
Logistic Regression is recommended for this problem due to its simplicity and excellent overall performance. However, given the class imbalance, further improvements like class balancing, adjusting the decision threshold, or trying other models (like Random Forest or XGBoost) could potentially improve the precision for high-risk loan predictions.
If predicting high-risk loans with higher precision is a priority, further tuning or exploring other models might be necessary to optimize performance for that class.

# Module-20

In this section, we describe the analysis completed for the machine learning models used in this Challenge.

# Explain the purpose of the analysis.
   The purpose of this analysis was to build a predictive model to evaluate the risk level of loans, helping financial institutions distinguish between healthy loans and high risk.

# Explain what financial information the data was on, and what you needed to predict.
  The csv contain financial information in the columns like loan_size', 'interest_rate', 'borrower_income', 'debt_to_income'
  
# Provide basic information about the variables you were trying to predict (e.g., `value_counts`).

loan_status
0    75036
1     2500
  
# Describe the stages of the machine learning process you went through as part of this analysis.
   Identified correlations between features and loan status.
   Used logistic regression.
   Assessed performance using precision, recall, F1 score, and accuracy.
   Examined confusion matrix to analyze misclassifications.
  
# Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).
   Logistic Regression  chosen for its simplicity and effectiveness in binary classification (loan status)

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

# Machine Learning Model 1:
    * Description of Model 1 Accuracy, Precision, and Recall scores.
 
           precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.84      0.94      0.89       619

    accuracy                           0.99     19384
   macro avg       0.92      0.97      0.94     19384
weighted avg       0.99      0.99      0.99     19384

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

  For the 0 that are the (healthy loans ) having 0.99 in recall means that the model identified 99% of all 0 (or healthy loans) , for the 1 that are the (high risk loans) having 0.94 in recall means that the model identified 94% of      all 0 (or high risk loans) also considering that the precision of 84% means that 16% was considered as a false positive and that could mean some healthy loans were classified as high risk instead.

  If minimizing risk is the priority predicting 1 (high risk loans) correctly is more important than perfectly identifying healthy loans. In this case the recall for high risk loans (0.94) is very good, meaning the model identifies      most of them therefore it is recommended depending on the business purpose.


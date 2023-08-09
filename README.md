# credit-risk-classification
## Overview of the Analysis
The purpose of this analysis is to develop a model that assesses the creditworthiness of borrowers using historical lending activity data from a peer-to-peer lending services company. The goal is to create a predictive model that can effectively determine whether a borrower is likely to default on a loan or not. In a nutshell, it builds a predictive model that enhances the lending company's ability to make accurate and consistent loan decisions, ultimately leading to better risk management, improved customer experience, regulatory compliance, and business growth.
The data included various financial features related to borrowers' profiles, credit history, and loan application details. The target variable, loan_status, indicated whether a borrower defaulted on a loan (1) or not (0).

#### Basic Information About the Variables:
The original dataset was imbalanced, with a significant difference in the number of "low-risk" and "high-risk" borrowers. The value_counts of the loan_status variable revealed this imbalance,  with a higher number of 75036 "low-risk" borrowers and 2500 "higher-risk" borrowers.

#### Stages of the Machine Learning Process:
Data Preparation and Splitting: I initially separated the dataset into labels (y) and features (X). The data was then split into training and testing sets using the train_test_split function. The training set was used to train the models, while the testing set was used to evaluate their performance.

Logistic Regression Model: I employed a Logistic Regression model from the sklearn library to predict loan default risk. The model was trained using the training data, and predictions were made on the testing data.

Evaluation and Resampling: To address the class imbalance issue, I utilized the Random Over-Sampling technique from the imblearn library. The training data was resampled to balance the classes before training the model.

## Results
* Machine Learning Model 1 (Original Model):

    * Original Model Accuracy Score: 95% of the predictions were correct.
    * Precision (non-default Class): 100% of the predicted non- default loans were accurate.
    * Precision (default Class): 85% of the predicted loan defaults were accurate.
    * Recall (non-default Class): 99% of the actual non- default loans were correctly identified by the model.
    * Recall (default Class): 91% of the actual loan defaults were correctly identified by the model.

* Machine Learning Model 2 (Resampled Model):

    * Resampled Model Accuracy Score: 99% of the predictions were correct.
    * Precision (non-default Class): 100% of the predicted non- default loans were accurate.
    * Precision (default Class): 84% of the predicted loan defaults were accurate.
    * Recall (non-default Class): 99% of the actual non- default loans were correctly identified by the model.
    * Recall (default Class): 99% of the actual loan defaults were correctly identified by the model.

## Summary
Based on the results obtained, the Resampled Model seems to do better overall because it has a higher score that shows how well it can accurately predict loan defaults and avoid mistakes.

Deciding on Which model is best depends on what the lending company wants to focus on. If they really want to catch as many possible loan defaults as they can, Resampled Model is a good choice. But if they want to make sure they don't mistakenly label too many borrowers as high risk, they might need to work more on Model 1 (Original Model).

It is worthy to note that even though Resampled Model did better, both models need to be monitored over time to make sure they're always working well in the real world.

In a nutshell, both models did well in figuring out who might not repay their loans, with Resampled Model being a bit better. With some more testing and adjustments, these models can be made even better at helping the lending company make safe decisions and avoid financial problems.






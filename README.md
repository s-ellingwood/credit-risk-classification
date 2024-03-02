# credit-risk-classification

Within the Credit_Risk folder is the main file - credit_risk_classification.ipynb (contains all of the code for this challenge) - and the Resources folder which contains the lending_data.csv, from which the data is pulled. The analysis report is below:

# Module 20 Report
## Overview of the Analysis
The purpose of this analysis was to train and evaluate a model based on loan risk using a dataset of historical lending activity from a peer-to-peer lending services company. This model is supposed to identify tehe creditworthiness of borrorwers. The data contains factors such as loan size, inerest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, and total debt. The variables that we try to predict using this model is the loan_status variable, with possible values of 1 - to indicate a loan with a high risk of defaulting - and 0 - to indicate a loan that is healthy.

The data was split into y labels (loan_status) and X features (all other factors listed above). The data was then split using test_train_split and fitted to both a LogisticRegression model using the original data and a LogisticRegression model using resampled training data (sampled using RandomOverSampler from imbalanced-learn).


## Results
Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Accuracy: The balanced_accuracy_score gives us an accuracy score of aorund 0.952 which is quite high, suggesting that the model is almost perfectly accurate and a well suited model from predicting loan status.
  * Precision: The precision is fairly high for predicting both 0s and 1s, however it is higher for 0s with a perfect score of 1.00. The precision score for identifying loan status' of 1 is a bit lower, at only 0.85. This means that it labels more loans as high risk than there actually are.
  * Recall: For recall, both scores are very high with the model getting a recall score of 0.99 for predicting 0s and 0.91 for predicting 1s. The model seems to be almost perfect at predicting healthy loans and high risk loans. However, for both labels (0s and 1s), the model seems to indicate fewer positives than there actually are. This means, when identifying high risk loans, the model may miss some and that could lead to major problems.

* Machine Learning Model 2:
  * Accuracy: The balanced_accuracy_score gives us an accuracy score of aorund 0.952 which is quite high, suggesting that the model is almost perfectly accurate and a well suited model from predicting loan status.
  * Precision: The precision is fairly high for predicting both 0s and 1s, however it is higher for 0s with a perfect score of 1.00. The precision score for identifying loan status' of 1 is a bit lower, at only 0.85. This means that it labels more loans as high risk than there actually are.
  * Recall: For recall, both scores are very high with the model getting a recall score of 0.99 for predicting 0s and 0.91 for predicting 1s. The model seems to be almost perfect at predicting healthy loans and high risk loans. However, for both labels (0s and 1s), the model seems to indicate fewer positives than there actually are. This means, when identifying high risk loans, the model may miss some and that could lead to major problems.


## Summary
I'd recommend either model, if having one was absolutely necessary, as they're both fairly accurate in identifying loans that should be labeled high risk - which is something we're more concerned about. However, if there were another model that was even more accurate, I'd recommend neither of these models as they're both better at predicting 0s - the more low risk label - than they are 1s. This could cause issues if the model does, in fact, miss some loans that should be labeled high risk and instead marks them as healthy. The accuracy and precision scores are the least concerning part of either model. Concern starts with the recall score for 1s. This model is not perfect as is only has a recall score of 0.91 for identifying 1s. While that is a high score, it's not as high as it could be, and it could cause major issues down the line.

In short, if having a model is absolutely necessary, I'd recommend either one. However, if there were a better model available or it was possible to continue without a model until a better one was made, I would recommend continuing on without either of these models.

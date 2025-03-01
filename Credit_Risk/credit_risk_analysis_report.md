# Module 20 Report

## Overview of the Analysis

The purpose of this analysis was to identify the creditworthiness of borrowers for a peer-to-peer lending services company using a dataset of historical lending activity and determine their associated loan risk.

The financial information represented by the data included:
* loan size ($)
* interest rate (%)
* borrower's income ($)
* borrower's debt-to-income ratio
* number of accounts
* derogatory marks (if any)
* total debt carried by the borrower
* loan status (0 meaning healthy, 1 meaning high risk of default)

In this analysis, I needed to predict the y value, which represented loan status--either healthy or high risk of default--based on the x values, which were the features of the dataset outlined in the bullet points above.

The machine learning process stages of this analysis were:
* load and prepare the data
* split the data into Training and Testing sets
* fit a logistic regression model using the Training data
* predict the loan status using the testing feature data and fitted model
* evaluate the model's performance by:
    * generating a confusion matrix
    * printing the classification report

The main method used was LogisticRegression, which is a supervised machine learning algorithm analysis performed to determine whether or not a result belongs in a certain group--in this case, whether given a set of features (x-values), a borrower would default (y=1) or not (y=0).

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Accuracy score: the accuracy score is 99%, which means that the linear regression method is a good fit
    * Precision score: the precision score for healthy loans is 100%, which is the best. This is higher than the precision score for predicting high-risk loans, which is 85%. This means that the model is better at predicting healthy loans than at-risk loans.
    * Recall scores: the recall score for healthy loans is 99% and for high-risk loans, the recall score is 95%. This indicates that healthy loans' ratio of correctly-classified "actual" positives to total "actual" positives is high at 99%, while for high-risk loans the ratio is slightly smaller. However, both scores are high at over 95% each.

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any.

* Which one seems to perform best? How do you know it performs best?
    * Machine Learning Model 1 (Logistic Regression) seemed to perform best, since the accuracy score is 99%, and precision and recall scores are over 85%.
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
    * performance does depend on the problem we are trying to solve; as a lender, it's important to correctly predict a borrower's high-riskiness of default (the 1), which indicates money lost to the lender, as well as to correctly predict the borrow's likelihood of maintaining a healthy loan (the 0), which indicates money recouped by the lender. Both predictions are necessary to balance a lending company's books, although the loan defaults would harm the company most in the short term. A false positive in predicting default (a borrower defaults unpredictably) is much more harmful than a false negative for default (a borrow unpredictably does not default)



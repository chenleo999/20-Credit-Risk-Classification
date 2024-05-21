# 20-Credit-Risk-Classification

completed by Li Chen 5/20/2024

description:

use various techniques to train and evaluate a model based on loan risk

use dataset of historical lending activity from peer-to-peer lending services company to build model to identify creditworthiness 

*** split data into training and testing sets (train_test_split) ***

read csv into Pandas DataFrame
create label, features DataFrame 
* loan status = 0 means healthy, 1 means high risk

create Logistic Regression Model
fit model with training data
use tesing data to predict
evaluate performance by confusion matrix, print classfication report
* answer how well predict is?


*** Write Credit Risk Analysis Report ***
summary and analysis on performance of machine learning model

Precision = TP/(TP+FP), means out of all the cases this model classified as healthy loan, 100% of them are truly health, and 84% of model-classified high-risk loans are correct.

Recall = TP/(TP+FN), means among all healthy loans, this model can identify 99% of them, and for all high-risk loans, this model can identify 94%.

F1-score, defined as Harmonic mean of Precision and Recall. For healthy loans, it is pretty good. For high-risk loans, it is somewhat imbalanced. 

This makes sense to me as lenders would prefer a model with higher recall on high-risk cases. After all, providing funds to high-risk customers being identified as healthy loan would lead to loss of money, while not providing funds to healthy-loan customers being identified as high-risk might result in customer loss, but this is not as too big a deal. In credit risk management, cost of misclassification for high-risk as healthy cases can be significantly higher than other error types. Lower precision in high-risk cases will not harm business drastically.




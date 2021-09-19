# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
The purpose of this analysis is to utilize supervised machine learning, logistic regression, and resampling techniques to become more aware of the credit risk a typical lending firm poses. The data set is imbalanced as the target variable clearly has a majority class, it is important to make sure the model can set these two apart and resample for a better analysis.

* Explain what financial information the data was on, and what you needed to predict.
The financial information is lending data from a peer to peer lending service. The train test split function was used to split the data into training sets and testing sets to make sure that the analysis is clear from bias. The X data is the feautures and y data is the binary outcome(Loan Risk). First train the algorithms with the training data and predict with test data. 

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
The analysis relies on a dataset of lending data with seven columns that characterize each loan such as debt to loan ratio, loan size, etc. The dataset classifies loans in a binary manner; where 0 means the loan is healthy, and 1 means the loan is risk.
From the original dataset the value counts function displayed the target column binary classification for loan health.
class_0 - 75,036 healthy loans
class_1 - 2,500 unhealthy loans
** After resampling of Original Dataset**
class_0 - 56,271
class_1 - 56,721
* Describe the stages of the machine learning process you went through as part of this analysis.
First understood the data that was being worked with, then built a logistic regression model for the original dataset, split data and then fit the model to the training data and tested on the test data. 

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).
Logistic Regression was used to find classifiers for the model to be familiar with for classifying loans. 
As it was apparent that the original dataset was imbalanced, it was necessary to apply resampling method to compare testing results.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
Accuracy - 95% accuracy in predicting the imbalanced loan data as healthy loans heavily outweighted risk loans.
Precision - {0:1.00, 1:.85}The model was sufficient at predicting healthy loans and was subpar with picking out the unhealthy loans as it made more mistakes in target 1.
Recall - {0:.99, 1:.91} - The recall also indicated that the first model was good at predicting healthy loans and decent at predicting risky loans. It shows that unhealthy loans has a less trustable ratio because the model made a few mistakes on classifying unhealthy loans.


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
Accuracy - 99% with a balanced dataset means our model is performing well.
Precision - {0:1.00, 1:.84} The correct amount of positive predictions for the unhealthy class decreased by one percent.
Recall - {0:.99, 1:.99} The unhealthy class was predicted better after the resampling. Its recall rose by 8% which means that this model was much better at predicting unhealthy loans. 
## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
The resampled model perfomed best because its recall is 8% greater than the original dataset. The recall is the best metric to use in this loan classification scenario because it indicates how well the minority class is being predicted(risky loans)
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
The choice of model is the resampled model because it is better at predicting the 1s which is loan risk for the firm. The recall metric specifies how well the model is at predicting the more important class which is unhealthy loans. I would recommend using the resampled model since the type 2 error in the data has become less of a problem as it was in Machine learning model 1.
If you do not recommend any of the models, please justify your reasoning.

# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).

The purpose of this analysis was to evaluate a model we created using a confusion matrix and the metrics it generates(precision and recacll)
to identify how well the model is able to identify a healthy loan vs a high risk loan and if the model is able to capture
all of the high risk and healthy loans presented. 

The financial data presented was loan data containing different parameters and features of a healthy or high risk loan. We seperated our data into
a feature ['y'] data which is whether or not the loan is healthy or not(loan status), and the rest of our data into our X variable containing all the other
parameters listed in the table in the pynb file(loan_size	interest_rate	borrower_income	debt_to_income	num_of_accounts	derogatory_marks	total_debt).

The basic info we were looking at is the value counts which shows 2500 high risk loans denoted by '1' and 75036 healthy loans denoted by '0'.

The stages of the machine learning process was that first we split the data into a feature 'y' variable for loan status and contained the other variables
as mentioneD earlier in the X variable. We then split the data into a training and testing data for both X and y. We then created a logistic regression
model to to fit the training data into the logistic regression model to help us make predictions on the health of future loans using the logistic model. We then
checked the training data and compared it against the testing data to be able to determine how well our model is working in predicting vs the actual results.
We then generated a confusion matrix and a classification report to look at the metrics such as the precision and recall to determine how well our model
is able to predict whether a loan is healthy a high risk loan.

After running the logistic regression model using the original data - we resampled the data in order to improve the accuracy of our model and to
test the model of a different subsection of the data so that our machine learning model can learn from more of the data.

We then generated the same metrics for the resampled data such as our confusion matrix to see if the the resampling had an effect on our precision and
recall scores


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.

The balanced accuracy score of model 1 is 0.9218124642767772 - which is only slightly higher than model. Both models have almost identical accuracy. 

The precision for model 1 shows that it is highly precise for predicting healthy loans and has only 85 percent accuracy in predicting the high risk loans. 

The recall for model 1 model is 99 percent for healthy loans predictions and 91 percent for high risk loan predictions.

In model 1 based on the precision that when we identify a healthy loan we are always right that it is a healthy loan, but when we identify a high risk loan only 
85 percent of the time it is correctly idefntied as such. 

In model 1 we also see that the recall score is is 99 and 91 for healthy loans and high risk respectively. we can see that this moddel captures 99 and 91 percent of the true statements


* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.

  The balanced accuracy score of model 2 is 0.9205494133884273

  The precision for model 2 is is 99 percent for healthy loans and 99 percent for high risk loans meaning it is right 99 percent of the time in predicting both 
  healthy and high risk loans

  The recall for model 2 is 100 percent for healthy loans and 84 percent for high risk loans meaning only 84 percent of the high risk loans are contained in the model



## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.

The model that performs the best in my opinion is model 2 with the resampled data because although the recall is lower and it does not contain as much of the
high risk loans as in model 1, model 2 has as high precision score meaning that it is more able to correctly identify the high risk and healthy loans
when it does make a prediction

It is more important here to be able to identify a 1 as a 1 high as high risk loan can pose more of a threat to our FI than identifying one single correct 
healthy loan. That's why in model 2 we are able to identifty the high risk loans with highe precision meaning that we should be using model 2. 



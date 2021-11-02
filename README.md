# Credit-Card-Fraud-Detection-with-SMOTE-handling
Credit Card Fraud Detection with SMOTE handling due to the class imbalancing problem
Clearly the data is totally unbalanced!!
This is a clear example where using a typical accuracy score to evaluate our classification algorithm. For example, if we just used a majority class to assign values to all records, we will still be having a high accuracy, BUT WE WOULD BE CLASSIFYING ALL "1" INCORRECTLY!!
There are several ways to approach this classification problem taking into consideration this unbalance.
Collect more data? Nice strategy but not applicable in this case
Changing the performance metric:
Use the confusio nmatrix to calculate Precision, Recall
F1score (weighted average of precision recall)
Use Kappa - which is a classification accuracy normalized by the imbalance of the classes in the data
ROC curves - calculates sensitivity/specificity ratio.
Resampling the dataset
Essentially this is a method that will process the data to have an approximate 50-50 ratio.
One way to achieve this is by OVER-sampling, which is adding copies of the under-represented class (better when you have little data)
Another is UNDER-sampling, which deletes instances from the over-represented class (better when he have lot's of data)
Approach
We are not going to perform feature engineering in first instance. The dataset has been downgraded in order to contain 30 features (28 anonamised + time + amount).
We will then compare what happens when using resampling and when not using it. We will test this approach using a simple logistic regression classifier.
We will evaluate the models by using some of the performance metrics mentioned above.
We will repeat the best resampling/not resampling method, by tuning the parameters in the logistic regression classifier.
We will finally perform classifications model using other classification algorithms.

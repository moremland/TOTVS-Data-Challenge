# TOTVS-Data-Challenge
# Author: Matthew Oremland

Source code for Senior Data Scientist data challenge

This Jupyter notebook was created on 64-bit Windows 7 Enterprise (Service Pack 1) with the following specifications:
1. Notebook server 5.6.0
2. Python 2.7.13 [MSC v.1500 32 bit (Intel)]
3. IPython 5.7.0

The code uses the following packages and versions:
1. JSON: 2.0.9
2. pandas: 0.24.2
3. Numpy: 1.16.0
4. sklearn: 0.19.2

The blocks are intended to be executed in order; each is commented with a brief description of its purpose.

Block 1: import necessary packages.
Block 2: read data from file, cast as pandas dataframe
Block 3: Data is scanned; parameters that do not contain variation are removed. Date is removed as it is irrelevant to analysis in this case.
Block 4: Categorical variables are converted into dummy variables for modeling purposes. ID columns are not used as they are not categories in the typical sense.
Block 5: Data is separated into training and testing data sets; 10% of the data are used for testing.
Block 6: The Zero classifier predicts 0 for all transactions. This naive model has an accuracy of 81% since the churn column is imbalanced. All predictive models are compared against the zero model.
Block 7: Logistic regressions are fit for each individual variable and scores compared to the zero model. Then a multivariable logistic model using all inputs is fit.
Block 8: A Random Forest Classifier model is fit to the data and tested against the test set; its performance against the zero model is reported.

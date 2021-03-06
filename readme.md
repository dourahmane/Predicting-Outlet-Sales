# Big Mart Sales III

## Problem Statement
The following description is just as found on [Big Mart Sales 3 Problem Statement](https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/ "Big Mart Sales 3").

**The data scientists at BigMart have collected 2013 sales data for 1559 products across 10 stores in different cities.
Also, certain attributes of each product and store have been defined.
The aim is to build a predictive model and find out the sales of each product at a particular store.
Using this model, BigMart will try to understand the properties of products and stores which play a key role in increasing sales.**

## Data
We have train (8523) and test (5681) data set, train data set has both input and output variable(s).
We need to predict the sales for test data set.

## Data Dictionary
| Variable        | Description|
| :-------------: | :-------------: |
| Item_Identifier| Unique product ID|
| Item_Weight | Weight of product|
| Item_Fat_Content | Whether the product is low fat or not|
| Item_Visibility | The % of total display area of all products in a store allocated to the particular product|
| Item_Type | The category to which the product belongs|
| Item_MRP | Maximum Retail Price (list price) of the product|
| Outlet_Identifier | Unique store ID|
| Outlet_Establishment_Year | The year in which store was established|
| Outlet_Size | The size of the store in terms of ground area covered|
| Outlet_Location_Type | The type of city in which the store is located|
| Outlet_Type | Whether the outlet is just a grocery store or some sort of supermarket|
| Item_Outlet_Sales | Sales of the product in the particulat store. This is the outcome variable to be predicted.|

## Evaluation Metric Used
As stated on [Evaluation Metric](https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/ "Big Mart Sales 3").

## Submission
Submission needs to be in the format as shown in ["SampleSubmission.csv"](https://datahack-prod.s3.ap-south-1.amazonaws.com/sample_submission/SampleSubmission_TmnO39y.csv "Sample Submission Format").

## Summary
I built a scikit-learn pipeline which allows with one line of code to perform the following tasks :

- For numeric data :

  Fill null values with median values.

  Build variables with Quantiles.

  Compute polynomial features.

  Scale variables.
       
- For categorical data :

  Fill null values with mode values.

  Build binary variables.

  Create numeric values for variables like outlet-size.

This helped me build randomn forest and xgboost models .

The best submission result was RMSE = 1152 .

## Bibliography

Part 1 [Hands-on Machine Learning with Scikit-Learn and TensorFlow](http://shop.oreilly.com/product/0636920052289.do)

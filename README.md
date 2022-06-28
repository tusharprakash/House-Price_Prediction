# Problem Statement:

###
A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. For the same purpose, the company has collected a data set from the sale of houses in Australia. The data is provided in the CSV file below.

The company is looking at prospective properties to buy to enter the market. You are required to build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.
###

# Business Goals:

###
You are required to model the price of houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.
###

# Objective:

###
To build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.
The company wants to know:

-Which variables are significant in predicting the price of a house, and

-How well those variables describe the price of a house.

Also, determine the optimal value of lambda for ridge and lasso regression.
###

# Methodology and Important Observations:

###
There are many independent variables specified in the dataset. We perform the EDA and do a visual inspection of the relationship of independent variables with house price. We further use correlation analysis to remove variables with high levels of multicollenearity. 

For categorical variables we do label encoding and use *Point Biserial Correlation* to find out the most significant categorical variables with correlations above 30 percent. 

We then fit a simple linear regression model and check the distribution of error terms and R-squared on training and test data. It is observed that error terms are normally distributed but there is a large gap between training and test R2. We conclude that this overfitting must be because of large number of predictor variables, and not because non-linearity of relationship between denepdent and independent variables. Hence we do not attempt polynomial regression

We then perform regularization using ridge and lasso regression to find out the most important predictor variables on various values of the hyperparameter *lambda*. We choose those values of *lambda* that maximize r-squared on test data
###

# Conclusion

###

The 5 most variable predicted by lasso regression with multicollinear variables removed are **‘GrLivArea’, ‘OverallQual’, ‘TotalBsmtSF’, ‘GarageArea’, ‘Fireplaces’**. The highest r-squared observed for test data with ridge regression is **0.6395** for lambda= of 1 and with lasso is **0.6384*** for lambda of 0.0001.

###



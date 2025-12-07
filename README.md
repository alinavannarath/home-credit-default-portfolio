# Home Credit Default Project Fall 2025
Portfolio containing all of my individual work on the Home Credit Default project that was done for my IS 6812 MSBA Capstone class.  

## Business Problem and Project Objective
- Home Credit is struggling with predicting how capable each applicant is of repaying a loan. Picking the wrong clients increases defaults, which decreases profitability for the company. Similarly, rejecting the right clients who are likely to repay can also contribute to revenue loss.

- This is a predictive analytics project and will use historical data on customers to find strong predictors for default. The model will use the same information on current customers to predict the probability that they will default in the near future.

## Group Solution to the Business Problem
- Utilizing the historical data provided by Home Credit, we ran various models to get the best possible area under the curve (AUC). First, we created a simple logistic regression model, which served as our baseline. From there, we generated a random forest model and a gradient boosted tree model. The gradient-boosted tree model was our best-performing model, with an AUC of 0.74.

## Individual Contribution to the Project
- My contribution consisted of cleaning up the data, which narrowed down the variables from 122 to 12. I also focused on creating the gradient-boosted tree model and adjusted the hyperparameters to get the best possible AUC. 

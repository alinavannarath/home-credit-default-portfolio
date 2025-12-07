# Home Credit Default Project Fall 2025
Portfolio containing all of my individual work on the Home Credit Default project that was done for my IS 6812 MSBA Capstone class.  

## Contents
- ## Business Problem and Project Objective
  - Home Credit is struggling with predicting how capable each applicant is of repaying a loan. Picking the wrong clients increases defaults, which decreases profitability for the company. Similarly, rejecting the right clients who are likely to repay can also contribute to revenue loss.

  - This is a predictive analytics project and will use historical data on customers to find strong predictors for default. The model will use the same information on current customers to predict the probability that they will default in the near future.

- ## Group Solution to the Business Problem
  - Utilizing the historical data provided by Home Credit, we ran various models to get the best possible area under the curve (AUC). First, we created a simple logistic regression model, which served as our baseline. From there, we generated a random forest model and a gradient boosted tree model. The gradient-boosted tree model was our best-performing model, with an AUC of 0.74.

- ## Individual Contribution to the Project
  - [Exploratory Data Analysis](https://github.com/alinavannarath/home-credit-default-portfolio/blob/main/EDA.Rmd): Analysis of Home Credit loans and loan applicants, including visualizations to help understand the distribution of variables.
  - [Modeling](https://github.com/alinavannarath/home-credit-default-portfolio/blob/main/Modeling.Rmd): Developing a simple logistic regression model and a gradient-boosted tree model.
 
- ## Business Value of the Solution
  - During the EDA phase of the project, 8% of loan applicants defaulted. With our gradient-boosted tree model, we can identify the top 10% of high-risk individuals. Of the top 10%, 32% actually defaulted. This means that if we manually review or decline this group, we will remove approximately one-third of all defaults, which reduces the portfolio default rate from 8% to 4.8%.
  -  Although our final model relied heavily on external credit scores, which conflicts with Home Credit's objective of making lending more inclusive, we believe the model is still extremely valuable as a baseline. We can identify the highest-risk individuals to protect the portfolio, and then roll out another model that focuses on identifying safe segments within the high-risk population.
 
- ## Difficulties Encountered Along the Way
  - Runtime: Given how large the original dataset was, it would take us hours to run our models. We had to reduce the number of variables and opt for LightGBM instead of XGBoost to reduce the runtime.
  - Redundancy: We realized later in the project that we had correlated variables that were violating regression principles and were ultimately preventing us from getting a decent AUC. After we removed those redundant variables then our model dramatically improved.
 
- ## What I Learned in the Project
  - Feature Engineering: This was the first time I experimented with feature engineering, and I learned how valuable it can be to help make sense of raw data. It created meaningful inputs that improved model accuracy and efficiency.
  - Data Leakage: There were steps that were taken in the EDA and modeling phase of the project where I inadvertently leaked data. I learned that there are steps that need to be taken before ever splitting the data into training or testing sets, or else it sabotages the model's performance. One example would be imputing missing values using the overall median instead of computing it on the training subset. This prompted me to revisit and redo the modeling steps. 

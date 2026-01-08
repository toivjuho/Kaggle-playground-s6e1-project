The goal of this project is to showcase the proficiency of myself in a basic prediction problem. 
This is done by using a Kaggle playground competition in which the goal is to predict students exam results based on dataset given. 

Link to the datasets and competition instructions:
https://www.kaggle.com/competitions/playground-series-s6e1/overview

For the feature engineering the following example was used to influence of creating the new variables:
https://www.kaggle.com/code/mdevian/ps-s6e1-student-test-scores-xgboost

This project includes following steps:
- Data tidying
  * Data transformation for approriate form for the use of XGBoost
- Feature Engineering
  * Conservative addition of ratios and intersections of known variables (some of created new variables were removed to avoid multicollinearity -> not included in R-code)
- Modelling and hyperparameter tuning with XGBoost
  * Limited hyperparameter tuning and best models with and without FE included
- Predictions

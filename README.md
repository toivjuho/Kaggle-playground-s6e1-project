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
  * Conservative addition of ratios and intersections from known variables (some of created new variables were removed to avoid multicollinearity -> not included in R-code)
- Modelling and hyperparameter tuning with XGBoost
  * Limited hyperparameter tuning and best models with and without FE included
- Predictions

Editor notes:
- Data tidying
  * Tidying is likely not performed with the most efficient way. Original data is sectioned based on which kind of changes variables needed
  * Some of the transformations are done differently to avoid certain issues/improve the quality of variables in feature engineering (ie. study_hours, sleep_hours and class_attendance is transformed into similar procentual form and categorial variables with three categories are valued with 1-3)
- Feature Engineering
  * This is partially influenced by person doing more heavy FE (link above). The approach for this project was more conservative. This meant trying to create variables which might have interesting information (either used by influence or not) and then performing correlation test to remove some of the new variables with high correlation between each other.
  * This FE considered only ratios and interactions
- Modelling
  * Due the limitation of gear the modelling part is limited to using only one fairly fast model: XGBoost
  * Due the same issues the hyperparameter tuning is done via minimal grid search method
  * R-code features best performed models from with FE and without FE for comparison

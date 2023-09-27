# Student Performance Indicator


## PROBLEM STATEMENT
This project understands how the student's performance (test scores) is affected by other variables such as Gender, Ethnicity, Parental level of education, Lunch and Test preparation course.

## DATA COLLECTION
- Dataset Source - https://www.kaggle.com/datasets/spscientist/students-performance-in-exams?datasetId=74977
- The data consists of 8 column and 1000 rows.


### DATA DESCRIPTION
1.	gender : sex of students -> (Male/female)
2.	race/ethnicity : ethnicity of students -> (Group A, B,C, D,E)
3.	parental level of education : parents' final education ->(bachelor's degree,some college,master's degree,associate's degree,high school)
4.	lunch : having lunch before test (standard or free/reduced)
5.	test preparation course : complete or not complete before test
6.	math score
7.	reading score
8.	writing score.


### DATA CHECKS TO PERFORM
- Check Missing values
- Check Duplicates
- Check data type
- Check the number of unique values of each column
- Check statistics of data set
- Check various categories present in the different categorical column


### MODEL TRAINING

<ins>Model Selection</ins> - After clusters are created, we find the best model for each cluster. We are using the following algorithms:
- "Random Forest": RandomForestRegressor(),
- "Decision Tree": DecisionTreeRegressor(),
- "Gradient Boosting": GradientBoostingRegressor(),
- "Linear Regression": LinearRegression(),
- "XGBRegressor": XGBRegressor(),
- "CatBoosting Regressor": CatBoostRegressor(verbose=False),
- "AdaBoost Regressor": AdaBoostRegressor()
  
For each algorithm, best parameters derived from GridSearch are passed. We calculate the Rsquared scores for the models and select the model with the best score. The model is saved for use in prediction. 


### DEPLOYMENT
We have deployed our model as a web application using flask.

# Fitbit---Calories-burnt
Problem Statement:-
To build a regression model to predict the calories burnt based on the given indicators in the training data. 

Data Description:-
1.	Id: The customer ID
2.	Activity Date: The date for which the activity is getting tracked.
3.	Total Steps:  Total Steps taken on that day.
4.	Total Distance: Total distance covered.
5.	Tracker Distance: Distance as per the tracker
6.	Logged Activities Distance: Logged 
7.	Very Active Distance: The distance for which the user was the most active. 
8.	Moderately Active Distance: The distance for which the user was moderately active.
9.	Light Active Distance: The distance for which the user was the least active.
10.	Sedentary Active Distance: The distance for which the user was almost inactive.
11. Very Active Minutes: The number of minutes for the most activity.
12. Fairly Active Minutes: The number of minutes for moderately activity.
13. Lightly Active Minutes: The number of minutes for the least activity
14. Sedentary Minutes: The number of minutes for almost no activity
15. Calories (Target): The calories burnt.
	
Model Training :-
1) Data Export from Db - The data in a stored database is exported as a CSV file to be used for model training.
2) Data Preprocessing   
   a) Drop columns not useful for training the model. Such columns were selected while doing the EDA.
   b) Replace the invalid values with numpy “nan” so we can use imputer on such values.
   c) Check for null values in the columns. If present, impute the null values.
4) Model Selection - We are using two algorithms, “Random forest Regressor" and "XGBoost regressor". For each model, both the algorithms are passed with the best parameters derived from GridSearch. We calculate the R squared scores for both models and select the model with the best score. Similarly, the model is selected and is saved for use in prediction.


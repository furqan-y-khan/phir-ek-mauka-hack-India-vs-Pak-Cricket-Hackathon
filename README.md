# phir-ek-mauka-hack-India-vs-Pak-Cricket-Hackathon

Introduction:
We will need to predict the runs scored and wickets taken by these 30 players in the upcoming clash between India and Pakistan.
By Using Deep Learning Method namely Vanilla Neural Networks.

Data Collection:
Data Sources: Used Analytics Vidhya provided datasets for analysis and predication. 
Key attributes of dataset are 

Column
Description
player_id
Unique identifier of a player
player_name
Name of the player
runs_scored
No. of runs scored by the player in the match
wickets
Wickets taken by the player in the match
runs_conceded
No. of runs conceded by the player
catches
No. of catches taken by the player
stumpings
No. of stumpings done by the player
match_date
Date of the match
opposition
Opponent team name and Ground 
match_id
Unique identifier of the match



Imported Libraries & Load Dataset:
Importing essential libraries namely pandas, numpy, matplotlib.pyplot, Keras etc.
Importing train_test_split library from sklearn.model_selection
Importing nn module from keras
The dataset loaded by using pandas read_csv 

Data Preprocessing:
Verified Dataset first few rows by using head, tail and sample function
Verified size and shape of the dataset
By using describe function, analysed statistical measures of data frame.
 By using info method, analysed non-null count, dtype of columns of dataframe
Converted object datatype to integers of runs_scored, wickets, runs_conceded, catches, stumpings columns by cleaning data, handling missing values and data transformation.
The match_date column is converted to a datetime format for easier handling and manipulation of date-related operations.
Dropped unnecessary columns in feature engineering. 
Created a median runs for every player and multiplied with impact number
Predicted on this median run of every player.


Feature Engineering:
The Dataset spilt into training & testing for   predicting runs and wickets. 
Consider x columns as player_id, match_date, y columns as runs_scored, wickets with two different codes. 

Model Selection:
Chosen Machine learning models as MultioutRegression and RandomForestRegressor doesnot seem to work so I went with the heart of machine learning that is neural networks. 
The model is trained on the training dataset and predictions are made on the test dataset and median dataset. 

Evaluation Metrics:
Mean_squared_error metrics used to assess model performance. 

Results:
Using the trained models, predictions are made for runs and wickets for the India and Pakistan  match. 
The predictions are saved in a CSV file named. 

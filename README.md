# nba
Data science and ML project on predicting the NBA season and playoffs data
# Introduction
The objective of this proect is to predict the 2022-2023 regular season of the NBA, and the outcome of its post season games. 

Historical data of games statistics since the 1980 season were obtained. However, due to the several changes in the teams, franchises, and NBA system, the data used to develop the ML models began from the 2015 season; when the NBA teams became more consistent. The NBA teams https://www.nba.com/teams are organized in conferences as such: Atlantic, Central, and South East teams are in the Eastern conference while Northwest, Pacific, and Southwest teams are in the Western Conference.

Every regular season, there are 30 teams divided into two conferences: Western and Eastern. Each team plays 82 games per season. At the end of the regular season, the seven teams with the most wins in each conference qualify for the playoffs. The winners from each conference play against each other in the NBA finals which is a best-of-7-games series like other playoff series.

2 different models were developed and used to perform predictions on what teams qualified for playoffs, while 3 different models were built to predict the winner of the post-season playoffs games; the NBA finals. The results of these different models were compared to see which model would be the most accurate.

Finally, a virtual team was created to participate in the 2023 season. The team referred to as 'The Avengers', was given a position on the 2023 season league table; the trained model was used to predict if the team would make it to the playoffs or not.
# Data Source
*Elo ratings

The Complete History Of The NBA From https://data.fivethirtyeight.com/

Data Explanation: https://github.com/fivethirtyeight/data/tree/master/nba-elo

Data: 1. https://github.com/fivethirtyeight/data/blob/master/nba-elo/nbaallelo.csv

nba_elo.csv contains game-by-game Elo ratings and forecasts back to 1946. nba_elo_latest.csv contains game-by-game Elo ratings and forecasts for only the latest season.

2. https://projects.fivethirtyeight.com/nba-model/nba_elo.csv

3. https://projects.fivethirtyeight.com/nba-model/nba_elo_latest.csv From https://github.com/fivethirtyeight/data/tree/master/nba-forecasts

RAPTOR

Data Explanation: https://github.com/fivethirtyeight/data/tree/master/nba-raptor

Data:

4. https://projects.fivethirtyeight.com/nba-model/2023/latest_RAPTOR_by_team.csv

The data obtained from these sources were analysed and cleaned up to suit the ML model training process.
# Model Building
Three different types of models, Logistic Regression, Random Forest, and Support Vector Machine (SVM).

The performance statistics used to train the models include; team avergae elo rating per season, total points scored per season, and team win rate (total wins / total season games). These values were put ino a dataframe and scaled using MinMaxScaler.

The regular season data was split by Eastern and Western conferences. From the split data, 2015 to 2022 was used to train the model. The 2020 season was left out of this project due to the incomplete statistics from that season. The trained models were tested against the 2023 season.

The playoffs data were aggregated and split from 2015 to 2022 for training and 2023 data for testing and predicting.
# Results
The model predictions for the 2023 season showed that the Eastern Conference models were better at predicting the teams more precisely than the Western Conference models. 2 out of 3 of the models that were developed to predict the playoffs winner seemed to have a hard time deciding the winner, however, the models also predicted the probabilities of each team winning the playoffs.
# Conclusion
Logistic, Random Forest and Support Vector Machine all provided similar predictions with good enough accuracy. The challenges the models faced may be due to insufficient historic data, or the models may be in need of more feature engineering. Model performance at this stage seems satisfactory with room for improvement.

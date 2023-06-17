# Board_Game_Recommender_Jupyter
# Jupyter Notebooks for EDA, Similarity Score Calculation, and Push to Azure PostgreSQL Server
Public Projects

This repository holds the different notebooks used to create the similarity scores used in the collaborative filtering. The data used in these notebooks was obtained here: https://www.kaggle.com/datasets/threnjen/board-games-database-from-boardgamegeek?select=games.csv,
which was sourced using BoardGameGeek's XML API.


In order to have multiple ways of filtering based on a given games the scores were calculated using:

* Combined Mechanics and Themes feature data
* Mechanics features biased with a small amount of user to user similarity scores
* Theme features biased with a small amount of user to user similarity scores
* Game descriptions (count vectorization). This did not work as well, but I may give this another try.

The scores were pushed to a SQL server after some cleaning of games names due to special characters and duplicate names.

Each game has its own table in the SQL server with multiple scores referenced to every other game in the database.


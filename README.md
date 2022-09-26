<h1 align="center"> Movie Recommendation System </h1>

# Introduction
This project retrieves movie rating data from [Netflix prize dataset](https://www.kaggle.com/datasets/netflix-inc/netflix-prize-data) and builds a recommendation system based on Alternating Least Square (ALS) Matrix Factorization. Spark ML is used for implementation of the model.

# Part 1: OLAP
Use Spark SQL to explore the movie rating dataset by looking into these aspects:

1. About users
- Number of users
- Number of movies rated by each user
- Minimum and maximum number of movies rated by each user
- User distribution with respect to the quantity of rated movies

2. About movies
- Number of movies
- Number of movies in each year
- Number of users rating each movie
- Minimum and maximum number of users rating each movie
- Movie distribution with respect to the quantity of raters

3. About ratings
- Distinct values of rating
- Average rating of each movie
- Movie with the highest and lowest average rating
- Movie distribution with respect to the average rating
- Average rating of movies in each year
- Best movie in each year

# Part 2: Model Training
- Use grid search and cross validation to find the best set of hyperparameters. 
- Then adopt the best hyperparameter set to train the model again using the entire dataset. 
- Finally, save the fully trained model which will be used for giving recommendation.

# Part 3: Recommendation
- Find similar movies to a given movie by the cosine similarity of their feature vectors derived in ALS model.
- Recommend movies to an existing user by selecting the movies with highest predicted ratings given by the ALS model.
- Recommend movies to a new user, who has just watched a few movies. Include that user's viewing history in the training set and retrain the model. Then give recommendations correspondingly.
# Recommendation-System
Building a recommendation system using both collaborative filtering and content-based filtering

## Collaborative Filtering
Building a recommendation system using collaborative filtering that recommends movies based on ratings of users with similar taste using autodiff functionality in tensorflow.
For a existing user we make recommendations by using the prediction matrix and sorting the movies according to predicted rating
We can also find similar movies by the distance metric and the distance matrix and then suggest similar movies

Collaborative Filtering suffers from the problem of cold start which is making recommendations for users who have not yet rated movies and suggesting newer movie that have been not yet rated by many users
It also does not efficiently utilise other side information such as features of individual movies and users

## Content-based Filtering 
Building a recommendation system using content-based filtering that recommends movies using features of individual movies and users using tensorflow keras functional API.
Making a complex neural network with two sub-networks namely for user and item
Then for making recommendations for new or existing user we again predict the ratings by carrying out inference on the trained network and then selecting the movies with highest predicted ratings

To optimize this recommendation procedure for large datasets we precompute the movie vectors by carrying out the inference on the item neural network separately and then when a user wants recommendations we only run inference with the users vector on the user neural network and then obtain the predicted ratings
This is carried out in two steps called Retrieval and Ranking

Moreover we can find similar movies to a given movie in a similar fashion as done in collaborative filtering which is by computing the decision matrix


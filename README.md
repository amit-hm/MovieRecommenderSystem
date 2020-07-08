# MovieRecommenderSystem
This is an implementation of Latent Factor Recommendation System to recommend movies to users.

Suppose we are given a matrix R of recommendations. The element R of this matrix corresponds to the rating given by user u to item i. The size of R is m × n, where m is the number of movies and n the number of users.

Most of the elements of the matrix are unknown because each user can only rate a few movies.

Our goal is to find two matrices P and Q, such that R = QP_T . The dimensions of Q are m × k, and the dimensions of P are n × k. k is a parameter of the algorithm. We define the error as

![Error](Images/Error.png?raw=true "Error Calculation")

The Σ(i,u)∈ratings means that we sum only on the pairs (user,item) for which the user has rated the item, i.e., the (i,u) entry of the matrix R is known. qi denotes the ith row of the matrix Q (corresponding to an item), and pu the uth row of the matrix P (corresponding to a user u). λ is the regularization parameter. ||.||2 is the L2 norm and is square of the L2 norm, i.e., it is the sum of squares of elements of pu.

# Implementation
The code is in Movie Recommender System.ipynb
## Dataset
ratings.csv: this is the matrix R. Each entry is made of a movie id, user id, and a rating that is an integer between 1 and 5.

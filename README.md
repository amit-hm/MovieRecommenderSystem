# MovieRecommenderSystem_Spark
This is an implementation of Latent Factor Recommendation System, using PySpark, to recommend movies to users.

Suppose we are given a matrix R of recommendations. The element R of this matrix corresponds to the rating given by user u to item i. The size of R is m × n, where m is the number of movies and n the number of users.

Most of the elements of the matrix are unknown because each user can only rate a few movies.

Our goal is to find two matrices P and Q, such that R = QPT . The dimensions of Q are m × k, and the dimensions of P are n × k. k is a parameter of the algorithm. We define the error as

![Error](Images/Error.png?raw=true "Title")

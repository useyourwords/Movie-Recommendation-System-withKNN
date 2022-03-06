# Movie-Recommendation-System-withKNN

- **Objective of the work:** Our purpose is to recommend 5 movies similar to the movie the user is looking for through our movie recommendation system when the user searches for a movie, using an item-based collaborative filtering algorithm.
- In this study, we use item-based collaborative recommendation system and modeled the similarity with the help of the KNN algorithm.

## Dataset Description
<img width="331" alt="image" src="https://user-images.githubusercontent.com/90156792/156937965-a5847b2d-3ea3-4368-9e7b-82951c696ca0.png">

## Algorithm used
1. Created a new pivot table dataset using the "movies" and "ratings" datasets. The columns of the new dataset represent the "userId" and the rows the "movieId". "userId" and "movieId" intersections are filled with rating values.
2. Filled the missing "rating" values with "0" to make it more understandable for the algorithm.
3. In order to make the recommendations more meaningful, how many people voted for the movies was examined. Likewise, the number of movies users voted was taken into account. We eliminated movies rated by a small number of users and users who voted for a small number of movies.
   
   Some filters used (thresholds)
   
	◦ A minimum of 10 users should have voted a movie
  
   ◦ A minimum 70 movies should have voted by the user
  
4. Sparse matrix was created.

5. KNN model was created with "metric=cosine", "algorithm=brute" and "n_neighbors=20". The cosine distance metric is faster when compared to the Pearson coefficient. Euclidean distance does not work correctly when the values are equidistant.

6. 5 movies that are closest to the movie that the user typed as input are recommended. Distances are also shown in the output. Using cosine distance, we get values between 0 and 1, where 0 means the vectors are 100% similar to each other and 1 means they are not similar at all. 

## Output

<img width="336" alt="image" src="https://user-images.githubusercontent.com/90156792/156938279-2fc8778b-2edc-476a-afa0-612d9666ca07.png">



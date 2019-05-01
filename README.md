# Anime-Recommendation

As a newbie in the world of anime, I depended on my friends for suggestions on what to watch. So instead of asking them everytime, i decided to take it into my own hands. I built this recommendation system using collaborative filtering. 

# The Dataset
This repository was posted on Kaggle by CooperUnion in 2017 with a goal to Build a better anime recommendation system based only on user viewing history.
This data set contains information on user preference data from 73,516 users on 12,294 anime. Each user is able to add anime to their completed list and give it a rating and this data set is a compilation of those ratings.
It has two CSV files, anime.csv and rating.csv.
# Features

######	Anime.csv

-	anime_id : myanimelist.net's unique id identifying an anime.
-	name : full name of anime.
-	genre : comma separated list of genres for this anime.
-	type : movie, TV, OVA, etc.
-	episodes : how many episodes in this show. (1 if movie).
-	rating : average rating out of 10 for this anime.
-	members : number of community members that are in this anime's "group".

######	Rating.csv	

-	user_id : non identifiable randomly generated user id.
-	anime_id : the anime that this user has rated.
-	rating : rating out of 10 this user has assigned (-1 if the user watched it but didn't assign a rating).

# Installation
This project requires python 3.6 or anyother higher versions of python, along with these libraries :
- numpy
- pandas
- Plotly (Create an account and copy the API key)
- matplotlib

# About the Repository

- This repository contains 3 Notebooks and 2 csv files.
- Visualiaztion.ipynb contains a visualization of the csv data files in the dataset.
- The recommendation Euclidian.ipynb contains the recommendation based on similarity filtering using Eucildian 
  distances.
- The recommendation Pearson.ipynb contains the recommendation based on similarity filtering using Pearson 
  Correlation.

 
# Running the Code


# A Jist of what it does

# The Recommendation
Even though the data is the same, the recommendation given by the two types of recommendation techniques are completely different.



# For the Newbies. 
### How Collaborative filtering Works

### Building your preference list

### Similarity Scores

### Ranking the Similarity Scores

### Recommending Items
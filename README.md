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
In a terminal or command window, navigate to the top-level project directory and run the command below:

	jupyter notebook recommedation Ecuclidian.ipynb

You can change the name of the notebook to whichever notebook you want to open.

This will open the Jupyter Notebook software and project file in your browser.


# The Recommendation
Even though the data is the same, the recommendation given by the two types of recommendation techniques are completely different.



# For the Newbies. 

### How Collaborative filtering Works
A collaborative filtering algorithm usually works by searching a large group of people
and finding a smaller set with tastes similar to yours.

### Building your preference list
The first thing you need is a way to represent different people and their preferences.
In Python, a very simple way to do this is to use a nested dictionary.


### Similarity Scores
After collecting data about the things people like, you need a way to determine how
similar people are in their tastes. You do this by comparing each person with every
other person and calculating a similarity score. I have used Euclidian and Pearson Scores.

### Ranking the Similarity Scores
Next create a function that scores everyone against a given person and finds the closest matches. In this
case, I’m interested in learning which anime users have tastes simliar to mine so that
I know whose advice I should take when deciding on an anime.

### Recommending Items
Finding a good user to read is great, but what I really want is an anime recommendation
right now. I could just look at the person who has tastes most similar to mine
and look for an anime he likes that I haven’t seen yet, but that would be too permissive.
Such an approach could accidentally turn up reviewers who haven’t reviewed
some of the animes that I might like. It could also return a reviewer who strangely
liked a movie that got bad reviews from all the other users returned by topMatches.
To solve these issues, you need to score the items by producing a weighted score that
ranks the users.
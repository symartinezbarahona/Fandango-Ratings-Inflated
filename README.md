# Capstone Project - Are Fandango's Movie Ratings Inflated? 
## Overview

When planning on seeing a movie, how well can you trust online reviews and ratings? What if the online reviewer company showing the rating *also* makes money by selling movie tickets. Do they have a bias towards rating movies for the sake of higher profit?

In this capstone project, with the guidance of Jose Portilla, Instructor of 2022 Python for Machine Learning & Data Science, I will explore whether or not Fandango artificially displays higher ratings than warranted to boost ticket sales. Ultimately, the goal is to tell a compelling data-driven story as well as showcase my skills as a python programmer. Hope you enjoy!  

----

### Setup

1. Fork or clone this repo to your own computer and `cd` into the directory
2. Make sure you have the proper dependencies installed. 
   -   You can do this by typing `pip install -r requirements.txt` in the command line

----

### The Data

This is the data behind the story [Be Suspicious Of Online Movie Ratings, Especially Fandango’s](http://fivethirtyeight.com/features/fandango-movies-ratings/) openly available on 538's github: https://github.com/fivethirtyeight/data. There are two csv files, one with Fandango Stars and Displayed Ratings, and the other with aggregate data for movie ratings from other sites, like Metacritic, IMDB, and Rotten Tomatoes.

----

#### all_sites_scores.csv


`all_sites_scores.csv` contains every film that has a Rotten Tomatoes rating, a RT User rating, a Metacritic score, a Metacritic User score, and IMDb score, and at least 30 fan reviews on Fandango. The data from Fandango was pulled on Aug. 24, 2015.

Column | Definition
--- | -----------
FILM | The film in question
RottenTomatoes | The Rotten Tomatoes Tomatometer score  for the film
RottenTomatoes_User | The Rotten Tomatoes user score for the film
Metacritic | The Metacritic critic score for the film
Metacritic_User | The Metacritic user score for the film
IMDB | The IMDb user score for the film
Metacritic_user_vote_count | The number of user votes the film had on Metacritic
IMDB_user_vote_count | The number of user votes the film had on IMDb

----

#### fandango_scape.csv

`fandango_scrape.csv` contains every film 538 pulled from Fandango.

Column | Definiton
--- | ---------
FILM | The movie
STARS | Number of stars presented on Fandango.com
RATING |  The Fandango ratingValue for the film, as pulled from the HTML of each page. This is the actual average score the movie obtained.
VOTES | number of people who had reviewed the film at the time we pulled it.

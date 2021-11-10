# Spotify Data Analytics and Visualisation

## Backgroud

*What is Spotify? How is the market share? etc.*




## Data Source

### Open Dataset

Dataset: Spotify Songs
https://github.com/rfordatascience/tidytuesday/tree/master/data/2020/2020-01-21

```R
spotify_songs <- readr::read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2020/2020-01-21/spotify_songs.csv')
```



### Spotify API

We will also be downloading our own spotify data by using `spotifyr` package to get data on demand.

> Sample queries

First register on Spotify as a developer.

⬇️ What was the Beatles' favorite key?

```R
# install.packages("spotifyr")
library(spotifyr)
# System settings
Sys.setenv(SPOTIFY_CLIENT_ID = '96d8c2cea37c435ea73b9866b72a00d7')
Sys.setenv(SPOTIFY_CLIENT_SECRET = 'f93a0e7682bb431e9cbf31f08d5fe069')

access_token <- get_spotify_access_token()
beatles <- get_artist_audio_features('the beatles')

beatles %>% 
  count(key_mode, sort = TRUE) %>% 
  head(5) %>% 
  kable()
```



## Questions to answer

We want to analyse the most popular songs, the different genres, what makes a song popular and other things. Ideally we will use our own data in combination with the dataset and analyse our listening patterns. 
* What trends are we seeing on popularity of song genre, popularity, and release date 
* What songs and genres are more similar to each other than others? 
* What features of a song (ex: tempo, valence, etc.) can explain their popularity at a greater degree?
* Discover commonalities on modes, song types, and artist 

## Statistical Techniques 

* Regression Analyses 
* Similarity Analysis 
* Item-Based Cluster Analysis 
* General Data Exploration (Avg, Count, Max, Min, Mean, Median) 




## To-do list

- [ ] Fill the Background
- [ ] Fill the Sample query in R (and register a API key)
- [ ] Fill the questions to answer



## Storyline





## References


> NOTE: 

As a back-up, we have chosen:
https://databank.worldbank.org/source/environment-social-and-governance?preview=on#




# The Ultimate-ish Movie Review
Project Goal: To use movie data from preexisting spreadsheets, as well as the OMDB API to uncover trends across films and their gross earnings.

## Project Questions
1. Do ratings corrrelate to the total revenue that a film earns?
    Intent: Compare ratings from IMBD, Metacritic, and Rotten Tomatoes to assess if there are is a correlating between ratings and the amount of gross earnings for the films.
2. Do certain actors and directors generate higher grossing films?
    Intent: Look at the per film average gross earings and total gross earnings by actor and director.
3. Are their more advantageous times to release a film to general higher earnings?
    Intent: Compare release dates for films and see if there are trends regarding box office performance based on release year, release month, and calendar season.

## Project Resources in the Resource folder
1. Top 1000 Highest Grossing Movies of All Time csv file, downloaded from Kaggle: https://www.kaggle.com/datasets/therealoise/top-1000-highest-grossing-movies-of-all-time
- file entitled Top_1000_Highest_Grossing_Movies_Of_All_Time.csv
- Dataset updated Sept 5, 2022
2. IMDb 5000+ Movies csv file, downloaded from Kaggle: https://www.kaggle.com/datasets/rakkesharv/imdb-5000-movies-multiple-genres-dataset?resource=download
- file entitled IMDb_All_Genres_etf_clean1.csv
3. Movie Metadata csv file, downloaded from Kaggle: https://www.kaggle.com/datasets/karrrimba/movie-metadatacsv
- file entitled movie_metadata.csv
- file not used as movie titles were formatted in a way that it led to duplicating over 4000 films within the data set

## Project Findings
1. Do ratings corrrelate to the total revenue that a film earns?
- The IMDb 5000+ Movies file contained IMDb scores, while the Top 1000 films file contained Metascore ratings.  Additional Metascore ratings, and Rotten Tomatoes data was not able to the pulled due to persistent connection issues when using the OMDB API.
- The dataset was trimmed down to the movies with both IMDb and Metascore ratings to ensure consistency.
- Neither IMDB ratings nor Metascore ratings correlated strongly to gross revenue earnings, with r-values of .28 and .27, respectively. There was little difference between IMDB and Metascore ratings for the same set of films, illustrating that neither system’s methodology was more accurate in predicting the financial success of a film, as IMDB allows user-ratings to dictate the score and Metascore relies solely upon the weighted average of industry critic experts. While a weak correlation, IMDB ultimately produced a slightly higher r-value. 
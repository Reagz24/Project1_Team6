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

# Project Findings
## 1. Do ratings corrrelate to the total revenue that a film earns?
- Applicable images from the images folder are IMDB_Gross.png and  Meta_Gross.png

- The IMDb 5000+ Movies file contained IMDb scores, while the Top 1000 films file contained Metascore ratings.  Additional Metascore ratings, and Rotten Tomatoes data was not able to the pulled due to persistent connection issues when using the OMDB API.
- The dataset was trimmed down to the movies with both IMDb and Metascore ratings to ensure consistency.
- Neither IMDB ratings nor Metascore ratings correlated strongly to gross revenue earnings, with r-values of .28 and .27, respectively. There was little difference between IMDB and Metascore ratings for the same set of films, illustrating that neither system’s methodology was more accurate in predicting the financial success of a film, as IMDB allows user-ratings to dictate the score and Metascore relies solely upon the weighted average of industry critic experts. While a weak correlation, IMDB ultimately produced a slightly higher r-value. 

## 2. Do certain actors and directors generate higher grossing films?
(Note on methodology: We looked at the top 20 directors and actors of the highest grossing films by average and by total. For the analysis, we used only the top-credited director and actor for a given film.) 
- Applicable immages from the images folder are Director_Average.png , Director_Total.png , Actor_Average.png , and Actor_Total.png

- Stephen Spielberg runs away with the number one spot for director with the highest total box office earnings of more than $3.7 billion, leading the rest of the director field by more than $1.4 billion. Michael Bay comes in second at $2.3 billion, followed by Anthony Russo in third with $2.28 billion. While Spielberg handily wins this category, he is absent from the top 20 directors by average box office, coming in at 82 with average Box Office earnings of $138m. 
- Only 25% of directors appear on both lists. Avengers director, Anthony Russo, had the highest average box office earnings with $456 million. Some further areas of exploration to consider would be how the number of films a director has made impacts the average, as well as the years directors were active where revenue in earlier years was substantially lower than contemporary revenue earnings from film. 
- Only 3/20 actors and actresses are in the top 20 for both total earnings and average earnings. Daisy Ridley tops the average list and features on the total revenue list for her work as the lead actress in the most recent Star Wars trilogy, with her films average $690 million. Tom Hanks’ films earned more than any others on the list with more than $4 billion.
- By only focusing on top-credited directors and actors/actresses, we limited the scope of the data we pulled in to only account for a director/actor’s top work, which means the average fails to account for all of their other work which may be less acclaimed or less profitable. Daisy Ridley exemplifies this, who topped the average list, but that ranking only accounts for her leading work in the Star Wars franchise and not her other films.

## 3. Are their more advantageous times to release a film to general higher earnings?
- Both datasets used included release years for films.  Release month was not able to be pulled from the OMDb API due to persistent connection issues, and thus was not able to be analyzed.
- Applicable images from the images folder are Year_Average.png , Year_Total.png , and Film_Count.png

- Of the data available, 2016 was the highest-grossing year for films, generating nearly $11 billion in revenue. There were significantly fewer films in the dataset from the early-mid 20th century leading to spikes in the average box-office earnings, due to years when a blockbuster came out like 1939's Gone With the Wind. Revenue began to rise exponentially in the 1980s and continued to double with each decade. Film revenue took a nosedive in 2020 during the COVID-19 pandemic and dropped to levels not seen since the early 1980s. This time period also reflects a shift towards streaming which has eaten into box office earnings. Integrating streaming data would help elucidate the impact of streaming platforms on traditional box office revenue. 
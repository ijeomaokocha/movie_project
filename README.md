# movie_project
# Introduction
This data set contains information of about 10,000 movies collected from movie database.

The following are the columns and their meanings: Id - The unique identifier of the data imdb_id - International Movie Database identifier popularity - Popularity index per movie budget - Amount spent in making movie revenue - Total Amount received from movie original_title - Name of the movie cast - Actors/Actresses that starred in the movie homepage - Movie website director - Movie director tagline - Tagline of the movie keywords - Associated words with the movie content overview - description of the movie runtime - Movie time in minutes genres - Genres associated with the movie (separated by "|") production_companies - Companies involved in the movie production release_date - Date of movie release vote_count - Number of votes on the movie rating vote_average - Mean votes of voter count and voter rating release_year - Year of movie release budget_adj - Budget with inflation accounted for as at 2010 revenue_adj - Revenue with inflation accounted for as at 2010
### Questions
From the dataset above we would consider the profit margin of each movies across the years using the budget_adj and the revenue_adj, which shows the budget with inflation accounted for as at 2010 and revenue with inflation accounted for as at 2010, since it accounts for the inflated prices we can get the difference and analyse:

(a) How profitable has the movie industry been across the years (b) How popularity affects profits (c) How runtime affects profits (d) How does release date affect profit
### Summary 
- Feature Engineering was done to bring out some Variables 
- Exploratory Data Analysis

Generally its good to know the factors that makes a movie profitable and to take avantage of those factors From our analyses we see that the movie industry as a whole is a profitable one which makes an average of 50 million dollar profit per year, where inflation has been accounted for as at 2010 Popularity is a factor in making profits, but we have a limitation of what measurement was used to get the popularity points, which makes it an unreliable factor. Runtime is a key factor in making profits, we saw that the average runtime for a profitable movie is 102 minutes,Directors can take a clue fom this and make their movies about 30 minutes within the average runtime. We saw that Wednesdays and Thurdays are best to release a movie in the months of June or December to be most profitable. We also se that this is influenced by the vote count. Viewers seem available to vote on these same times. An investigation to this might show the availablity of veiwers at these month.
Run time is a huge factor in determining the profit of a movie, it can be advisable to consider movies to be 30 minutes range from the average runtime to be profitable
runtime also shows viewers attention span to movies irrespective of the genre.
### Limitations
We found some errors which posses questions like;How the popularity is being measured, what are the factors that determine the popularity figures in this data set. we saw some recording of zero runtime and , if that is possible then no movie was made, so there might have been few data entry errors Other factors affect the vote count, which affects the profit and we would have loved to explore more if influences like, age groups, holidays and more data on the viewers were included.
popularity data here does not tell us how it was being measured , as we are just given different number as points. More questions on why a movie is popular comes to mind
### References
www.google.com https://pandas.pydata.org/docs/reference/api/pandas.to_datetime.html https://www.analyticsvidhya.com/blog/2016/01/guide-data-exploration/

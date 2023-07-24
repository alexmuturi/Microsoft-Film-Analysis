# Microsoft Movie Analysis

**Author**: Alex Muturi
![A]("images/200w.gif") 
 

## Overview
Microsoft is looking to enter the film industry, and this analysis is conducted to help the company choose an informed entry position. It analyses datasets with film information to generate insights and recommendations. 

Data-backed answers to the proposed business questions suggest that Microsoft invests generously in Adventure, Action, Comedy and Drama genres.



## Business Problem
As a business, the main intention to join the film industry is the industry's potential for profit. Therefore, the business problem is to consider all available factors and make a decision that optimizes returns. 

This analysis proposes 3 business questions to help with the goal:
1. What are the most Popular Genres? 
2. Which Genres have the highest monetary returns?
3. Does a higher production budget translate to higher returns?

The selection of these questions is based on the type of data available and the intention mentioned above. 


## Exploratory Data Analysis
The data used in the analysis was sourced from [IMDB Developer](https://developer.imdb.com/non-commercial-datasets/) non commercial datasets collection. I used the following datasets:

 
>title.basics.csv\
>title.ratings.csv\
>bom.movie_gross.csv\
>tn.movie_budgets.csv

They can all be accessed from the /data folder.


After loading into dataframes, The first section in the goes through the dataframes to inspect their shapes, column names, what each row represents and viewing sample rows from the head or tail of each. It ends with combining the `basics_df` and `ratings.df` into `combined_df` as the infomation they contain is highly related for the purposes of our analysis.

## Methods

### Data Preparation
This section presents the process of cleaning the data, alongside the reasoning for decisions in each step.

I use `.sample(5)` to view sample records and `info()` to view info about the columns' data types and number of values 

I find no duplicate rows and continue to create a function `null_percentages(data_frame)` that prints out the number of null values and the percentage as in the below image:




The data analysed came from IMDb website. IMDb (an acronym for Internet Movie Database) is a popular worldwide online database of infomation relating to all movies, television programs, video games and streaming content online. I used 3 files from IMDb to answer the question of which genres were most successful, mainly focusing on the Domestic and Foreign Gross sales along with average ratings given and number of votes received.

After checking the information on each table to see column names and null values, I joined the two datasets, df_titles_basic_info and df_ratings together using the 'tconst' column as it was a unique identifier creating a new dataframe called joinedimdb. I then joined the dataset df_movie_gross with the new dataframe using the title as the unique identifier, creating a combined new dataset called complete_df.

Checking the information on the new dataframe complete_df, I then cleaned up the null values by removing them, tidied up the "Domestic Gross' and 'Foreign Gross' columns and converted them to units of $ millions for easier readability and analysis. The columns"studio", "original title", and the original domestic and foreign gross columns were deleted as they were not required to carry out this analysis.
***

## Methods

The data analysed came from IMDb website. IMDb (an acronym for Internet Movie Database) is a popular worldwide online database of infomation relating to all movies, television programs, video games and streaming content online. I used 3 files from IMDb to answer the question of which genres were most successful, mainly focusing on the Domestic and Foreign Gross sales along with average ratings given and number of votes received.Describe the process for analyzing or modeling the data.

***
After checking the information on each table to see column names and null values, I joined the two datasets, df_titles_basic_info and df_ratings together using the 'tconst' column as it was a unique identifier creating a new dataframe called joinedimdb. I then joined the dataset df_movie_gross with the new dataframe using the title as the unique identifier, creating a combined new dataset called complete_df.

Checking the information on the new dataframe complete_df, I then cleaned up the null values by removing them, tidied up the "Domestic Gross' and 'Foreign Gross' columns and converted them to units of $ millions for easier readability and analysis. The columns"studio", "original title", and the original domestic and foreign gross columns were deleted as they were not required to carry out this analysis.
***

## Results

3 of the above graphs, Domestic Gross Sales, Foreign Gross Sales and Number of Votes clearly show that Adventure, Action and Sci-Fi combination are most successful in Domestic and Foreign Gross Sales and also in the average rating given. Its clear also to see that the adventure genre is popular across the board especially when elements of animation, action and or comedy are also included.

The 4th graph showing Top 20 Average Ratings shows Adventure as top as a solo genre.

To improve confidence in the results next time I would:-

Include the movie classification This could have narrowed down the target audience the most successful movies were aimed at i.e PG etc.

Broken the data into the relevant years to see if there are changes year by year in the top genres of movies, see if audience tastes change over time.



***

***



## Conclusions

This analysis leads to three recommendations regarding types of movies that are successful:-

Movies with the genre combination Action, Adventure & Sci-Fi topped the leaderboard in both Domestic and Foreign Gross Sales, this combination is obviously a hit at the box office worldwide, make this the first type of movie to produce for success.
Movies with Adventure, Animation and Comedy were the next most successful in Foreign Gross Sales and Domestic Sales, use this combination as the next or alternative type of movie to produce.
Movies in the top 20 number of votes yielded slighly different results but Action, Adventure and Sci-Fi combination did come out 1st still.
Adventure genre seems constant in all the above graphs so must be a key element of any movie to be produced.
Questions to consider:

Limitations-Could the same movie be classified into different genres by different audiences? Who classifies the genres for each movie? Can the classification of genres be improved to provide a more benchmark approach?
Future analysis could include the movie classification ie PG, MA etc to see which audience the most successful movies were made for.
***





## Repository Structure

Describe the structure of your repository and its contents, for example:

```
├── README.md                           <- The top-level README for reviewers of this project
├── dsc-phase1-project-template.ipynb   <- Narrative documentation of analysis in Jupyter notebook
├── DS_Project_Presentation.pdf         <- PDF version of project presentation
├── data                                <- Both sourced externally and generated from code
└── images                              <- Both sourced externally and generated from code
```

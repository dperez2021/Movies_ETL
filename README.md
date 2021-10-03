# Movies_ETL

## Project Overview

The purpose of this project was based on a dataset provided by Amazing Prime. The project objective will be to create an automated pipeline that takes in new data from Wikipedia data, Kaggle metadata, and the MoviesLens rating data. It then performs the appropriate transformations and loads the data into an existing PostgreSQL database.

The following steps are used to complete this project:

1. Write an ETL function to read three data files,
2. Extrat and transform the Wikipedia data,
3. Extract and transform the Kaggle and rating data,
4. Load the data to a PostgreSQL Movie Database.

## Resources
CSV: movies_metadata.csv; ratings.csv
JSON: wikipedia-movies.json
Software: Python, Anaconda Navigator, Jupyter Notebook, PostgreSWL, pgAdmin 4.

## Results

-Write an ETL function to read three data files
  -The function takes the Wikipedia JSON, the Kaggle metadata and MovieLens csv files and creates three separate DataFrames.

-Extract and Transform the Wikipedia data
  -We filtered out the TV shows, consolidated the redundant data, removed the duplicates and formatted the Wikipedia data.

-Extract and Transform the Kaggle and rating data
  -Again, we consolidated the redundant data, removed the duplicates, formatted and grouped the data.
  -The Kaggle and rating data were then merged with the Wikipedia movies DataFrame.
  -When creating the databse we run a code that prints out the elapsed time to import each row.
  
  ![ETL_create_database_elapsed_time](https://user-images.githubusercontent.com/88256967/135775358-937997f5-177c-44d6-8b41-3c00c030712b.PNG)

  
-Load the data to a PostgreSWL Movie Database

Below I have run two queries run on the PostgreSQL database that retreives the number of rows for the movies table, and ratings table.

Movies finished with 6,052 rows.

![movies_query_count](https://user-images.githubusercontent.com/88256967/135775307-79d625b9-56f0-4843-b773-35ed95fdc166.PNG)

![movies_query](https://user-images.githubusercontent.com/88256967/135775310-aece49e0-a6bc-4fda-8d31-0ff064d3b096.PNG)

Ratings finished with 26,024,289 rows

![ratings_query](https://user-images.githubusercontent.com/88256967/135775319-b1073e6d-28ea-4683-a882-6eba90a5107e.PNG)

![ratings_query_count](https://user-images.githubusercontent.com/88256967/135775321-1a9c96d2-4e3f-4a12-aa95-0bf73963f69a.PNG)

## Summary

As requested for the Hackathon this completes the project that includes an automated pipeline starting with ETL function that creates, collects, and cleans movie data from different sources. Then it transforms and merges the data to load it into two PostgreSQL dataset tables that are updatable and ready to be used by the hackathon participants.


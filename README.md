# Movies-ETL

## Project Overview

After the initial assignment of getting all the needed data for the Amazing Prime Hackaton, we wanted to create a pipeline that would take the metadata from Wikipedia, Kaggle and MovieLens.

We performed the correct extraction, transformation processes and continued to load the data into a PostgrSQL database. 

These were the followed steps to complete the assignment:
1. Write an ETL function to read and go over three data files
2. Extract and transform the Wikipedia  data
3. Extract and transform the Kaggle data
4. Create a Movie Database in PostreSQL

## Resources
- Data Source:  wikipedia-movies.json, movies_metadata.csv, ratings.csv
- Software: Python 3.7.7, Jupyter Notebook, PostreSQL 11, pgAdmin 4

## Results
### Write an ETL function to read three data files
We took the Wikipedia JSON, and the Kaggle and MovieLens csv files and used a function to create three separate DataFrames.

### Extract and transform Wikipedia data
We filtered out TV shows and got rid of duplicated information to format the data

### Extract and transform Kaggle data
For this analysis we only had to eliminate duplicates and format the data. Once this was completed we merged the result with the Wikipedia DataFrame.

### Create a Movie Database in PostreSQL
We created a connection to the PostreSQL database and added the merged data frame to it.

## Summary
The created functions successfully collected and cleaned the data from the selected sources. The functions also transformed the data to make it ready to upload to PostreSQL. With this, the Hackathon participants will have all the necessary information for their analysis.

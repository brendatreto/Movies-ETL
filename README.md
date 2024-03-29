# Movies-ETL

## Project Overview

After the initial assignment of getting all the needed data for the Amazing Prime Hackaton, we wanted to create a pipeline that would take the metadata from Wikipedia, Kaggle and MovieLens.

We performed the correct extraction, transformation processes and continued to load the data into a PostgreSQL database. 

These were the steps taken to complete the assignment:
1. Write an ETL function to read and go over three data files
2. Extract and transform the Wikipedia data
3. Extract and transform the Kaggle data
4. Create a Movie Database in PostreSQL

## Resources
- Data Source:  wikipedia-movies.json, movies_metadata.csv, ratings.csv
- Software: Python 3.7.7, Jupyter Notebook, PostgreSQL 11, pgAdmin 4

## Results
### Write an ETL function to read three data files
We took the Wikipedia JSON, and the Kaggle and MovieLens csv files and used a function to create three separate DataFrames.

*Fig 1. ETL Function*

![ETL_function](https://user-images.githubusercontent.com/22451540/189238137-63637f10-dcb6-4dc3-9b8a-94c79634baa7.PNG)


### Extract and transform Wikipedia data
We filtered out TV shows and got rid of duplicated information to format the data

*Fig 2. Use ETL function to transform data from Wikipedia*

![clean_wikipedia](https://user-images.githubusercontent.com/22451540/189239957-4020024f-d7b4-41a4-b313-2615cb0ed449.PNG)

*Fig 3. Check DataFrame from Wikipedia data*

![wiki_df](https://user-images.githubusercontent.com/22451540/189240795-d0449a7c-b426-4eff-befa-4b8dcf927f1a.PNG)


### Extract and transform Kaggle data
For this analysis we only had to eliminate duplicates and format the data. Once this was completed, we merged the result with the Wikipedia DataFrame.

*Fig 4. Merge DataFrame with Kaggle ratings*

![Kaggle_df](https://user-images.githubusercontent.com/22451540/189242535-ec43ace9-a11c-48ab-a797-78140d70178d.PNG)


### Create a Movie Database in PostgreSQL
We created a connection to the PostgreSQL database and added the merged data frame to it.

*Fig 5. Connect to PostgreSQL*

![PG_connection](https://user-images.githubusercontent.com/22451540/189242801-00289467-53cd-4377-91b1-3555caae2c07.PNG)


## Summary
The created functions successfully collected and cleaned the data from the selected sources. The functions also transformed the data to make it ready to upload to PostgreSQL. With this, the Hackathon participants will have all the necessary information for their analysis.

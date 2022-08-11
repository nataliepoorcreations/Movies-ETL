# Movies-ETL

## Project Overview
Amazing Prime loves the dataset and wants to keep it updated on a daily basis. Britta needs help to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. We needed to refactor the code from this module to create one function that takes in the three files—Wikipedia data, Kaggle metadata, and the MovieLens rating data—and performs the ETL process by adding the data to a PostgreSQL database.

## Resources
* Software: Postgres, PgAdmin, Python
* Data: movies_metadata.csv, wikipedia-movies.json, ratings.csv

## Deliverable 1: Write an ETL Function to Read Three Data Files
Using knowledge of Python, Pandas, the ETL process, and code refactoring, write a function that reads in the three data files and creates three separate DataFrames.


* The wiki_movies_df DataFrame


![wiki_movies_df DataFrame](https://user-images.githubusercontent.com/106033535/184258534-bcba3077-e728-4740-8317-79ccec857e57.png)


* The kaggle_metadata DataFrame


![kaggle_metadata DataFrame](https://user-images.githubusercontent.com/106033535/184258577-8678a282-30ce-4b70-b820-5a9658214d17.png)


* The ratings DataFrame


![ratings DataFrame](https://user-images.githubusercontent.com/106033535/184258627-76bde677-9da6-40c4-855c-6d5f32df54fb.png)


## Deliverable 2: Extract and Transform the Wikipedia Data
Using knowledge of Python, Pandas, the ETL process, and code refactoring, extract and transform the Wikipedia data to merge it with the Kaggle metadata. While extracting the IMDb IDs using a regular expression string and dropping duplicates, use a try-except block to catch errors.


* The wiki_movies_df DataFrame


![wiki movies df](https://user-images.githubusercontent.com/106033535/184259074-59f20097-03d0-4eb3-bb27-6505207241a5.png)



* The columns from wiki_movies_df DataFrame to a list


![wiki movies column list](https://user-images.githubusercontent.com/106033535/184259086-056d48f5-0546-4a5d-bc2c-0acf961edfc3.png)


## Deliverable 3: Extract and Transform the Kaggle Data
Using knowledge of Python, Pandas, the ETL process, and code refactoring, extract and transform the Kaggle metadata and MovieLens rating data, then convert the transformed data into separate DataFrames. Then, merge the Kaggle metadata DataFrame with the Wikipedia movies DataFrame to create the movies_df DataFrame. Finally, merge the MovieLens rating data DataFrame with the movies_df DataFrame to create the movies_with_ratings_df.


* The movies_with_ratings_df DataFrame


![Screen Shot 2022-08-11 at 7 31 15 PM](https://user-images.githubusercontent.com/106033535/184259372-120d1768-52aa-43ad-99db-3177417f77f1.png)


* The movies_df DataFrame


![Screen Shot 2022-08-11 at 7 31 28 PM](https://user-images.githubusercontent.com/106033535/184259401-edff78ca-5ff4-497d-b702-57e0bee005c5.png)


## Deliverable 4: Create the Movie Database
Use knowledge of Python, Pandas, the ETL process, code refactoring, and PostgreSQL to add the movies_df DataFrame and MovieLens rating CSV data to a SQL database.


* The movies table has 6,052 rows


<img width="884" alt="movies_query" src="https://user-images.githubusercontent.com/106033535/184259584-bef08b0a-b809-4ab7-aa5e-1843d772b809.png">


* the ratings table has 26,024,289 rows


<img width="774" alt="ratings_query" src="https://user-images.githubusercontent.com/106033535/184259603-be63ed2f-ab86-4c0a-9f47-a2050a6c3391.png">





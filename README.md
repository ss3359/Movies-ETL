# Movies-ETL

# Purpose

This is a collection of datasets made by a streaming serivce, Amazing Prime, and trying to update the datasets on a daily basis. The technique to update and refactor the data to create functions that take in three files, and performing a process which adds the data to a Postgres SQL database. This is called Extracting, Transfering, and Loading the data. This is also known as ETL. We have used this process to analyze data presented from movies viewed along with each movies ratings acquired by IMDB. 

# Part One: Write an ETL function to read Three Data Files 

By applying the knowledge of Python, Pandas, code refactoring, and the ETL process, we created a function reading three data files and creating three separate Dataframes. The function is simply called "extract_transform_load()". The code presenting these dataframes are provided in the file "ETL_function_test.ipynb". Here are the dataframes for wiki_movies_df, kaggle_metadata, and for the movie ratings respectively. 

### Fig 1 (wiki_movies_df):

<img width="999" alt="Screen Shot 2022-08-10 at 10 23 47 AM" src="https://user-images.githubusercontent.com/104328106/183962503-e7af3e55-08ee-4f28-a448-5ba852e5e89e.png">

### Fig 2 (kaggle_metadata): 

<img width="977" alt="Screen Shot 2022-08-10 at 10 24 46 AM" src="https://user-images.githubusercontent.com/104328106/183962725-eeec3927-601f-41ff-922d-94f3674325a1.png">


### Fig 3 (ratings): 

<img width="384" alt="Screen Shot 2022-08-10 at 10 25 19 AM" src="https://user-images.githubusercontent.com/104328106/183962842-014b900b-a93a-495a-a132-4b79969e7d77.png">



# Part Two: Extract and Transform the Wikipedia Data

In this section, we have used our Python and Knolwledge, combining with using the ETL process on the Wikipedia data so we are able to merge dataframes with the Kaggle metadata. The catch is, while looking for the IMDB id numbers, we have used a try-catch block to target anf capture errors along the way. The code to conduct this process is under the file "ETL_clean_wiki_movies.ipynb". Here is the merged dataframe for the Wikipedia movies. 

### Fig 4: 
<img width="981" alt="Screen Shot 2022-08-10 at 10 33 38 AM" src="https://user-images.githubusercontent.com/104328106/183964495-b8a4b634-a8ef-482e-90fd-aaed7f51ec40.png">

This is a pretty hefy dataframe. Just to give a persective of the layout of the dataframe, here are the collumns presented in this dataframe. 

### Fig 5: 
<img width="293" alt="Screen Shot 2022-08-10 at 10 36 02 AM" src="https://user-images.githubusercontent.com/104328106/183964937-b87c99ec-2b52-43e4-827d-30b6597d026a.png">

# Part Three: Extract and Transform the Wikipedia Data

In this section, we have used our Python and Knolwledge, combining with using the ETL process on the Kaggle meteadata and the MovieLens ratings data. We then converted the transformed data into sepatate dataframes. The last step is we mergered. the MovieLens ratings Dataframe with the "movies_df" Dataframe to create a new dataframe, called "movies_with_ratings_df". Here are the dataframes for "wiki_movies_df", the mergered "movies_with_ratings_df", and the mergered "movies_df" respectively. The code to execute this process is provided under the file "ETL_clean_kaggle_data.ipynb" 

### Fig 6 (wiki_movies_df): 

<img width="989" alt="Screen Shot 2022-08-10 at 10 55 43 AM" src="https://user-images.githubusercontent.com/104328106/183970866-8bb56a5d-bc37-4e74-b7aa-89903840666e.png">


### Fig 7 (movies_with_ratings_df): 

<img width="977" alt="Screen Shot 2022-08-10 at 10 56 04 AM" src="https://user-images.githubusercontent.com/104328106/183971022-b54ee67e-bad8-4240-b9f8-29955964aeb1.png">


### Fig 8 (movies_df): 

<img width="978" alt="Screen Shot 2022-08-10 at 10 56 29 AM" src="https://user-images.githubusercontent.com/104328106/183971215-257809f5-2fde-4dd8-8165-f2cc2dbb215e.png">


# Part Four: Create the Movie Database

At the last step, we load our mergered data into a Postgres SQL database. From there, we can export that database as a comma separated file (.csv). The code to execute this process is provided under "ETL_create_database.ipynb"
Here are the queries presented for movies_query, and ratings_query respectively. 

### Fig 9 (movies_query) 

<img width="1375" alt="movies_query" src="https://user-images.githubusercontent.com/104328106/183976986-c0297d74-92b7-4d50-815f-ce9fd9edf2e3.png">



### Fig 10 (ratings_query)

<img width="1378" alt="Screen Shot 2022-08-10 at 11 21 31 AM" src="https://user-images.githubusercontent.com/104328106/183977007-a6f2ee9d-1692-4c99-bd5f-47e0923053a4.png">


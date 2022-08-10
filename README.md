# Movies-ETL


# Purpose 

In this project, we use out knowledge of Python, Pandas, and SQL, to use a process called Extract, Transform, and Load the data. This is known as ETL We refactor code to create one function taking in three files-Wikipedia data, Kaggle metadata, and the MovieLens rating data. Finally, we add the data to a PostgresSQL database. 

# Part One: Write an ETL function to Read Three Data Files
Using our knowledge of Python and Pandas, we refactor our code and applying the ETL process by creating a function that reads three data files and makes three separate dataframes. The code to execute this process is provided under the file "ETL_function_test.ipynb". Here are the wiki_movies_df, kaggle_metadata, and the ratings dataframes respectively.

### Figure One (wiki_movies_df): 
<img width="881" alt="Screen Shot 2022-08-10 at 11 37 26 AM" src="https://user-images.githubusercontent.com/104328106/183979473-e6021345-1340-467a-959c-4ba4db0813f8.png">

### Figure Two (kaggle_metadata): 
<img width="874" alt="Screen Shot 2022-08-10 at 11 37 43 AM" src="https://user-images.githubusercontent.com/104328106/183979527-ed3d1c23-5998-41f9-b2c1-fa12e434ce6c.png">

### Figure Three (ratings): 
<img width="336" alt="Screen Shot 2022-08-10 at 11 37 55 AM" src="https://user-images.githubusercontent.com/104328106/183979580-da67c3c0-d711-42ab-9fd9-b5f5585e22a9.png">


# Part Two 
The second step is using our Python, Pandas, the ETL process, and our code refactoring knowledge to extract and transform the Wikipedia data and merge that data with the Kaggle metadata. The catch is extracting the IMDB id's will require droping deplicates. We used a try-catch blocks to handle these errors.  The code to execute this process is provided under the file "ETL_clean_wiki_movies.ipynb". Here is the dataframe representing "wiki_movies_df" with the columns listed included as well. 

### Figure Four: 

<img width="884" alt="Screen Shot 2022-08-10 at 11 44 21 AM" src="https://user-images.githubusercontent.com/104328106/183980738-2dfe27ea-c2f8-4037-b0d7-212bcee8b627.png">


### Figure Five: 

<img width="482" alt="Screen Shot 2022-08-10 at 11 44 47 AM" src="https://user-images.githubusercontent.com/104328106/183980813-c46491a5-fbf8-4a48-9994-86b0984c445e.png">


# Part Three 

The third step is to apply the same techniques in Part Two to extract and transform the Kaggle metadata and the MovieLens rating data
The code to execute this process is provided under the file "ETL_clean_kaggle_data.ipynb".Then, we mergered the MovieLens rating data Dataframe with another dataframe called "movies_df" to create the dataframe "movies_with_ratings_df". Here are the dataframes "wiki_movies_df", "movies_with_ratings", and "movies_df" respectively.  


### Figure Six (wiki_movies_df):

<img width="858" alt="Screen Shot 2022-08-10 at 11 50 45 AM" src="https://user-images.githubusercontent.com/104328106/183982034-4540de8e-0982-4f9a-8d2a-01e4d880533a.png">



### Figure Seven (movies_with_ratings_df): 

<img width="866" alt="Screen Shot 2022-08-10 at 11 51 02 AM" src="https://user-images.githubusercontent.com/104328106/183982093-73c376bf-e6ac-4851-83c2-4a71f85b6691.png">


### Figure Eight (movies_df): 

<img width="864" alt="Screen Shot 2022-08-10 at 11 51 37 AM" src="https://user-images.githubusercontent.com/104328106/183982195-badfc849-45fc-4f4a-ab36-38e50199d093.png">

 
# Part Four 
 The last part is to add the "movies_df" dataframe and MoviesLens ratings CSV file to an SQL database. 
 The code to execute this process is provided under the file "ETL_create_database.ipynb". Here are the queries for "movies_query.png" and "ratings_query.png" respectively 
 
 ### Figure Nine (movies_query.png): 
 <img width="1375" alt="movies_query" src="https://user-images.githubusercontent.com/104328106/183982849-6baed5d9-35be-4994-b4fb-b1474cd7940e.png">

 
 ### Figure Ten (ratings_query.png)
 
 <img width="1378" alt="Screen Shot 2022-08-10 at 11 21 31 AM" src="https://user-images.githubusercontent.com/104328106/183982893-c54503f1-e444-49a0-a1d5-f6965d434345.png">

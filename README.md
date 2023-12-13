# bootcamp-project-2
For this project we used a total of three datasets all of which were found through Kaggle.com.
Our main focus was to look at NFL penalties and see if there was any correlations within the data.
All three datasets were .csv files which were imported using pandas into our jupiter notebook.
After this we made all three datasets into dataframe to make sure they were inputed correctly.
The games dataset is an overview of the penalties for each team thorughout all seasons from 2009-2022.
Our log dataset looked mainly at the instances of which players on each team caused a penalty in each game, and also looked at which referee crew was officiating each game.
The penalty dataset went week by week is an genreral overview of each type of penalty that was called in each game and also listed the amount of each penalty called throughout the week. 

 Our next step was to clean our data into a clear and readable dataframe using only useful columns in our data.
 We used the .loc() function to pull all of our necessary columns for a new dataframe.
 We examined the type of variables to see if any dtypes needed to be changed.
 Our group was using specific dates so we also had to import datetime into our code.
 We ran into an error when trying to change a value in our date column because of negative value that was not consistant with our data.
 First we had to locate our incorrect value in our dataframe by once again using .loc() 
 Then we had to replace the incorrect value 11/30/-0001 into the correct value 11/30/2011.
 This was acomplished by using .replace() to bring in our new value into the dataframe.
 After our error was fixed we made new improved dataframes with our proper data and readable values.
 Lastly for the transforming portion of ETL we turned our dataframe into dictionaries to prepare to bring them into our non-relational database.

 Our final step of our ETL process was to load our transformed data into MongoDB Compass.
 Because of the volume of data in each of our datasets our group thought it would be best to use a non-relational database which is why we choose to use MongoDB.
 Also another reason is the data we are using is getting constantly updated with new stats throughout the current season of the NFL, and if we were to continue using these datasets the task of bringing new data would be simplified.
 After deciding to use MongoDB we had to create a connection to MongoDB and make references to our database and each of our collecitons.
 Then we used the insert_many() function for each of our dataframes to create multiple collections in our database.
 Once our data was loaded into MongoDB we looked at our results using the .find() function and pretty printed our results.


 Sources:
 https://www.kaggle.com/datasets/mattop/nfl-penalties-data-2009-2022-season/data?select=games.csv
 
 
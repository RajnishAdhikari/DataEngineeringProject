Summary of the project
Libraries Used are 
1. Pandas
	It is the library used for data manipulation, analysis and simple mathematical 	calculation.
	
2. Numpy
	It is the library used for mathematical and scientific calculation. In this project
	numpy is just used to replace any missing or NaN value in the 'final_df' dataframe
	with 0.
	
3. Mysql.connector
	It is used create connection with MySQL from python.
	
4. Sqlalchemy
	It is used to provide a set of high-level API to interact with relational database.



Steps and thought process used behind the execution

Step 1: Downloaded messy and large aviation data from kaggle

Step 2: Loaded the csv data into pandas dataframe

Step 3: Data Pre-processing like checking the null value, checking the shape of data, 	 	  
        finding the total number and percentage of null data so that if the null value is 	  
        greater than 20%, then the column was dropped, as the dataset was large, rows with         	  
        the null value was dropped
	
Step 4: With date in column called Flight_Date(FL_DATE), a new column with Year, Quarter, 
	Month was created. For this the data type of FL_DATA was object so it was converted 
	into datetime datatype.
	
Step 5: As the dataset was very large and the system crashed time and again so numbers of rows 	  
        was dropped and reduced to less than 15000.
	
Step 6: Using MySQL Workbench, a database was created in my local system.

Step 7: Using the python script, database was created.

Step 8: Data was loaded into database using python approach and database sql approach. 	 	  
        'df.to_sql()' this parameter was used to insert dataframe into database table.
	
Step 9: Another table with named new_flight_data was created and data was loaded with 	 	  
        previous created data

# csvimport
CSV data import of millions of records using redis


Author : Raju Kumar Yadav
Phone : 
===========================================================================
Task : Importing a large CSV data into database using Laravel version 5.8

Observation : This task can be accomplished by two way
	1. Make the chunks of csv file during upload and process them one by one but this technique is feasible for small size csv  file.
	2. Importing huge csv data : Practically, uploading a huge csv file with millions of rows through form is dificult, as default server settings for handling POST_MAX_SIZE, MAX_EXECUTION_TIME etc will not allow. So, my technique is upload the csv file within a specified directory on the server and process data in the backgroud without any intervention to end users.
	
	I have uploaed the CSV file on this path of server : root_directory/resources/sales_import 
	
	I have implemented redis to handle background process.
  
  SQL file is in root directory.


Server Requirements : 

1. PHP >= 7.1.3 
2. Redis should be installed 

URL : http://localhost/importcsv/


Conclusion : Once the data import will get finished the uploaded csv file will be deleted automatically.

Note : CSV data validation is not done in this script.

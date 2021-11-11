# This is a simple PII detection demo using Snowflake Python UDF 

Many times we have to search through rows of text data to identify personal identifiable information (PII). It is to make sure that developers don't misuse this information and create a secure and governed data platform.

# How to use this code

1. First step is to setup the demo database, schema and table. You can use any database and schema. The hasPIICheck.sql contains all the code necessary to create the table and file format to load the csv file that contains 100K tweets
2. Once the data is loaded using either snowsql or direct UI upload into tweets table, you are ready to setup the UDF
3. Create the UDF using the code provided in the SQL file. It uses regular expression to find the PII. Code has a list of such regex elements like phone, ssn and email. This can be extended with more
4. First time run (cold load/run) takles about 40s on small warehouse
5. use the select statement to demo the UDF functionality

tags - #snoparkUDF #PythonUDF

Slack us at #feat-Python-UDFs for any issues or comment
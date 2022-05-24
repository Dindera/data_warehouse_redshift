
## Sparkify Data Warehouse Redshift - DE Nanodegree Project




The purpose of this project is to develop a data warehouse on AWS Redshift. The data warehouse is built by creating a Redshift cluster which can be connected with using the IAM role, cluster credentials and access keys. The two datasets are first loaded into the staging tables from the S3 bucket. Data from the staging tables are then transformed and inserted into the fact and dimension tables respectively. The database is modelled based on Kimball's dimensional modelling and it includes the fact table songplays, the dimension tables songs, users, artists and time. 




### Summary of files

###### sql_queries.py

* Includes variables for accessing the S3 bucket.
* Initially drops tables if exists.
* Contains queries for creating, copying, transforming and inserting data into the tables.

###### create_tables.py

* Imports the create_table and drop_table queries from sql_queries.py file.
* Connects to the data warehouse cluster.
* Executes the drop_table and create_table functions to drop and create tables in the database.

###### etl.py

* Imports the copy_table and insert_table queries from sql_queries.py file.
* Connects to the data warehouse cluster using the cluster details, IAM role and S3 access.
* Executes the copy_table and insert_table queries to copy into staging tables, transform and insert into fact and dimension tables in the database. 

###### dwh.cfg

* Contains environment variable for the cluster details, IAM role and S3 access. 
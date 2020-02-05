# Summary
This project was designed to walk us through the ETL process from start to finish by extracting data from json files and inserting them into different tables for query optimization. The purpose was to create a star schema optimized for queries on song play. The schema was separated into Fact tables (songplays) and Dimension tables (users, songs, artists, time). 

# Instructions
Please run all cells in test.ipynb in order to see working ETL process.

# File Explanations
- Data folder contains log_data and song_data folders and within these folders contain the raw json files we need to extract data from.

- The etl.ipynb jupyter notebook was designed to provide a step by step process on how we should be extracting the data from the json files using pandas. The queries in there are not deisnged to loop through each json file. Please refer to etl.py.

- The create_tables.py is a python file that will create a connection to sparkify database and imports from sql_queries.py in order to create/drop the tables. sql_queries.py contains several CREATE/INSERT statements to help us 1. create the empty tables 2. insert data we extract from json into the tables.

- etl.py is the main python file that contains many of the core functions developed from etl.ipynb but will loop through each of the json files in the data folder to extract all the data and populate the tables. 

- test.ipynb is a jupyter noteboook we use to run the python files (create_tables.py and etl.py) and then we run a series of SQL statements to make sure that our ETL processed work and data was extracted and loaded. To run the python files we simply do "!python python_file" within jupyter notebook and execute it in one of the cells.


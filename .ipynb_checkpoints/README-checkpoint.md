## Data Modelling with Postgre

The point of this project is to create a relational database (Postgre)
for a fictional music application called Sparkify. 

The database models music and logging datasets with a star schema optimised for queries on analysis of user listening behaviour.

### Data Schema

Fact Table

songplays - records in log data associated with song plays i.e. records with page NextSong
    songplay_id, start_time, user_id, level, song_id, artist_id,
    session_id, location, user_agent


Dimension Tables

users - users in the app
    user_id, first_name, last_name, gender, level

songs - songs in music database
    song_id, title, artist_id, year, duration

artists - artists in music database
    artist_id, name, location, latitude, longitude

time - timestamps of records in songplays 
    start_time, hour, day, week, month, year, weekday


### How to run 

1. run create_tables.py from the terminal to create the database wit
    the empty tables. 

2. to confirm the existence of your tables run test.ipynb. 

3. run etl.py with terminal to insert all records from song_data and
    log_data into tables. 

4. run test.ipynb to confirm your records were properly inserted into
    the correct table.
    
### Files

* create_tables.py: create the tables (or override them if the already
    exist)

* test.ipynb: for sanity checks of the tables and the data

* etl.ipynb: to understand etl.py 

* etl.py: reads the and parses the files in the data folder and inserts
    them into the right tables 

* sql_queries.py: helper file that contains all necessary SQL
    statements
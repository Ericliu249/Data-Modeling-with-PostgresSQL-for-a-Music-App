# Sparkify

## Backgroud

A startup called Sparkify wanted to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team were particularly interested in understanding what songs users are listening to. However, they did't have an easy way to query their data, which resided in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

## Objective

As a data engineer, my role is to create a Postgres database with tables designed to optimize queries on song play analysis. My tasks included creating a database schema and ETL pipeline for this analysis as well as testing the database and ETL pipeline by running queries given to me by the analytics team from Sparkify and comparing the results with their expected results.

## Dependencies

- psycopg2
- Python 3.5+
- pandas
- os
- glob

## Data Sources

### Song Dataset

The first dataset is a subset of real data from the [Million Song Dataset](http://millionsongdataset.com/). Each file is in JSON format and contains metadata about a song and the artist of that song. The files are partitioned by the first three letters of each song's track ID. For example, here are filepaths to two files in this dataset.

- song_data/A/B/C/TRABCEI128F424C983.json
- song_data/A/A/B/TRAABJL12903CDCF1A.json

And below is an example of what a single song file, TRAABJL12903CDCF1A.json, looks like.

{"num_songs": 1, "artist_id": "ARJIE2Y1187B994AB7", "artist_latitude": null, "artist_longitude": null, "artist_location": "", "artist_name": "Line Renaud", "song_id": "SOUPIRU12A6D4FA1E1", "title": "Der Kleine Dompfaff", "duration": 152.92036, "year": 0}

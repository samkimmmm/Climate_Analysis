# sqlalchemy-challenge - Module 10 Challenge

# Overview
In this challenge, I conducted a climate analysis and data exploration of Honolulu, Hawaii using Python and SQLAlchemy.

# Technologies
* Python
* SQLAlchemy
* Pandas
* Matplotlib
* Numpy
  
# Part 1: Analyze and Explore the Climate Data
After successfuly connecting to the SQLite Database and reflecting my tables into classes, I linked Python to the database be creating a SQLAlchemy session.
<img width="475" alt="Screenshot 2023-12-18 at 3 05 11 PM" src="https://github.com/samkimmmm/sqlalchemy-challenge/assets/135805393/1360741f-fe03-4f37-bd55-e3ebaa235def">

# Precipitation Analysis
Using the most recent date in the dataset, retrieve the previous 12 months of precipitation data, select only the "date" and "prcp" values, then plot the results using the .plot() method.
<img width="758" alt="Screenshot 2023-12-18 at 3 07 09 PM" src="https://github.com/samkimmmm/sqlalchemy-challenge/assets/135805393/fd178cbe-c59c-4c89-9ad1-9d50f653db8e">

# Station Analysis
Design 4 queries:
1. Total number of stations in the dataset.
<img width="565" alt="Screenshot 2023-12-18 at 3 11 04 PM" src="https://github.com/samkimmmm/sqlalchemy-challenge/assets/135805393/0107b988-1a48-4cee-9eda-c8cb2ae9af5b">
2. Most active stations (most rows), then find the station id that has the greatest number of observations.
<img width="690" alt="Screenshot 2023-12-18 at 3 11 29 PM" src="https://github.com/samkimmmm/sqlalchemy-challenge/assets/135805393/f1ec7efb-1e07-4513-a4c9-98e279764906">
3. Calculation of the lowest, highest, and average temperatures that filters on the most active station id.
<img width="871" alt="Screenshot 2023-12-18 at 3 12 01 PM" src="https://github.com/samkimmmm/sqlalchemy-challenge/assets/135805393/ec9bdfc8-c049-4668-8bb5-f81aa21efa27">
4. Previous 12 months of temperature observations of the most active station's id, then plot the results in a histogram.
<img width="850" alt="Screenshot 2023-12-18 at 3 12 17 PM" src="https://github.com/samkimmmm/sqlalchemy-challenge/assets/135805393/5bef720b-d536-400d-bf38-aa23a871d0fe">

# Part 2: Design your Climate Map
Design a Flask api based on the queries I had developed. The following routes are as follows:
1. "/": Homepage that lists all of the available routes.
2. "/api/v1.0/precipitation": Convert the "date" as the key" and "prcp" as the value, and return the JSON representation of the dictionary.
3. "/api/v1.0/stations": Return a JSON list of stations from the dataset.
4. "/api/v1.0/tobs": JSON list of the temperature observations of the most active station for the previous year.
5. "api/v1.0/<start>" and "/api.v1.0/<start>/<end>": Return a JSON list of the minimum, average, and maximum temperatures for a specified start or start-end range. 

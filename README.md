# Climate Analysis and Flask API Project
Analyze and explore climate data using SQLAlchemy with a climate database, followed by designing a Climate App


## Overview
This project is focused on analyzing climate data in Honolulu, Hawaii, using a SQLite database and building a Flask API based on the results of the data analysis. The project is divided into two main parts:

### 1. Climate Data Analysis:
Utilizing SQLAlchemy ORM, Pandas, and Matplotlib to perform data analysis and visualization on the climate data.
### 2. Flask API Creation:
Building a RESTful API with Flask based on the data queries and analysis.
   
## Project Structure
Resources/hawaii.sqlite: The SQLite database containing the climate data.
climate_starter.ipynb: Jupyter Notebook used for the initial data analysis and exploration.
app.py: Python script containing the Flask API.
README.md: Project documentation (this file).

## Part 1: Climate Data Analysis
### Steps
1. Database Setup and Connection:
Used SQLAlchemy's create_engine() to connect to hawaii.sqlite.
Reflected the database schema using automap_base() and created references to Measurement and Station tables.
Created a session to interact with the database.

2. Precipitation Analysis
Queried the last 12 months of precipitation data.
Loaded the data into a Pandas DataFrame.
Sorted the data by date and visualized it using Matplotlib.

3. Station Analysis
Calculated the total number of stations in the dataset.
Identified the most active station (station with the most observations).
Queried the minimum, maximum, and average temperatures for the most active station.
Queried the last 12 months of temperature data for the most active station and plotted the results as a histogram.

4. Summary Statistics
Printed summary statistics for the precipitation data using Pandas.

## Part 2: Flask API Creation
Routes
1. /
Description: Homepage listing all available routes.
Output: A list of routes with brief descriptions.
2. /api/v1.0/precipitation
Description: Returns a JSON representation of the last 12 months of precipitation data.
Output: A dictionary where the date is the key and the precipitation value is the value.
3. /api/v1.0/stations
Description: Returns a JSON list of all stations in the dataset.
4. /api/v1.0/tobs
Description: Returns a JSON list of temperature observations (TOBS) for the last year from the most active station.
5. /api/v1.0/<start>
Description: Returns the minimum, average, and maximum temperature for all dates greater than or equal to the specified start date.
6. /api/v1.0/<start>/<end>
Description: Returns the minimum, average, and maximum temperature for the dates between the specified start and end dates.

## Example Usage
-Visit the homepage at http://127.0.0.1:5000/ to see available routes.
-Query precipitation data: http://127.0.0.1:5000/api/v1.0/precipitation
-Query station data: http://127.0.0.1:5000/api/v1.0/stations

### Setup and Installation
Clone the repository: git clone 
Install the required packages: pip install flask sqlalchemy pandas matplotlib
Start the Flask application: python app.py
Open a web browser and navigate to http://127.0.0.1:5000/ to access the API.

## Requirements Met
### Part 1: Climate Analysis
Connected to SQLite database using SQLAlchemy.
Used SQLAlchemy ORM to reflect tables and created database references.
Completed precipitation and station analysis using SQLAlchemy queries and visualized the data using Pandas and Matplotlib.

### Part 2: Flask API
Created a Flask API with the specified routes.
Used SQLAlchemy queries to retrieve data and returned results in JSON format using Flask's jsonify() function.



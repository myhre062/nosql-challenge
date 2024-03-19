# nosql-challenge

# Module 12

## Overview
The UK Food Standards Agency evaluates various establishments across the United Kingdom and assigns them a food hygiene rating. This project involves analyzing the ratings data to assist the editors of a food magazine, Eat Safe, Love, in focusing future articles. MongoDB is used as the database to store the establishments' information.

## Part 1: Database and Jupyter Notebook Set Up

### Importing Data
To import the data provided in the [establishments.json](https://github.com/myhre062/nosql-challenge/blob/main/Resources/establishments.json) file in the `Resources` folder into the MongoDB database, run the following command in your Terminal once you have navigated to the `Resources` folder: `mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json`


### Notebook Set Up
In the Jupyter Notebook [NoSQL_setup_starter.ipynb](https://github.com/myhre062/nosql-challenge/blob/main/NoSQL_setup_starter.ipynb), the following steps are performed:

1. Importing necessary dependencies such as `MongoClient` from `pymongo` and `pprint`.
2. Creating an instance of `MongoClient`.
3. Confirming the creation of the new database and reviewing its collections.

## Part 2: Update the Database

1. Adding a new restaurant, "Penang Flavours", to the database.
2. Finding the `BusinessTypeID` for "Restaurant/Cafe/Canteen" and updating the new restaurant with the correct `BusinessTypeID`.
3. Removing any establishments within the Dover Local Authority from the database.
4. Converting the data type of `latitude`, `longitude`, and `RatingValue` fields.
   
## Part 3: Exploratory Analysis

### Notebook Set Up
In the Jupyter Notebook [NoSQL_analysis_starter.ipynb](https://github.com/myhre062/nosql-challenge/blob/main/NoSQL_analysis_starter.ipynb), the following steps are performed:

1. Importing necessary dependencies such as `MongoClient`, `pandas`, and `pprint`.
2. Creating an instance of `MongoClient`.
3. Accessing the `uk_food` database and its `establishments` collection.

### Exploratory Analysis
The notebook conducts an exploratory analysis by addressing the following questions:

1. Which establishments have a hygiene score equal to 20?
2. Which establishments in London have a `RatingValue` greater than or equal to 4?
3. What are the top 5 establishments with a `RatingValue` of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
4. How many establishments in each Local Authority area have a hygiene score of 0?

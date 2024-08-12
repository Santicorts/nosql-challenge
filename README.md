# nosql-challenge



## Project Overview

The UK Food Standards Agency evaluates various establishments across the United Kingdom, giving them food hygiene ratings. You've been contracted by the editors of a food magazine, *Eat Safe, Love*, to evaluate some of the ratings data to help their journalists and food critics decide where to focus future articles.

In this project, you'll set up a MongoDB database, update and clean the data, and perform exploratory analysis to answer key questions posed by the magazine editors.

## Table of Contents

1. [Before You Begin](#before-you-begin)
2. [Files](#files)
3. [Instructions](#instructions)
   - [Part 1: Database and Jupyter Notebook Setup](#part-1-database-and-jupyter-notebook-setup)
   - [Part 2: Update the Database](#part-2-update-the-database)
   - [Part 3: Exploratory Analysis](#part-3-exploratory-analysis)
4. [Results](#results)
5. [Conclusion](#conclusion)

## Before You Begin

1. Create a new repository for this project called `nosql-challenge`. 
2. Clone the repository to your computer.
3. Add your Jupyter notebook starter files and your `Resources` folder containing `establishments.json` to this folder.
4. Push the changes to GitHub.

## Files

The following files are included in this project:

- `NoSQL_setup_starter.ipynb`: Jupyter notebook for database setup and data insertion.
- `NoSQL_analysis_starter.ipynb`: Jupyter notebook for performing exploratory analysis.
- `Resources/establishments.json`: The dataset containing information about various food establishments across the UK.

## Instructions

### Part 1: Database and Jupyter Notebook Setup

1. **Import Data**: 
   - Import the data from `establishments.json` using the MongoDB shell or `mongorestore`.
   - Name the database `uk_food` and the collection `establishments`.
   - Copy the terminal command used to import the data into a markdown cell in `NoSQL_setup_starter.ipynb`.

2. **Set Up MongoDB in Jupyter**:
   - Import the necessary libraries: `PyMongo` and `pprint`.
   - Create an instance of the Mongo Client.
   - Verify that the database and collection were created successfully.
   - Display one document from the `establishments` collection.

### Part 2: Update the Database

The magazine editors have requested the following modifications:

1. **Add New Restaurant**:
   - Add a new halal restaurant, "Penang Flavours", located in Greenwich, to the database. This restaurant hasn't been rated yet.

2. **Update BusinessTypeID**:
   - Find the `BusinessTypeID` for "Restaurant/Cafe/Canteen" and update the new restaurant with this `BusinessTypeID`.

3. **Remove Dover Establishments**:
   - The magazine is not interested in any establishments within the Dover Local Authority.
   - Count how many documents contain the Dover Local Authority and remove them from the database.

4. **Convert Data Types**:
   - Convert the `latitude` and `longitude` fields to decimal numbers.
   - Convert the `RatingValue` field to integers where applicable.

### Part 3: Exploratory Analysis

Use the data to answer specific questions for the magazine:

1. **Hygiene Score of 20**:
   - Find and display establishments with a hygiene score of 20.

2. **London Establishments with High Rating**:
   - Find establishments in London with a `RatingValue` greater than or equal to 4.

3. **Top 5 Establishments Near "Penang Flavours"**:
   - Find the top 5 establishments with a `RatingValue` of 5, sorted by the lowest hygiene score, closest to "Penang Flavours".

4. **Hygiene Score of 0 by Local Authority**:
   - Count how many establishments in each Local Authority area have a hygiene score of 0, and sort the results from highest to lowest.

## Results

- The database has been successfully set up, and data has been imported.
- Various updates and cleaning operations were performed as requested by the magazine editors.
- Exploratory analysis was conducted to provide insights based on the food hygiene ratings.

## Conclusion

This project provided valuable insights into the food hygiene standards of various establishments across the UK. The data can now be used by *Eat Safe, Love* to guide their editorial decisions and focus on areas of interest.

---

This README file provides a comprehensive overview of the project, instructions for setting up the database, performing updates, and conducting analysis, as well as a summary of the results and conclusions.
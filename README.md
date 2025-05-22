# Game Recommendation System using SQL and Machine Learning on Databricks

## Overview

This project implements a personalized game recommendation system using a hybrid approach that combines SQL for data preprocessing and Spark MLlib for building a collaborative filtering model. The work was conducted on the Databricks platform and exported as a `.ipynb` notebook (`Task2`).

## Task 2: Recommendation System Development

### Objectives

- Analyze Steam user-game interaction data
- Build a scalable, collaborative filtering model for recommending games
- Use SQL for data exploration and feature preparation
- Apply Spark MLlib’s ALS model using Python

### Dataset

- Source: Steam interactions (200,000+ records)
- Fields: `user_id`, `game`, `event_type`, `play_hours`, `purchase_flag`
- Format: CSV, loaded into Databricks for analysis

### Tools and Technologies

- **Platform**: Databricks
- **Languages**: SQL & Python
- **Libraries**: PySpark, Spark SQL, Spark MLlib

## Project Workflow

1. **Data Ingestion**
   - Load CSV data into Spark DataFrame
   - Infer schema and clean null or invalid values

2. **Data Preprocessing (SQL)**
   - Normalize game names
   - Filter and encode user interactions
   - Assign interaction weights using SQL logic

3. **Feature Engineering (Python)**
   - Encode categorical columns using `StringIndexer`
   - Create feature vectors using `VectorAssembler`
   - Train-test split

4. **Model Training**
   - Use ALS (Alternating Least Squares) from MLlib
   - Tune model hyperparameters (e.g., rank, regularization)
   - Fit model on training data

5. **Evaluation & Recommendation**
   - Evaluate using RMSE
   - Generate top-N recommendations for each user

## Running the Project

> This notebook is best run on [Databricks Community Edition](https://community.cloud.databricks.com/).

### Steps:
1. Upload the notebook `00787835_Task2.html`
2. Attach to a Spark cluster
3. Run cells in sequence

## Output

- User-specific game recommendations
- ALS model performance metrics (e.g., RMSE)
- SQL transformation and cleaning steps logged in notebook

## File Structure


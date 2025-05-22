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
  <img width="1201" alt="Screenshot 2025-05-22 at 16 12 01" src="https://github.com/user-attachments/assets/9289efac-5af5-441a-b806-1fc02c2b665c" />

   

2. **Data Preprocessing (SQL)**
   - Normalize game names
   - Filter and encode user interactions
   - Assign interaction weights using SQL logic
     <img width="1206" alt="Screenshot 2025-05-22 at 16 12 19" src="https://github.com/user-attachments/assets/46e0ff48-44ef-4b22-95c1-0eac55c0ad47" />


3. **Feature Engineering (Python)**
   - Encode categorical columns using `StringIndexer`
   - Create feature vectors using `VectorAssembler`
   - Train-test split
<img width="1297" alt="Screenshot 2025-05-22 at 16 12 46" src="https://github.com/user-attachments/assets/e99f1d87-d4ef-46a6-92bc-ef58c4f92f4b" />


4. **Model Training**
   - Use ALS (Alternating Least Squares) from MLlib
   - Tune model hyperparameters (e.g., rank, regularization)
   - Fit model on training data
<img width="1260" alt="Screenshot 2025-05-22 at 16 13 11" src="https://github.com/user-attachments/assets/f06d3f38-d87f-43a9-9ea9-d9bcbbfc76c2" />

5. **Evaluation & Recommendation**
   - Evaluate using RMSE
   - Generate top-N recommendations for each user
   - <img width="1192" alt="Screenshot 2025-05-22 at 16 13 43" src="https://github.com/user-attachments/assets/d1cb3728-9bba-409d-bbd3-de92b3d2c61e" />

![Uploading Screenshot 2025-05-22 at 16.14.34.png…]()

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


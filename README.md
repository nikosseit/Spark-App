# Spark ETL Application

## Overview
This project is a scalable ETL (Extract, Transform, Load) pipeline built using Apache Spark. It ingests, processes, and integrates data from multiple sources into a structured database and Parquet format for downstream analytics and reporting.

## Key Features
- **Data Ingestion**: Reads raw data from two CSV files (`subscribers` and `transactions`).
- **Data Transformation**: 
  - Cleanses and standardizes data for consistency.
  - Joins datasets using `subscriber_id` as the common key.
  - Derives additional attributes such as unique keys and formatted dates.
- **Data Loading**: 
  - Loads cleansed subscriber data into a relational database (e.g., SQLite).
  - Persists the final processed dataset in a Parquet format for efficient querying and analysis.

## Pipeline Architecture
1. **Extract**: Load raw CSV files into Spark DataFrames.
2. **Transform**:
   - Cleanse missing or invalid records.
   - Enrich data with derived columns and proper formatting.
   - Perform a join operation to create a unified dataset.
3. **Load**:
   - Store intermediate data in a relational database.
   - Save the final dataset as a Parquet file for optimized storage and analytics.

## Technologies and Tools
- **Apache Spark**: Distributed data processing engine for ETL workflows.
- **SQLite**: Lightweight relational database for intermediate storage.
- **Parquet**: Columnar file format for efficient storage and analytics.
- **Python**: Orchestrates the ETL pipeline.

## Prerequisites
- Python 3.x
- Apache Spark
- SQLite or a compatible database
- pip install pyspark==3.4.1 sqlite3 pandas==1.5.3 pyodbc==4.0.35


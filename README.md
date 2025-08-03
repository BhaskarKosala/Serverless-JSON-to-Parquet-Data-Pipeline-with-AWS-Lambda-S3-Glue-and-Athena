# Serverless-JSON-to-Parquet-Data-Pipeline-with-AWS-Lambda-S3-Glue-and-Athena

This project demonstrates a fully serverless, scalable data pipeline built with AWS services to automate the ingestion, transformation, storage, and querying of semi-structured JSON data.

## 🚀 Overview

- **Goal:** Convert incoming JSON files into Parquet format, catalog the data using AWS Glue, and enable analysis using AWS Athena.
- **Architecture:** Serverless pipeline using AWS Lambda, S3, Glue, and Athena.
- **Automation:** Triggers and processes new files automatically with timestamp-based versioning.

# AWS Serverless End-to-End ETL Pipeline

![image alt](https://github.com/BhaskarKosala/Serverless-JSON-to-Parquet-Data-Pipeline-with-AWS-Lambda-S3-Glue-and-Athena/blob/7cc2d2f681e6600889765a586090473fc74fb157/aws%20pipeline.jpg)


## 🧱 Components & Flow

1. **Jupyter Notebook**  
   - Loaded a complex JSON file.
   - Transformed it into a tabular structure using `pandas`.

2. **AWS S3**  
   - Uploaded the JSON file into a designated S3 bucket.
   - Organized transformed data and Parquet outputs in separate folders.

3. **AWS Lambda (ETL Trigger)**  
   - Triggered automatically on S3 file upload.
   - Flattened nested JSON and converted it to a `DataFrame`.
   - Transformed and saved as `.parquet` using Python’s `io` and `pandas`.

4. **AWS Glue**  
   - Created a **Glue database** and a **crawler** to catalog Parquet files.
   - Automatically inferred schema and registered it in Glue Data Catalog.

5. **AWS Athena**  
   - Queried Parquet data using SQL.
   - Verified schema and performed analytics without moving data.

6. **AWS Lambda (Automation)**  
   - Second Lambda function for auto-processing of newly added JSON files.
   - Used `boto3` and `datetime` to prefix files with timestamps and trigger pipeline automatically.

## 📊 Technologies Used

- **Python** – Data transformation and file handling.
- **Pandas** – JSON to tabular structure.
- **AWS S3** – Storage layer.
- **AWS Lambda** – Serverless compute for transformation and automation.
- **AWS Glue** – Schema inference and cataloging.
- **AWS Athena** – Serverless querying of Parquet files.
- **Boto3** – AWS SDK for Python automation.


## 🧪 Demo & Results

- Successfully cataloged and queried multi-record nested JSON data.
- Enabled real-time ingestion and query using a 100% serverless architecture.
- Improved efficiency using Parquet storage over JSON.
- Scalable and cost-efficient for future data loads.

# Youtube Data Analysis

## Project Overview
This project is designed to process and analyze YouTube data using AWS services. It involves data extraction, transformation, and loading (ETL) processes primarily executed through AWS Lambda, AWS Glue, and S3.

## Architecture
The project leverages several AWS services:
- **AWS Lambda**: Used for processing JSON data files uploaded to S3.
- **AWS Glue**: Utilized for ETL operations on YouTube data, transforming it into a structured format.
- **Amazon S3**: Serves as the storage layer for raw and processed data.

## Setup Instructions
1. **AWS Configuration**: Ensure your AWS CLI is configured with the necessary permissions to access S3, Lambda, and Glue.
2. **Environment Variables**: Set the following environment variables for the Lambda function:
   - `s3_cleansed_layer`
   - `glue_catalog_db_name`
   - `glue_catalog_table_name`
   - `write_data_operation`
3. **Data Upload**: Use the `s3_cli_command.sh` script to upload data to the specified S3 bucket.

## File Descriptions
- **lambda_function.py**: Contains the AWS Lambda function code for processing JSON files from S3 and writing the output to another S3 location in Parquet format.
- **pyspark_code.py**: A PySpark script executed in AWS Glue for transforming YouTube data and writing it back to S3.
- **s3_cli_command.sh**: A shell script for uploading JSON and CSV files to the S3 bucket.
- **YOUTUBE DATA ANALYSIS.pdf**: A document providing detailed analysis and insights into the YouTube data.
- **YOUTUBE DATA ANALYSIS-2.pptx**: A presentation summarizing the project's findings and methodologies.

## Usage
- **Lambda Function**: Triggered by S3 events when a new JSON file is uploaded.
- **Glue Job**: Run the PySpark script to process and transform data stored in S3.

## Additional Resources
For more detailed information, refer to the `YOUTUBE DATA ANALYSIS.pdf` and `YOUTUBE DATA ANALYSIS-2.pptx` files included in the project.

Final PowerBI Analysis:

<img width="1405" alt="Screenshot 2025-04-30 at 10 03 00 PM" src="https://github.com/user-attachments/assets/84e5d475-498f-4e0e-9c16-07596a1e7057" />

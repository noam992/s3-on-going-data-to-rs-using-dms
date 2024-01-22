# s3-on-going-data-rs
This repository contains code for handling ongoing data changes in an on-premise SQL database using AWS services. The primary components are AWS Lambda Function, AWS DMS, and AWS CodeBuild.

## Technology

- AWS Lambda Function
- AWS DMS (Database Migration Service)
- AWS CodeBuild

### AWS Lambda Function

The Lambda Function provided in this repository is designed to handle changes in the source database, which is an on-premise SQL database. AWS DMS (Database Migration Service) is utilized as a Change Data Capture (CDC) service, allowing the migration of data from one source to another. The Lambda Function processes the CDC records and inserts them into an S3 bucket. The CDC modes include:

- I - Insert
- U - Update
- D - Delete

### AWS CodeBuild

AWS CodeBuild is employed to upload the Lambda Function to the AWS platform. It is an AWS service that streamlines the process of building and deploying code. CodeBuild handles the uploading of code to AWS and installs the necessary dependencies from the `requirements.txt` file.

## Usage

1. Ensure you have the required AWS services set up, including Lambda, DMS, and CodeBuild.
2. Configure the Lambda Function to operate with the desired on-premise SQL database.
3. Utilize CodeBuild to upload the Lambda Function code to the AWS platform.

# Spotify End-To-End ETL Data Engineering Project

### Introduction
In this project we will build and ETL(Extract, Trnsform, Load)Pipeline using the Spotify API on AWS. The pipeline will retrive data from the spotify API, transform it accroding to the required format, and load it into the AWS data store

### About Dataset/API
This API contains information about music artist, albums and songs - (https://developer.spotify.com/documentation/)

### Services Used
1. **S3 (Simple Storage Service):** Amazon S3 (Simple Storage Service) is a highly sclabale object storage service that can store and retrive any amount of data from anywhere on web. It is commonly used to store and distribute large media files, data backups, static web files.

2. **AWS Lambda:** AWS Lambda is a Serverless computing service that lets you run your code without managing servers. You can use Lambda to run code in response to events like changes in S3, DynamoDB, or other AWS Services.

3. **Cloud Watch:** Amazon CloudWatch is a monintering services for AWS resources abd the applications you run on them, you can use cloudwatch t track metrics, collect and moniter log files, and set alarms.

4. **Glue Crawler:** AWS Glue Crawler is a fully managed service that automatically crawls your data sources,identifies data formats, and infers schemas to create AWS Glue Data Catalog

5. **Data Catalog:** AWS Glue Data Catalog is a fully managed metadata repository that makes it easy to discover and manage data in AWS. You can use the Glue Data Catalog with other AWS Services such as athena.

6. **Amazon Athena:** Amazon Athena is an interactive query service that makes it easy to analyse data in amazon S# using standard SQL. You can use Athena to analyze data in your Glue Catalog or in any other S# Buckets

###Install Packages
```
pip install pandas
pip install numpy
pip install spotipy
```

###Project Execution Flow
Extract Data from API -> Lamda Trigger (every 1 hour) ->  Run Extract Code-> Store Raw Data -> Trigger Data Transformation Function -> Trannsform Data and Load It -> Quering the transformed data using Athena

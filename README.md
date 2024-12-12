<p align="center"><strong>Project 1: Contact Center Metrics</strong></p>

# Descriptive Analysis

## Project Description:
Descriptive Analysis of Contact Center metrics of the City of Vancouver.

## Project Title:
Understanding Contact Center Metrics of the City of Vancouver.

## Objective:
This project's main objective is to provide a descriptive analysis of a Vancouver contact center's monthly call stats. The study aims to highlight important aspects of monthly calls, spot patterns, and generate insights that might enhance resource allocation and customer service operations.

## Dataset:
The dataset includes contact center data from the City of Vancouver over the past year, containing the following key features:
- **Date**: Date of the call.
- **Calls Offered**: Number of calls received by day.
- **Calls Handled**: Number of calls handled in a day.
- **Calls Abandoned**: Number of calls abandoned in a day.
- **Average Speed of Answer**: Average speed it took to answer each call for the day.
- **Service Level**: Ratings given by each caller.
- **BI_ID**: Unique identifier for each caller.

## Methodology:
1. **Data Collection and Preparation**:
   - Data has been extracted from [Vancouver Open Data Portal](https://opendata.vancouver.ca/explore/dataset/3-1-1-contact-centre-metrics/information/).
   - Data has been prepared using Microsoft Excel.

2. **Descriptive Statistics**:
   - Calculated the average number of calls handled each month.

3. **Workflow**:
   - **Data Ingestion**:
     - Uploaded the data into the Standard S3 storage class for frequent access.
     - Directory path for raw data: `Amazon S3/Buckets/raw-data`.

   - **Data Profiling**:
     - Created a new bucket: `grp1-ccm-trf-cha` for storing transformed data.
     - Path: `Amazon S3/Buckets/grp1-ccm-trf-cha/data_profiling/`.
     - Used AWS Glue DataBrew to preview the dataset.

   - **Data Cleaning**:
     - Created folders for system and user data in S3.
     - Path: `Amazon S3/Buckets/grp1-ccm-trf-cha/data_cleaning/`.
     - Renamed non-standard columns, extracted months from the date column, and deleted the date column for monthly analysis.

   - **Data Pipeline Design**:
     - Created a visual ETL job: `grp1-ccm-etl-cha`.
     - Dropped unnecessary columns, filtered data by months, and calculated the average for each month.

## Insights and Findings:
- **Average Calls by Month**:
  - January: 1241
  - February: 983
  - March: 823
  - April: 955
  - May: 1007
  - June: 1073
  - July: 1059
  - August: 903
  - September: 818
  - October: 865

## Recommendations:
- Optimize Resource Allocation.
- Focus on Service Level Improvements.
- Enhance Call Abandonment Management.
- Evaluate Training and Performance.
- Data-Driven Decision Making.
- Regular Metrics Review.
- Continuous Process Improvement.

## Tools and Technologies:
- **Amazon AWS**:
  - AWS S3
  - AWS Glue
  - AWS Glue DataBrew
  - AWS CloudWatch
  - AWS CloudTrail
- **Other Tools**:
  - Microsoft Excel (data collection).
  - Draw.io (visualization).

---

<p align="center"><strong>Project 2: Data Quality Control</strong></p>

## Project Description:
Data Quality Control Initiative at University Canada West Registrar's Office.

## Project Title:
Implementation of Data Quality Control Measures at University Canada West Registrar's Office.

## Objective:
This project aims to establish consistent and reliable systems for data storage and stewardship at University Canada West (UCW). It focuses on creating a framework for data dictionaries and providing actionable insights to improve data accuracy, reliability, and decision-making processes.

## Background:
UCW's growth has led to data quality problems such as errors, duplicates, and inconsistent formats. These issues can result in inefficiencies, compliance risks, and flawed business strategies. This project aims to address these challenges by implementing robust data quality control measures.

## Scope:
The project focuses on the following key areas:
- **Data Storage**: 
  - AWS S3 has been used to store all project data.
  - Supports file, block, and object storage for different use cases.

- **Data Profiling**:
  - AWS Glue and AWS Glue DataBrew are used to assess data quality by reviewing and summarizing datasets.

- **Data Cleaning**:
  - AWS Glue removes errors, duplicates, and inconsistencies to ensure data reliability.

- **Monitoring and Reporting**:
  - AWS CloudWatch and AWS CloudTrail track project activities and provide reports.

## Methodology:
1. **Current State Assessment**:
   - Created a raw bucket in AWS S3.

2. **Data Profiling**:
   - Conducted profiling with AWS Glue DataBrew to assess data quality.

3. **Data Cleaning**:
   - Renamed incorrect columns, removed duplicates, and corrected invalid values.
   - Stored cleaned data in transformed buckets in AWS S3.

4. **Monitoring and Reporting**:
   - Used AWS CloudWatch and AWS CloudTrail for monitoring activities.

## Tools and Technologies:
- **Amazon AWS**:
  - AWS S3
  - AWS Glue
  - AWS Glue DataBrew
  - AWS CloudWatch
  - AWS CloudTrail
- **Other Tools**:
  - Microsoft Excel (data collection).
  - Draw.io (visualization).

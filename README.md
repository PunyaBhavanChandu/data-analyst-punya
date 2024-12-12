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
![image](https://github.com/user-attachments/assets/08cbaf6b-2c1f-4249-8a86-4dc9f304cd4f)
3. **Workflow**:
   - **Data Ingestion**:
     - Uploaded the data into the Standard S3 storage class for frequent access.
     - Directory path for raw data: `Amazon S3/Buckets/raw-data`.
![image](https://github.com/user-attachments/assets/4e3c2056-5304-4073-87e8-abf1f994126e)
   - **Data Profiling**:
     - Created a new bucket: `grp1-ccm-trf-cha` for storing transformed data.
     - Path: `Amazon S3/Buckets/grp1-ccm-trf-cha/data_profiling/`.
     - Used AWS Glue DataBrew to preview the dataset.
![image](https://github.com/user-attachments/assets/c4b94c0e-6115-415e-8764-f0c147d3d3a4)
   - **Data Cleaning**:
     - Created folders for system and user data in S3.
     - Path: `Amazon S3/Buckets/grp1-ccm-trf-cha/data_cleaning/`.
     - Renamed non-standard columns, extracted months from the date column, and deleted the date column for monthly analysis.
![image](https://github.com/user-attachments/assets/286cc378-30e3-4709-ade8-d5f5cb8013dd)
   - **Data Pipeline Design**:
     - Created a visual ETL job: `grp1-ccm-etl-cha`.
     - Dropped unnecessary columns, filtered data by months, and calculated the average for each month.
![image](https://github.com/user-attachments/assets/ae2887fc-25df-4e75-bc62-7dacd025b3fc)
![image](https://github.com/user-attachments/assets/5defa722-0453-4473-b11d-3ccea5e0594b)
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
![image](https://github.com/user-attachments/assets/5782d05c-65b6-4c93-a3d8-9b621d9895d5)
![image](https://github.com/user-attachments/assets/a1ec5694-c704-4bd4-a8fd-14339759503f)
2. **Data Profiling**:
   - Conducted profiling with AWS Glue DataBrew to assess data quality.
![image](https://github.com/user-attachments/assets/6504c1a5-b71e-49c2-90ca-1ac412ad50c3)
3. **Data Cleaning**:
   - Renamed incorrect columns, removed duplicates, and corrected invalid values.
![image](https://github.com/user-attachments/assets/92e7b19e-5bf3-4460-abd6-298de94f73f1)
   - Stored cleaned data in transformed buckets in AWS S3.
![image](https://github.com/user-attachments/assets/2bfb5827-407d-4b51-b54c-079831d3e9a0)
![image](https://github.com/user-attachments/assets/e95f42a0-95e1-4f28-b489-fce2dd73a1f8)
4. **Monitoring and Reporting**:
   - Used AWS CloudWatch and AWS CloudTrail for monitoring activities.
![image](https://github.com/user-attachments/assets/e250c129-df9f-427b-a51c-7f7e30823606)
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

# Descriptive Analysis of Lost Animal Breeds in Vancouver using AWS

## Project Overview

The City of Vancouver is improving its services with a **Data Analytics Platform (DAP)**, enabling smarter decision-making. My role in this project focused on analyzing the **animal control inventory**, particularly the **lost and found section**, to help the city better manage stray and missing animals.

This project provides insights into lost animal rates across various breeds for the years **2023 and 2024**, leveraging the power of AWS technologies for data storage, cleaning, analysis, and monitoring.

## Objective

The main goal of this project was to **identify the lost rate of animal breeds** in 2023 and 2024. The analysis provided insights into lost animal patterns to help the City of Vancouver optimize their animal control operations.

## Dataset

The dataset contains lost and found animal records from Vancouver, spanning December 2023 to January 2024. It includes the following key features:

- **Breed**: The type of animal breed.
- **Color**: The animal's color.
- **Date**: The date the animal was recorded as lost or found.
- **Name**: The animal's name.
- **Sex**: The gender of the animal.
- **State**: Whether the animal was found or lost.

Dataset link: [**Animal Control Inventory Dataset**](https://opendata.vancouver.ca/explore/dataset/animal-control-inventory-lost-and-found/information/?disjunctive.breed&disjunctive.color&sort=date)

## Data Analytical Question Formulation

### Goal
To **analyze the lost rate of different breeds** for the years 2023 and 2024, and identify how these rates have changed over time.

### Key Metric
- **Lost Breed Rate per Year**: This metric tracks the percentage of animals lost, categorized by breed, for both 2023 and 2024.

## Methodology

### 1. Data Collection and Storage

- **AWS S3**: The dataset was stored in two separate S3 buckets for the years 2023 and 2024, ensuring secure and scalable storage.
  
### 2. Data Cleaning and Preprocessing

- **AWS DataBrew**: The data was cleaned using AWS DataBrew to address missing values, remove duplicates, and ensure consistency across both datasets.

### 3. ETL Pipeline

- **AWS Glue**: I used AWS Glue to build an automated ETL (Extract, Transform, Load) pipeline, which enabled efficient data extraction from S3, transformation of the data, and loading it for analysis.
<img width="1027" alt="Screenshot 2024-09-18 at 2 48 42 AM" src="https://github.com/user-attachments/assets/f2c4c837-8958-48a2-ae35-ac7c100c29ad">

### 4. Data Analysis

- **AWS Athena**: SQL queries were run in AWS Athena to analyze the cleaned data. I calculated the lost rate of each breed and summarized trends in lost animals across 2023 and 2024.

Here is the exact query used to retrieve the necessary data from Athena:

```sql
SELECT * FROM parksrecreationandpets_aci_table_manjot;
```

## Data Visualization

- **Excel**: Histograms and bar charts were created in Excel to visualize the distribution of lost animal breeds, helping stakeholders easily interpret the trends.

**Visualization 1**: Histogram of Lost Breed Rates %

<img width="1441" alt="Screenshot 2024-09-18 at 2 57 03 AM" src="https://github.com/user-attachments/assets/53c0feb6-7a56-4f43-ab3b-41eb860e91f9">


## Publishing and Web Hosting

- **AWS EC2**: The analysis and results were published on a web server using AWS EC2 to make the findings easily accessible for stakeholders.

## Data Protection and Governance

- **AWS Key Management Service (KMS)**: Encryption was applied to secure data in S3 using KMS, ensuring that data at rest and in transit was protected with cryptographic keys.
- **Data Replication**: Replication rules were set to ensure data was duplicated across different AWS regions, providing redundancy in case of regional failures.
- **AWS Glue**: The data was governed and managed through AWS Glue, where a tested zone was established to maintain data quality.

## Data Monitoring

- **AWS CloudTrail**: API calls and user activities across the AWS environment were monitored using CloudTrail, enhancing auditing and security measures.
- **AWS CloudWatch**: CloudWatch tracked performance metrics and resource utilization, allowing me to monitor the health of services and ensure optimal performance.

## Data Insights and Findings

- **Lost Rates by Breed**: Certain breeds, especially dogs and cats, had a higher lost rate in 2024 compared to 2023.
- **Seasonal Trends**: The highest rates of lost animals were recorded during the holiday season (December to January).

**Recommendation**: The City of Vancouver could focus animal control efforts on high-risk breeds and holiday periods to improve lost animal recovery.

## Tools and Technologies Used

- **AWS S3**: For data storage.
- **AWS DataBrew**: For cleaning and transforming the dataset.
- **AWS Glue**: To automate the ETL pipeline.
- **AWS Athena**: For running SQL queries and analyzing the data.
- **Excel**: For visualizing the data using charts and histograms.
- **AWS EC2**: For hosting the analysis results on a web server.
- **AWS Key Management Service (KMS)**: For encryption and data protection.
- **AWS CloudTrail**: For monitoring user activities and API calls.
- **AWS CloudWatch**: For tracking performance metrics and monitoring system health.

## Deliverables

1. A detailed report summarizing the methods, findings, and recommendations.
2. Visualizations and dashboards to present key insights clearly.

## Conclusion

This project successfully analyzed the lost animal breed patterns in Vancouver for 2023 and 2024, providing insights that can improve the city’s animal control and recovery efforts. By leveraging AWS services, the project not only ensured scalability and efficiency but also maintained top-notch security and data governance. These findings can drive better animal control policies, helping reduce lost rates and improve recovery.


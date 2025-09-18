# Smart-Vehicles-Project-GM
This project demonstrates the design and implementation of a cloud-based data engineering pipeline leveraging Azure services to build a robust, automated data ingestion and validation framework. The primary goal is to enable seamless movement of data from external sources into an analytics-ready format while ensuring quality control at every stage.
![Untitled-1](https://github.com/user-attachments/assets/4b2988d0-3e6d-4b83-bdcd-052ab54d380d)

Project Overview

Data is sourced from Amazon S3 storage in JSON format and ingested into Azure Data Lake Storage (ADLS) as the raw landing zone. To ensure the quality and integrity of ingested data, an Azure Function App acts as a validation layer. The function parses incoming JSON files and categorizes them as valid or invalid.

Valid Data: Routed into a dedicated staging folder within ADLS for downstream processing.

Invalid Data: Sent to a rejected folder for monitoring, troubleshooting, or manual correction.

An event-based trigger monitors the staging folder. When new valid data arrives, it automatically invokes an Azure Data Factory (ADF) pipeline. The pipeline extracts data from the staging zone and ingests it into Azure SQL Database, where it can be queried for analytics and reporting.

Tools and Technologies Used

Amazon S3 → Source storage for raw JSON files.

Azure Data Lake Storage (ADLS) → Centralized landing zone for raw, staging, and rejected data.

Azure Function App → Data validation service for categorizing valid/invalid JSON files.

Azure Event Trigger → Watches for changes in the staging folder and kicks off pipelines.

Azure Data Factory (ADF) → Orchestrates ingestion from staging into Azure SQL Database.

Azure SQL Database → Stores curated, validated data for querying and analytics.

Key Outcomes

Built an automated ingestion framework that handles both data movement and quality checks.

Ensured data governance by separating valid and invalid data.

Enabled real-time, event-driven data pipelines with minimal manual intervention.

Delivered a scalable solution that can be extended to multiple data sources and formats.

<img width="1919" height="839" alt="image" src="https://github.com/user-attachments/assets/d85f44ff-d448-4dd5-b486-561bea2d078b" />

<img width="1920" height="574" alt="image" src="https://github.com/user-attachments/assets/62ec2c15-b37b-4899-9e0e-9a48a802848b" />
<img width="1045" height="504" alt="image" src="https://github.com/user-attachments/assets/cca708e0-51cb-46bd-bda9-5b9ba4f59365" />


<img width="1443" height="460" alt="image" src="https://github.com/user-attachments/assets/af220a80-3e2f-44b4-9019-9b4a22879c97" />

<img width="1643" height="756" alt="image" src="https://github.com/user-attachments/assets/5bd2360e-61ec-496b-ab19-62b9ac5fa858" />





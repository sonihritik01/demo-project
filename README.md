# demo-project𝐀𝐳𝐮𝐫𝐞
𝐄𝐧𝐝-𝐭𝐨-𝐄𝐧𝐝 𝐃𝐚𝐭𝐚 𝐄𝐧𝐠𝐢𝐧𝐞𝐞𝐫𝐢𝐧𝐠 𝐑𝐞𝐚𝐥-𝐓𝐢𝐦𝐞 𝐏𝐫𝐨𝐣𝐞𝐜𝐭 :

This project is a data engineering pipeline solution to a made-up business problem, created to aid in my learning and understanding of data pipelining.

𝐏𝐫𝐨𝐣𝐞𝐜𝐭 𝐎𝐯𝐞𝐫𝐯𝐢𝐞𝐰:

This project addresses a critical business need by building a comprehensive data pipeline on Azure. The goal is to extract customer and sales data from an on-premises SQL database, transform it in the cloud, and generate actionable insights through a Power BI dashboard. The dashboard will highlight key performance indicators (KPIs) related to gender distribution and product category sales, allowing stakeholders to filter and analyze data by date, product category, and gender.

𝐁𝐮𝐬𝐢𝐧𝐞𝐬𝐬 𝐑𝐞𝐪𝐮𝐢𝐫𝐞𝐦𝐞𝐧𝐭𝐬 :

The business has identified a gap in understanding customer demographics—specifically gender distribution—and how it influences product purchases. The key requirements include:

𝐒𝐚𝐥𝐞𝐬 𝐛𝐲 𝐆𝐞𝐧𝐝𝐞𝐫 𝐚𝐧𝐝 𝐏𝐫𝐨𝐝𝐮𝐜𝐭 𝐂𝐚𝐭𝐞𝐠𝐨𝐫𝐲:

A dashboard showing the total products sold, total sales revenue, and a gender split among customers.
Data Filtering: Ability to filter the data by product category, gender, and date.
User-Friendly Interface: Stakeholders should have access to an easy-to-use interface for making queries.

𝐒𝐨𝐥𝐮𝐭𝐢𝐨𝐧 𝐎𝐯𝐞𝐫𝐯𝐢𝐞𝐰:

To meet these requirements, the solution is broken down into the following components:


𝐃𝐚𝐭𝐚 𝐈𝐧𝐠𝐞𝐬𝐭𝐢𝐨𝐧:

Extract customer and sales data from an on-premises SQL database.
Load the data into Azure Data Lake Storage (ADLS) using Azure Data Factory (ADF).

𝐃𝐚𝐭𝐚 𝐓𝐫𝐚𝐧𝐬𝐟𝐨𝐫𝐦𝐚𝐭𝐢𝐨𝐧:

Use Azure Databricks to clean and transform the data.
Organize the data into Bronze, Silver, and Gold layers for raw, cleansed, and aggregated data respectively.

𝐃𝐚𝐭𝐚 𝐋𝐨𝐚𝐝𝐢𝐧𝐠 𝐚𝐧𝐝 𝐑𝐞𝐩𝐨𝐫𝐭𝐢𝐧𝐠:

Load the transformed data into Azure Synapse Analytics.
Build a Power BI dashboard to visualize the data, allowing stakeholders to explore sales and demographic insights.

𝐀𝐮𝐭𝐨𝐦𝐚𝐭𝐢𝐨𝐧:

Schedule the pipeline to run daily, ensuring that the data and reports are always up-to-date.
Technology Stack

Azure Data Factory (ADF): For orchestrating data movement and transformation.

Azure Data Lake Storage (ADLS): For storing raw and processed data.

Azure Databricks: For data transformation and processing.

Azure Synapse Analytics: For data warehousing and SQL-based analytics.

Power BI: For data visualization and reporting.

Azure Key Vault: For securely managing credentials and secrets.

SQL Server (On-Premises): Source of customer and sales data.

Setup Instructions
𝐏𝐫𝐞𝐫𝐞𝐪𝐮𝐢𝐬𝐢𝐭𝐞𝐬:

An Azure account with sufficient credits.
Access to an on-premises SQL Server database.

Step 1: Azure Environment Setup
Create Resource Group: Set up a new resource group in Azure.

𝐏𝐫𝐨𝐯𝐢𝐬𝐢𝐨𝐧 𝐒𝐞𝐫𝐯𝐢𝐜𝐞𝐬:

Create an Azure Data Factory instance.
Set up Azure Data Lake Storage with bronze, silver, and gold containers.
Set up an Azure Databricks workspace and Synapse Analytics workspace.
Configure Azure Key Vault for secret management.

Step 2: Data Ingestion
Set up SQL Server: Install SQL Server and SQL Server Management Studio (SSMS). Restore the AdventureWorks database.
Ingest Data with ADF: Create pipelines in ADF to copy data from SQL Server to the bronze layer in ADLS.

Step 3: Data Transformation
Mount Data Lake in Databricks: Configure Databricks to access ADLS.
Transform Data: Use Databricks notebooks to clean and aggregate the data, moving it from bronze to silver and then to gold.

Step 4: Data Loading and Reporting
Load Data into Synapse: Set up a Synapse SQL pool and load the gold data for analysis.
Create Power BI Dashboard: Connect Power BI to Synapse and create visualizations based on business requirements.

Step 5: Automation and Monitoring
Schedule Pipelines: Use ADF to schedule the data pipelines to run daily.
Monitor Pipeline Runs: Use the monitoring tools in ADF and Synapse to ensure successful pipeline execution.

Step 6: Security and Governance
Manage Access: Set up role-based access control (RBAC) using Azure Entra ID (formerly Active Directory).

Step 7: End-to-End Testing
Trigger and Test Pipelines: Insert new records into the SQL database and verify that the entire pipeline runs successfully, updating the Power BI dashboard.

𝐂𝐨𝐧𝐜𝐥𝐮𝐬𝐢𝐨𝐧:

This project provides a robust end-to-end solution for understanding customer demographics and their impact on sales. The automated data pipeline ensures that stakeholders always have access to the most current and actionable insights.

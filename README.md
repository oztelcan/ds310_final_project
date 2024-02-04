
Project Pathway and Methodology:
Provisioned a Data Lake and landed data in it from various Cloud resources, including Azure SQL DB and CosmosDB. 
Managed to land data from On-Premise resources, utilizing an Azure VM to simulate an on-prem store for SQL Server. 
A key part of our project involved creating Data Pipelines to merge these datasets into a usable format in an ODS container.
For all of the file outputs when pulling data into the data lake, we used the .parquet format which was crucial to avoid files being named with a GUID, which could lead to unnecessary confusion.
We defined Star/Snowflake Schemas and created a Data Warehouse.
To complete the project, we performed calculations on Fact tables. 
Finally, we visualized the data using Power BI, creating a compelling data story that highlighted the key insights and findings from our project.

Project Introduction:
The dataset sourced from a variety of sources including the WHO, CDC, Public Health Departments, and more using the Azure environment involves COVID-19 cases, deaths, and recovery statistics for 10 countries and their pandemic-era governmental policies. 
With the use of this data, we seek to draw conclusions about policy effectiveness and make recommendations to Caladan (an imaginary country) regarding best practices. 
Our two assigned policies were International travel - quarantine arrivals from some regions (Level 2) and Contact tracing - Comprehensive contact tracing (Level 2). 
To find the most effective policy we tried to answer 2 main questions:

If any, what level of International Travel Restrictions would be the most effective?
How does this level compare to Level 2 Restrictions?
What external factors could explain differences in effectiveness in different countries?

Is Contact Tracing at Level 2 an effective policy?
If not, what intuitive reason could explain why contact tracing was not effective? (dig deeper, to think micro)
What policy best fits that reason, and is that policy effective?
What external factors could explain differences in effectiveness between Contact Tracing and the better policy?

Data Overview and Exploration:
The Policy data ranged from 0 to 2,3, or 4 ranging from no restriction levels to highly restrictive measures. We can group policies by “Low” and “High” as countries vary in the length of time of each restriction. 
External data regarding ports of entry also featured demarcations between low and high. Due to the possible source errors, we made use of the ranges “Low” and “High” leaving a middle tier as well. 
Anomalies such as the United Kingdom’s negative case and death numbers were replaced with the average cases or deaths of the week prior and the week ahead. 
We used per capita numbers such that one country wouldn’t have an outsized impact on the data.

# Tokyo-Olympics-Azure-Data-Engineering-Project

I have created an Azure Cloud Data Engineering Project to analyze the Tokyo Olympics Dataset which includes creating ETL pipelines, transformation through spark and much more.

## Architecture Diagram

![Azure Architecture Diagram drawio](https://github.com/pakhijo/olympic-data-engineering-project/assets/93408790/f2a0dabb-ebd5-41b3-9d6c-bf462e6fa235)






## Data Source

The dataset in this project has been taken from Kaggle and stored into this Github repo in [data](https://github.com/Bloom-98/olympic-data-engineering-project/tree/main/data) folder. It is being fetched by Data Factory pipeline later on.

Dataset- [Tokyo Olympics Data](https://www.kaggle.com/datasets/arjunprasadsarkhel/2021-olympics-in-tokyo)




## Steps followed while execution-

- Export dataset from Kaggle and Store in Github.
- Create Azure Data Factory Pipeline for extracting data from Github and store in Azure Data Lake Gen2.
- Connect Azure Databricks workspace to ADLS Gen2 and perform necessary transformations on raw data.
- Write transformed data through Databricks into ADLS Gen2.
- Create DB through Data lake in Azure Synapse analytics and run SQL queries on the data to analyze it.
- Visualize the data using PowerBI dashboard.


## Azure Data Factory

Created a pipeline using Azure Data Factory to extract data from Github via HTTP Linked Service and store it in Azure Data Lake Storage Gen 2.

![image](https://github.com/Bloom-98/olympic-data-engineering-project/assets/93408790/7959d122-c664-47e7-b7f7-70fa34a62d11)

Code available at - [ADF](https://github.com/Bloom-98/olympic-data-engineering-project/tree/main/ADF)



## Azure Data Lake Storage Gen2

ADLS Gen2 is being used as Data Store for both Raw and Transformed Data.

![image](https://github.com/Bloom-98/olympic-data-engineering-project/assets/93408790/a4a431eb-2647-4bb1-afc6-6b4f617848aa)

The data is being stored in two different folders for convenience.

## Azure Databricks

In Azure Databricks necessary transformations are being performed on Raw data from ADLS Gen2, and then storing the transformed data back to ADLS Gen2.
![image](https://github.com/Bloom-98/olympic-data-engineering-project/assets/93408790/7b9268fe-9fe4-41d8-82cf-f21d139953de)

Code available at - [Databricks](https://github.com/Bloom-98/olympic-data-engineering-project/tree/main/Databricks)

## Azure Synapse Analytics

Azure Synapse Analytics provides data warehousing feature, executed SQL queries to extract insights from the data.

![image](https://github.com/Bloom-98/olympic-data-engineering-project/assets/93408790/c97829f6-5336-476b-90f2-0c8853567736)

Code available at - [Synapse Analytics](https://github.com/Bloom-98/olympic-data-engineering-project/tree/main/Synapse%20Analytics)



## Power BI

Created an interactive dashboard with importing data from Datawarehouse in Azure Synapse Analytics, analyzed the Tokyo Olympics data using various vizualizations(bar chart, column chart, map, donut chart, etc. 

![image](https://github.com/pakhijo/olympic-data-engineering-project/assets/93408790/9275d71e-70e8-4e7a-9bdc-802dae6a99ac)

PBIX file available at - [Power BI](https://github.com/pakhijo/olympic-data-engineering-project/tree/main/Power%20BI)

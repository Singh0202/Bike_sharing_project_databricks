# End-to-End-Bike-Sharing-Project
This End-to-End Bike Sharing Project developed using Azure Databricks, Blob, and Delta Lake.

### Project Overview
The project focuses on bike sharing systems, which are automated bike rental systems with a global presence. These systems play a crucial role in traffic, environmental, and health matters. The dataset contains hourly data from various bike-sharing programs worldwide, consisting of over 500 thousand bicycles. For more detailed information on the dataset used for this project, please refer to this [link](https://archive.ics.uci.edu/ml/datasets/bike+sharing+dataset).

### Project Requirements
#### [Data Ingestion](ingestion_pipeline):
1. Ingest the raw data into the data lake.
2. Apply appropriate schema to the ingested data.
3. Enable SQL-based analysis on the ingested data.
#### [Data Transformation](transformation_pipeline):
1. Normalize the ingested data and create data model.
2. Enable SQL-based analysis on the transformed data.
#### [Analysis](analysis):
1. Utilize Spark SQL to analyze the transformed data and gain insights.
#### [Business Intelligence](power_bi_dashboard.pbix):
1. Develop a Power BI dashboard to track Key Performance Indicators (KPIs) of the bike sharing system.
### Tools Used
To fulfill the project requirements, I utilized Azure Databricks, Azure Data Lake Gen 2, Delta Lake, PySpark, Spark SQL, Power BI, VSCode, and Lucid Chart.

### Solution Architecture
The project follows the "Azure Databricks Modern Analytics Architecture" and employs a three-layer approach: bronze, silver, and gold. These layers represent different stages of data refinement, where the data's value increases as it progresses from bronze to gold.
<img src="diagrams/architecture.png"  width="60%" height="30%">
|:--:|
|<b>Architecture</b>|

1. Bronze Layer: The bronze layer serves as the initial landing zone for raw and unprocessed data. It stores the ingested data in its original raw format.

<p align ='center'><img src="diagrams/raw_data.jpg"  width="40%" height="10%"></p>

2. Silver Layer: The silver layer acts as an intermediate stage where data undergoes cleaning, transformation, and structuring. It prepares the data for downstream analytics by performing deduplication, filtering, standardization, and enrichment. Data quality checks, schema validation, and integration processes ensure data consistency and reliability.

<p align ='center'><img src="diagrams/processed_data.jpg"  width="40%" height="10%"></p>

3. Gold Layer: The gold layer represents the final stage of data refinement. It contains a well-structured, clean, and validated dataset optimized for efficient querying and analysis. Further transformations, aggregations, joins, and optimizations are performed on the data to cater to specific analytical use cases.

<p align ='center'><img src="diagrams/data_models.jpg"  width="60%" height="30%"></p>

### Analysis using Spark SQL
One of the key highlights of this solution is the ability to analyze data in each layer using Spark SQL. This empowers users to leverage the power of Spark SQL in conjunction with PySpark for comprehensive data analysis. The "[analysis](Analysis)" folder provides all the Spark SQL queries performed on the transformed data.

### Project Outcome
The project culminates in a [Power BI dashboard](power_bi_dashboard.pbix) that utilizes data from the gold layer to track Key Performance Indicators (KPIs) of the bike sharing system.
<p align ='center'><img src="diagrams/BI dashboard.PNG"  width="40%" height="10%"></p>


# Bing News Sentiment Analysis

This project implements a comprehensive solution for analyzing the sentiment of the latest news articles sourced from the Bing News API. The data ingestion, transformation, and reporting are conducted using Microsoft Fabric technologies.

## Project Overview

### Environment Setup
- Created a resource group in Microsoft Azure to house the project.
- Set up a Bing Search v7 API resource as the data source.
- Established a Lakehouse database in Microsoft Fabric for data processing and analysis.

### Data Ingestion
- Utilized Data Factory within Microsoft Fabric to connect to the Bing API and ingest the latest news articles into OneLake Data Storage in JSON format.
- Implemented API authentication and specified parameters to filter news articles relevant to India from the last 24 hours.

### Data Transformation (Incremental Load)
- Read JSON files into a Spark DataFrame, selecting and flattening the data to extract relevant fields.
- Employed Type 1 merge for handling incremental updates in the data warehouse.

### Sentiment Analysis
- Utilized a pre-trained machine learning model in Synapse Data Science within Microsoft Fabric to perform sentiment analysis on the news articles.

### Power BI Reporting
- Created a semantic model in Power BI to visualize sentiment analysis results.
- Implemented measures and filters to display sentiment percentages for the latest news articles.

### Building Pipelines
- Integrated all activities into an end-to-end pipeline scheduled to run daily at 6:00 AM, ensuring that Power BI reports are updated with the latest news and associated sentiment.
- Set up alerts using Data Activator for monitoring negative sentiment news.

## Technologies Used
- Microsoft Azure (Resource Group for API setup)
- Microsoft Fabric (Data Factory, Synapse, Power BI)
- Apache Spark
- REST APIs
- Delta Lake

## How to Run
1. Set up an Azure account and create the necessary resources (Resource Group, Bing API).
2. Configure the Data Factory pipelines in Microsoft Fabric according to the instructions provided in the project notebooks.
3. Run the notebooks in Synapse to execute data transformation and sentiment analysis.
4. Access the Power BI report for visualization of results.

## Acknowledgments
- Microsoft Azure for providing the cloud infrastructure.
- Bing News API for the data source.
- Microsoft Fabric for data processing and analytics capabilities.

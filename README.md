# Bing News Sentiment Analysis

This project implements a comprehensive solution for analyzing the sentiment of the latest news articles sourced from the Bing News API. The data ingestion, transformation, and reporting are carried out using Microsoft Azure technologies, including Data Factory, Synapse, and Power BI.

## Project Overview

### Environment Setup
- Created a resource group in Microsoft Azure for the project.
- Set up a Bing Search v7 API resource as the data source.
- Established a Lakehouse database in the data engineering component of Microsoft Fabric.

### Data Ingestion
- Utilized Azure Data Factory pipelines to connect to the Bing API and ingest the latest news articles into OneLake Data Storage in JSON format.
- Implemented API authentication and parameters to filter news articles specific to India for the last 24 hours.

### Data Transformation (Incremental Load)
- Read JSON files into a Spark DataFrame, selecting and flattening the data to extract relevant fields.
- Utilized Type 1 merge for handling incremental updates in the data warehouse.

### Sentiment Analysis
- Employed a pre-trained machine learning model in Synapse Data Science to perform sentiment analysis on the news articles.

### Power BI Reporting
- Created a semantic model in Power BI to visualize sentiment analysis results.
- Implemented measures and filters to display sentiment percentages for the latest news articles.

### Building Pipelines
- Integrated all activities into an end-to-end pipeline that schedules data ingestion and updates Power BI reports daily at 6:00 AM.
- Set up alerts using Data Activator for monitoring negative sentiment news.

## Technologies Used
- Microsoft Azure (Data Factory, Synapse, Power BI)
- Apache Spark
- REST APIs
- Delta Lake

## How to Run
1. Set up an Azure account and create the necessary resources (Resource Group, Bing API, Lakehouse database).
2. Configure the Data Factory pipelines according to the instructions provided in the project notebooks.
3. Run the notebooks in Synapse to execute data transformation and sentiment analysis.
4. Access the Power BI report for visualization of results.


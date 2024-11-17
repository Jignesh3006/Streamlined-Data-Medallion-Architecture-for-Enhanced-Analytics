# Streamlined-Data-Medallion-Architecture-for-Enhanced-Analytics

## 📜 Table of Contents





# Project Overview : 

To build a medallion architecture in Microsoft Fabric for real-time analytics, start by creating data pipelines to copy data from a sample data. Next, ingest streaming events into Microsoft Fabric's Real-Time Analytics (RTA) with EventStream for immediate processing. Implement necessary data transformations within RTA to prepare the data for analysis, and then develop interactive reports and dashboards to visualize real-time insights. Finally, continuously monitor and optimize the performance of your pipelines and dashboards to ensure efficient data flow and responsiveness, enabling informed decision-making based on real-time analytics.

# What is the Medallion Architecture :

Medallion architecture, also known as multi-hop architecture, is a data design pattern that organizes data within a lakehouse to enhance its quality progressively through three distinct layers: Bronze, Silver, and Gold. The Bronze layer contains raw, unprocessed data, while the Silver layer involves filtering and cleansing to improve usability. Finally, the Gold layer features enriched and aggregated data ready for analysis and business applications. This structured approach allows organizations to incrementally refine their data, ensuring higher quality and better alignment with business needs as it flows through each layer, ultimately facilitating effective decision-making and insights.

## Bronze Layer 
- Contains raw data, sometimes referenced as the data staging area.
- Not accessible to consumers only to engineers.
- May contain private or personal information.

## Silver Layer
- Contains the deduplicated data and accessible to all consumers
- This data can be used by Data Analyst , Data Engineers and Data Scientist according to their needs

## Gold Layer
- Contains aggregated data
- Final analytical data use for building the dashboards

# E-commerce data store 

E - commerce database consist of the 
 - Customer
 - Address
 - SalesOrderHeader
 - SalesOrderDetail
 - Event : a click or impression event

# Building the Analytics Platform

### Create a Fabric Workspace and in that create a New EventHouse

In the image below, we are establishing an event house to manage all our batch and streaming data. This data will then be utilized in a lakehouse for further transformation based on our requirements.

![AltImage]()

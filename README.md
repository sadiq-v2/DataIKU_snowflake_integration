# RFM-Solution-Segmentation-with-Dataiku-and-Snowflake

Project Challenges and Solutions
This document describes the main challenges encountered during the project and the steps taken to resolve them.

1. RFM Solution Segmentation in Dataiku
Challenge:
When attempting to build the RFM (Recency, Frequency, Monetary) segmentation model in Dataiku, a "write-protected" error was encountered, preventing the model from being executed.

Solution:
To resolve this, I manually changed the write-protected status of the files involved to "normal." This allowed the build process to proceed without further issues.

2. Dataiku and Snowflake Connection
Challenge:
Establishing a connection between Dataiku and Snowflake posed difficulties due to configuration requirements.

Solution:
I created a Word document that details the required steps and SQL scripts to set up the connection. By following this document and executing the necessary scripts in Snowflake, I successfully established a working connection between Dataiku and Snowflake.

3. RFM Solution with Custom Data
Challenge:
Using our own transaction data for the RFM analysis required additional preprocessing and integration with Snowflake.

Solution:

Data Preparation:

Downloaded sample transaction_data from Kaggle.
https://www.kaggle.com/datasets/vipin20/transaction-data

Renamed columns to match the required and mandatory fields for RFM analysis, including:
Product ID (A product)

Transaction ID (A related transaction)

Product Quantity (Number of products purchased in a transaction)

Product Price (The product purchase price)

Date (Transaction date)

Customer ID (Customer who made the purchase)

Data Loading:

Loaded the modified data into Snowflake using the Snowflake GUI.
Transferred ownership of the database, schema, and table to the Dataiku role created in step 2, ensuring Dataiku had the necessary permissions.
Testing:

For testing purposes, I extracted a subset of 4,000 records from the original dataset of 1 million records.
Modified the date format, reordered columns, and then loaded this test dataset into Snowflake.
4. RFM Solution Using Dataiku with Snowflake Data
Challenge:
Once the Dataiku-Snowflake connection was established, implementing the RFM solution required specific configurations within Dataiku to work with the Snowflake-hosted data.

Solution:
Follow the document for RFM Solution Using Dataiku with Snowflake Data. This document contains the steps and configurations required to use the data stored in Snowflake for RFM analysis within Dataiku.

Important Links:
https://knowledge.dataiku.com/latest/solutions/retail/solution-rfm-segmentation.html
https://doc.dataiku.com/dss/latest/connecting/sql/snowflake.html
https://blog.dataiku.com/up-and-running-in-five-minutes-with-dataiku-and-snowflake
https://quickstarts.snowflake.com/guide/a_dataiku_and_snowflake_guide_to_data_science/#0


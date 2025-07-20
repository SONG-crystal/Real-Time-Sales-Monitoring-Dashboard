# Real-Time-Sales-Monitoring-Dashboard
This project involves building an automated ETL pipeline using Azure Data Factory to transfer JSON-based NoSQL data from Azure Cosmos DB to Azure Data Lake Storage Gen2, and creating dynamic Power BI dashboards for real-time data visualization and analysis.


This project uses Azure services (e.g., Azure Data Factory, Azure Cosmos DB, etc.). Because running the project incurs costs for Azure resources, I have deleted the resources after use to avoid unnecessary charges.


## Resources used:
- Resource Group
- Azure Cosmos DB
- Data Factory
- Storage Account
<img width="360" height="170" alt="image" src="https://github.com/user-attachments/assets/96f996ee-7626-4f45-b437-6cf70a829f71" />

## Step 1. Azure CosmosDB
- Created a sample database and container(table)
<img width="740" height="423" alt="image" src="https://github.com/user-attachments/assets/9e554d9b-39c1-4c8a-ab8c-ad0597674d57" />

## Step 2. Azure Data Factory - set the source
- Accessed Azure Data Factory Studio and created a new pipeline
- Configured the pipeline’s "source" to connect to the Cosmos DB database and container created in Step 1
<img width="612" height="411" alt="image" src="https://github.com/user-attachments/assets/0cae0746-b1e4-4fda-8485-ef07fd02a8cc" />

## Step 3. Data Lake Storage Gen2
- Created a new Storage Account in the Azure portal to manage and store data
<img width="559" height="381" alt="image" src="https://github.com/user-attachments/assets/78ee02f3-d5e6-4da5-a294-271202d6e6e8" />

## Step 4. Azure Data Factory - set the sink
- Go back to the Azure Data Factory Studio and set the "sink" with Data Lake Gen2 (JSON format)
- Set the file path
<img width="639" height="392" alt="image" src="https://github.com/user-attachments/assets/2bfa6c9b-7da4-426d-9d50-c8ac3143eee0" />

## Step 5. Power BI
- Connected to Azure Data Lake by selecting Get Data > Azure Data Lake in Power BI
- When entering the URL, used dfs instead of blob in the endpoint
- Performed Combine & Transform steps to properly load and shape the JSON data for analysis
<img width="580" height="299" alt="image" src="https://github.com/user-attachments/assets/c0850531-9b1c-4655-b0a7-53fff4ccb11d" />

## Step 6. Setting Automation
- Located my project in the Power BI workspace. (if not found, imported the project)
- In the Semantic Model’s Options > Settings > Credentials, pasted the Storage Account key created earlier
- Configured the data refresh schedule by setting the refresh time and automation frequency to update data automatically
<img width="368" height="398" alt="image" src="https://github.com/user-attachments/assets/3e5a7be9-4aeb-4645-ba9d-b3054a8b75c7" />

## Step 7. Testing
- Changed the category name to "yoga pants" from "YOGA pants"for testing purposes
- Refresh data in dataset at Power BI
<img width="622" height="395" alt="image" src="https://github.com/user-attachments/assets/3666427e-4149-4928-9ce5-93f7196a4cd2" />
<img width="416" height="251" alt="image" src="https://github.com/user-attachments/assets/49c5d1d5-7973-408b-9f68-7bd8c4bcdda4" />

## Step 8. Visualized Data



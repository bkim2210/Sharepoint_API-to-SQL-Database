SharePoint Data Retrieval and Transformation Script

This Python script is designed for retrieving and transforming data from a SharePoint document library and storing it into a SQL Server data warehouse. The script utilizes Azure AD application credentials for authentication to both SharePoint and SQL Server.

Key Features:

Connects to a SQL Server data warehouse using SQL Alchemy and pyodbc.
Authenticates to a SharePoint site using Azure AD application credentials.
Traverses through folders in a specified SharePoint document library, retrieving role assignments (groups and users) associated with each folder.
Fetches members of each group and creates a DataFrame containing information about folders, groups, and their members.
Filters and transforms the DataFrame to separate entries with group members and those without, flattening the DataFrame for entries with group members.
Adds a timestamp to the DataFrame.
Attempts to write the final DataFrame to a specified SQL Server table.
Includes error logging functionality to capture and log exceptions during execution.
Usage Instructions:

Replace placeholder values in the script with your actual Azure AD application ID, password, SharePoint site URL, database details, and other specific configurations.
Execute the script to retrieve and transform SharePoint data.

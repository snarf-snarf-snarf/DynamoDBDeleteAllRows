# DynamoDBDeleteAllRows
Application for deleting all rows from a DynamoDB table. It does this by scanning the table to retrieve the primary key values and then deletes the rows in batches. Currently, AWS limits the maximum batch size to 25, so with large amounts of data multiple requests are executed.

# Prerequisites
You will need to download and install the [AWS SDK for .NET](https://aws.amazon.com/sdk-for-net/).

# Useage

First edit the App.config file and change the AWS profile and region as required.

To run the application from a command window:

  `DynamoDeleteAllRows.exe table_name hash_key_name [range_key_name]`

*table_name* - The name of the DynamoDB table.  
*hash_key_name* - The name of the hash key for the table.  
*range_key_name* - The name of the range key for the table if it has one.  

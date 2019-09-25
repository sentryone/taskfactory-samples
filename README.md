# taskfactory-samples
This repository contains samples for the SentryOne Task Factory product.

## REST Configuration Files 
We've included [sample configuration files](/rest/configs/) for use with the REST Source and Destination. 
These make it easier to connect 
to certain REST APIs by providing the endpoints in a predefined file. To use them, copy the desired configuration file
to the following location: `[InstallDir]\OAuth2ConfigFiles`. Typically the InstallDir is 
`C:\Program Files (x86)\Pragmatic Works\Task Factory`.

## Sample Packages
We've included [sample SSIS packages](/samples/) to show the use of our most used Task Factory Components
Each directory under samples has a Setup package (e.g. 1_SetupUpsertDemoDBs.dtsx) that you should run prior to opening the other sample packages. 

The current list of samples are

### [Upsert](/samples/Upsert)
	
	- 1_SetupUpsertDemoDBs.dtsx - Use to setup the Upsert samples
	- UpsertDestination_BasicSetup.dtsx - A simple upsert configuration
	- UpsertDestination_ColumnCompareWithAuditVariables.dtsx - Upsert configured with comparison columns and auditing variables to show the number of records inserted / updates
	- UpsertDestination_ErrorOutput.dtsx - Upsert configured with error output
	- UpsertDestination_InsertOnly.dtsx - Upsert configured for insert only
	- UpsertDestination_UpdateOnly.dtsx - Upsert configured for update only

### [Compression](/samples/Compression)
	
	- 1_SetupCompressionTaskDirectory.dtsx - Use to setup the Compression samples
	- CompressionTask_Compress.dtsx - Compression task configured to compression files into a zip file
	- CompressionTask_Decompress.dtsx - Compression task configured to decompress files from a zip file

### [Dynamics CRM](/samples/DynamicsCRM)
	
	- 1_SetupLocalDynamicsDemoDB.dtsx - Use to setup the Dynamics samples
	- DynamicsSource_BasicDataPull.dtsx - Dynamics Source configured to pull data from Dynamics
	- DynamicsSource_UsingFilters.dtsx - Dynamics Source configured to filter rows with a filter
	- DynamicsSource_FilterVariableReplacement.dtsx - Dynamics Source configured to use a variable in the filter
	- DynamicsDestination_Update.dtsx - Dynamics Destination configured to update records
	- DynamicsDestination_Delete.dtsx - Dynamics Destination configured to delete records

### [REST](/samples/REST)
	
	- 1_SetupLocalRestDirectory.dtsx - Use to setup the REST Samples
	- RestTask_SaveResponseToVariable.dtsx - REST Task configured to save response to a variable
	- RestTask_FilteredResponse.dtsx - REST Task configured to filter the response of a request and save to a variable
	- RestSource_BasicPullData.dtsx.dtsx - REST Source configured to pull data from an endpoint
	- RestSource_CustomHeaders.dtsx - REST Source configured to use custom headers
	- RestSource_DotNotation.dtsx - REST Source configured to use dot notation in a JSON token
	- RestSource_VariableReplacements.dtsx - REST Source configured to use variable replacements in the Endpoint URL, PostBody and Headers
	- RestDestination_BasicPostData.dtsx - REST Destination configured to post data to an endpoint
	
### [Secure FTP](/samples/SecureFTP)
	
	- 1_SetupLocalSFTPDirectory.dtsx - Use to setup the SFTP Samples
	- SecureFTP_CheckIfFileExists.dtsx - SFTP Task configured to check if a file exists on the server
	- SecureFTP_DownloadDirectory.dtsx - SFTP Task configured to download a directory from the server
	- SecureFTP_DownloadFileFromServer.dtsx - SFTP Task configured to download a file from the server
	- SecureFTP_RenameFileOnServer.dtsx - SFTP Task configured to rename a file on the server
	- SecureFTP_UploadDirectory.dtsx - SFTP Task configured to upload a local directory to the server
	- SecureFTP_UploadFileToServer.dtsx - SFTP Task configured to upload a local file to the server

### [Salesforce](/samples/Salesforce)
	
	- 1_SetupLocalSalesForceDB.dtsx - Use to setup the Salesforce samples
	- SalesforceSource_BasicQuery.dtsx - Salesforce Source configured to pull data with a basic query
	- SalesforceSource_CustomRestrictedQuery.dtsx - Salesforce Source configured to pull data with a query using a variable in the WHERE statement
	- SalesforceSource_RelationalQuery.dtsx - Salesforce Source configured to pull data with a relational query
	- SalesforceDestination_InsertData.dtsx - Salesforce Destination configured to insert data
	- SalesforceDestination_Upsert.dtsx - Salesforce Destination configured to upsert data
	- SalesforceDestination_Delete.dtsx - Salesforce Destination configured to delete data
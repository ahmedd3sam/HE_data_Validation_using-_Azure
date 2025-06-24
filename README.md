# HR_data_Extraction_using_Azure:
Extracting and validation HR_Cleaned_Data using Azure Data Factory

## 1- Create a Linked service with Azure Blob Storage that contain data:
![Connecting Storage Account using Linked Service](https://github.com/user-attachments/assets/4b0ffabf-c199-47bd-9d2b-2d3e530a9728)

## 2- Creating Dataset (DelimitedText):
-- specifying that first row as a header.
![Linking data path in storage account](https://github.com/user-attachments/assets/b13caf1c-681a-4815-81a3-95fa67a0de20)

## 3- Adding "Get Metadata Activity" to the pipeline:
-- connecting data to get the structure and number of columns.
![Get MetaData Activity](https://github.com/user-attachments/assets/de690cf2-c6aa-4c82-a9b5-34d22268efa5)

## 4- Adding a Variable to hold column count:
![Setting Variable of type integer](https://github.com/user-attachments/assets/10401cd7-8678-4a46-a724-0a1f641d8f87)

## 5- Adding "If Condition" to the pipeline:
-- checking if number of columns is valid to procced into copy activity.
![If condition activity](https://github.com/user-attachments/assets/f0cff231-c650-4678-91f3-f89945d10975)

## 6- Copying data into dataLake using "Copy Data Activity":
-- copy data from storage account into dataLake if condition is True
![Copy Data Activity](https://github.com/user-attachments/assets/9dea3878-a205-4b62-a94b-ccb0b48bfbd7)

## 7- Adding "Storage Event Trigger" to the pipeline:
-- when uploading data to storage account, Pipeline will start to copy data into DataLake.
![Storage Event Trigger](https://github.com/user-attachments/assets/42d1fba8-88d3-4c4f-b96e-ad6f5a91ab26)
![Pipeline run](https://github.com/user-attachments/assets/abec59b5-6be6-4065-9ff3-225be0643c22)
![Data copied into DataLake succesfully](https://github.com/user-attachments/assets/e0a6b654-6c2d-40c4-b7f9-c5f7adae65b0)

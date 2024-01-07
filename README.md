# Electrical Service Central Task Aggregator

## Target Scenario
Whenever a field electrician completes a job, they send an email to a specific address with details about the procedures and services they have provided, in a table-like structure, with two attachments in PDF format: an image of the completed task and an invoice of the various products which were purchased. 

## Task Automation
The robot downloads the PDF documents, and scrapes the email body. Using a preconfigured Excel sheet with tariffs, another sheet is created for that particular task, using the scraped data, while also extracting the image from the attached PDF. Within the newly created Excel sheet, the products which were purchased are extracted from the invoice and appended to the table. The documents are uploaded to a folder belonging to the sender, in Google Drive. 

The path of the parent temporary folder, as well as the expected filenames of the attachments can be configured using a JSON file.

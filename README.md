# File-Sharing-Serverless-Platform
An AWS serverless for sharing with Base64 encoding. 


Project Description:
The Serverless File Sharing Platform allows users to securely upload and download files via a simple HTTP API. It leverages AWS Lambda for serverless compute, API Gateway for RESTful API management, and Amazon S3 for durable and scalable object storage. Users can interact with the platform using any HTTP client (like Postman), making it versatile for various use cases that involve file sharing and storage.

Use Cases:

File Sharing: Users can upload files to the platform using a POST request, specifying the file name and content. This can be useful for sharing documents, images, or any other digital assets securely.
File Distribution: Content creators can distribute files (e.g., software updates, media files) to consumers by generating download links through the platform.
Collaborative Work: Teams can share project resources, documents, and data securely, facilitating collaboration across different locations.

![File  sharing mast head](https://github.com/user-attachments/assets/f052e563-967f-4970-98f2-b737dce5a8ad)



Steps to Build the Project:


Prerequisites

AWS Account with appropriate permissions to create Lambda functions, API Gateway, and S3 buckets.
Passion to Learn!


Steps to Deploy


Step 1: 

Create an S3 bucket to store uploaded files:

Bucket Name: my-file-sharing-bucket-amc

Step 2:

Create the Lambda function to handle file uploads (UploadFunction):
Name: UploadFunction
Runtime: Python 3.x
Execution role: IAM role with S3 write permissions
Code: Use the UploadFunct Python code.
![upload](https://github.com/user-attachments/assets/8dfd44b1-f45f-4296-acc3-ebb97e9d2cf8)

Now create the  lambda function for file download 

Step 4: 

Create an API Gateway


Name: my-file-sharing-api-amc
Create two resources: /files with POST and GET methods.
For each method, configure Lambda integration with UploadFunction and DownloadFunction respectively.

![api-get-upload-meteh](https://github.com/user-attachments/assets/5d7be60a-dc2c-4a0b-a9e1-97af7442e6f2)

![post method ](https://github.com/user-attachments/assets/bd5f4ec5-b628-4c6e-b8df-0f2998743f0e)

Step 5: 

Configure GET Method:


Method Request --> Edit --> Request validator --> Validate Query String Parameters and Headers
Method Request --> Edit --> Request Body --> text/plain
![request for get ](https://github.com/user-attachments/assets/7dd50ad7-d462-48a9-8318-b9635da2ddfe)

Integration Request --> Edit --> Mapping Templates --> Content Type: application/json --> Content Body:





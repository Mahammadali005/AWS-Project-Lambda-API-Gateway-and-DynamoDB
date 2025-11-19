# AWS-Project-Lambda-API-Gateway-and-DynamoDB
This project implements a **serverless web application** using **AWS
Lambda**, **API Gateway**, and **DynamoDB**.\
HTML contact form sends user data to an API endpoint, and
Lambda stores the data in DynamoDB.

## 🚀 Project Architecture
![Architecture Diagram](images/<img width="850" height="491" alt="WEB APPLICATION USING LAMBDA,APIGATEWAY,DYNAMODB drawio" src="https://github.com/user-attachments/assets/660a9637-36db-49c0-9697-714facc6aa60" />
.jpg)

### **Services Used**

  -----------------------------------------------------------------------
  AWS Service                              Purpose
  ---------------------------------------- ------------------------------
  **API Gateway (HTTP API)**               Accepts POST requests from
                                           HTML form

  **AWS Lambda**                           Backend logic to process form
                                           data

  **DynamoDB**                             Stores submitted messages

  **IAM Role (admin-lambda-role)**         Grants Lambda permissions

  **S3 / Local HTML**                      Front-end contact form
                                           (contactus.html, success.html)
  -----------------------------------------------------------------------

## 🧩 How It Works 

1.  User fills the **Contact Us** HTML form (`contactus.html`).
2.  Form submits a POST request to API Gateway → Lambda.
3.  Lambda parses the form and inserts data into DynamoDB.
4.  Lambda returns an HTML success page (`success.html`).

## 🔐 IAM Role Used

Your Lambda function uses an IAM role named **admin-lambda-role** with:

-   AmazonDynamoDBFullAccess\
-   AWSLambdaBasicExecutionRole

## 📁 Project Structure

    AWS-Project-Lambda-API-Gateway-and-DynamoDB/
    │
    ├── contactus.html
    ├── success.html
    ├── lambda_function.py
    └── README.md

## 🧠 Lambda Function

Handles GET → serves HTML\
Handles POST → writes to DynamoDB and returns success page

## 📥 Deployment Steps

1.  Create DynamoDB Table\[images/<img width="1911" height="943" alt="Dynamodb" src="https://github.com/user-attachments/assets/eb308def-89f4-46c1-af67-278733347c77" />
2.  Create IAM Role\[images/<img width="1891" height="879" alt="IAM" src="https://github.com/user-attachments/assets/185e5e53-1f6c-48f3-93c4-619af5aca303" />
3.  Create Lambda Function\[images/<img width="1912" height="877" alt="Lambda Function" src="https://github.com/user-attachments/assets/f5d72c4a-20b0-45ec-b1c3-b749688897c0" />
3.1 Create Lambda Function\[images/<img width="1897" height="876" alt="Lambda Function 1" src="https://github.com/user-attachments/assets/054ab043-13e9-4efc-b0a6-24eaca3aac56" />
3.2 Create Lambda Function\[images/<img width="1907" height="876" alt="Lambda Function 2" src="https://github.com/user-attachments/assets/f50b44d5-2731-4957-bbb6-6cb3d99be59e" />
3.3 Create Lambda Function\[images/<img width="1895" height="883" alt="Lambda Function 3" src="https://github.com/user-attachments/assets/266bc320-fcb7-4d16-bf88-f9658c865343" />
3.4 Create Lambda Function\[images/<img width="1905" height="883" alt="Lambda Function 4" src="https://github.com/user-attachments/assets/7cc22613-684f-4529-8935-a9dd0034ea2a" />
4.  Create API Gateway\[images/<img width="1917" height="890" alt="Deploy" src="https://github.com/user-attachments/assets/d31a4525-1542-4d7d-9817-f1d93ca14249" />
4.1 Create API Gateway\[images/<img width="1913" height="888" alt="GET" src="https://github.com/user-attachments/assets/bf940d3a-3abf-44db-af74-1676f57d338b" />
4.2 Create API Gateway\[images/<img width="1919" height="881" alt="POST" src="https://github.com/user-attachments/assets/1ef33752-d697-4e89-aa04-d2c340f4dcbb" />
5. Output <img width="1919" height="989" alt="Output" src="https://github.com/user-attachments/assets/2c939a96-7c1a-43b6-a4be-b81f2a23db9e" />
5.1 Output <img width="1915" height="984" alt="Output1" src="https://github.com/user-attachments/assets/39c39aa3-12d3-4664-a3fe-3075a544a5bf" />
## 🛡 Security Notes

-   Use least privilege IAM in production\
-   Add input validation\
-   Use WAF / API Keys for public deployment

## 📚 References

-   AWS Lambda Docs\
-   AWS API Gateway Docs\
-   AWS DynamoDB Docs

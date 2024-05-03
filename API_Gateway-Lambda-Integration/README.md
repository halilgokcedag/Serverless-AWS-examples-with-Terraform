# Simple Lambda and API Gateway Project

This project demonstrates a simple serverless application using AWS Lambda and Amazon API Gateway. 
[AWS Lambda Reference Architectures](https://aws.amazon.com/lambda/resources/reference-architectures/)


## Architecture

The application consists of:

- A Node.js Lambda function that responds to HTTP requests. The Lambda function is defined in `lambda.tf`.
- An API Gateway REST API that acts as the public endpoint for the application. The API Gateway REST API is defined in `api-gateway.tf`.
- IAM roles and policies to grant the necessary permissions to Lambda and API Gateway.

## Getting Started

1. Clone this repo
2. Connect to AWS if not already authenticated by running `aws configure`
3. Deploy the Lambda function and API Gateway resources using the Terraform commands
4. Test the API endpoint in a browser or with curl

## Lambda Function

The Lambda function is defined in `index.js`. Lambda resources are defined in `lambda.tf`. It uses the AWS SDK to log invocation details to CloudWatch Logs.

## API Gateway

The API Gateway REST API is defined in `api-gateway.tf`. It exposes a POST method that integrates with the Lambda function.

## IAM

Required IAM role and Policy Attachment are defined in the Terraform resurces.

## Deployment

Resources are deployed using Terraform. The state file is stored locally for simplicity. Deploy the resources with Terraform commands:

- `terraform init`
- `terraform plan`
- `terraform apply`

This will create the necessary resources in your AWS account.

## Testing

Navigate to the API Gateway service, select the created API resource, and run a test in the API Gateway service page. 

You can test the API by navigating to the Invoke URL in Postman or using curl. Find the Invoke URL in the related Stages section of the API Gateway service. Logs will be sent to CloudWatch for troubleshooting.

Let me know if any part of the README needs more explanation or if you have additional questions!

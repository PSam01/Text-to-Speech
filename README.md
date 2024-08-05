# Text-to-Speech Project

This project demonstrates how to build a text-to-speech application using Amazon Polly, AWS Lambda, and other AWS services. The application converts text into lifelike speech and stores the audio files in an Amazon S3 bucket.

## Features

- Convert text to speech using Amazon Polly
- Store and retrieve audio files in Amazon S3
- Use AWS Lambda functions for asynchronous processing
- Manage application state with Amazon DynamoDB
- Notify components using Amazon SNS

## Prerequisites

- AWS account
- AWS CLI configured
- Basic knowledge of AWS services such as Lambda, S3, DynamoDB, and SNS

## Preview

![Στιγμιότυπο οθόνης (190)](https://github.com/user-attachments/assets/864adc86-8814-427b-a0bc-badc89aa51a6)

## Setup

### 1. Create an S3 Bucket

Create an S3 bucket to store audio files. Make sure to enable public access if necessary.

### 2. Create an SNS Topic

Create an SNS topic to notify when new text is processed.

### 3. Create an IAM Role

Create an IAM role with the necessary permissions for the Lambda functions. The policy should include permissions for Polly, S3, DynamoDB, and SNS.

### 4. Create Lambda Functions

Create two Lambda functions:

- **Text Processor**: Converts text to speech using Amazon Polly.
- **Notification Handler**: Handles notifications and updates the DynamoDB table.

### 5. Create a DynamoDB Table

Create a DynamoDB table to store the state of the text processing (e.g., text, status, audio file URL).

### 6. Deploy the Application

Deploy the Lambda functions and configure the triggers and permissions.

## Usage

1. Submit text to the application.
2. The Text Processor Lambda function converts the text to speech and stores the audio file in S3.
3. The Notification Handler Lambda function updates the DynamoDB table and sends a notification via SNS.

## Resources

- AWS

## License

This project is licensed under the MIT License.

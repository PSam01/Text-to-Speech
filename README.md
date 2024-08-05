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

## How to use the application
1. Write something in the text section.
2. Choose Voice (The accent of the voice in which your message will be delivered).
3. Press the button "Say it!" and wait for the Post ID to appear (Next to the button "Say it!").
4. Copy the Post ID and paste it here 'Provide post ID which you want to retrieve:'.
5. Press the button search, wait some seconds and the audio is going to appear below.
6. Finally you can press the play button to hear your text, at the accent you chose.

## Resources

- AWS

## License

This project is licensed under the MIT License.

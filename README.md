# policy-recommendation-engine
nagakirankasi.github.io/policy-recommendation-engine

A serverless health insurance policy recommendation engine that suggests policies based on user inputs like age, medical history, and family coverage needs. 
This project will help you get hands-on experience with AWS Lambda, API Gateway, DynamoDB, Step Functions, and SageMaker.

# Key Technologies used
- AWS Lambda: Understand function triggers, execution, and IAM roles.
- Amazon DynamoDB: Learn about NoSQL databases, tables, and querying.
- AWS API Gateway: Explore RESTful API creation and integrations with Lambda.
- AWS SageMaker: Introduction to ML model training and deployment.
- AWS Step Functions: Learn how to orchestrate workflows using Step Functions.

# Project Plan
1. Define the policy recommendation criteria (e.g., age, health conditions, budget).
2. Design the data schema for DynamoDB (e.g., policy_id, policy_name, age_range, premium, coverage, conditions).
3. Choose an ML model for recommendations (basic rule-based logic or a lightweight ML model using SageMaker).

# Setting up the Backend
4. Create the Insurance Policies Database
   Set up a DynamoDB table with attributes:
   policy_id (Primary Key)
   policy_name
   age_range
   premium
   coverage
   health_conditions
   Insert sample policy data using AWS Console or Python (Boto3).
5. Develop the Policy Recommendation Logic
   Create an AWS Lambda function to:
   Take user input (age, health conditions, budget).
   Query the DynamoDB table for matching policies.
   Return recommended policies in JSON format.
   Deploy the Lambda function and test it manually.
6. Create API Gateway Endpoint
   Set up an API Gateway to expose the Lambda function.
   Configure the API Gateway method (POST) and request/response handling.
   Deploy and test the API using Postman or Curl.

# ML Model Integration with AWS SageMaker
7. Build a Simple ML Model
   Create a dataset with historical policy selections and user profiles.
   Train a basic recommendation model using Amazon SageMaker (e.g., Random Forest, XGBoost).
   Save and deploy the trained model as an endpoint.
8. Connect SageMaker Model to Lambda
   Modify the Lambda function to call the SageMaker inference endpoint.
   Use the ML model’s predictions to recommend policies.
9. Automate with Step Functions
   Use AWS Step Functions to:
   Collect user input.
   Query DynamoDB.
   Call SageMaker for recommendation.
   Return a response to the user.

# Testing
10. Testing & Debugging
    Test the API with various user inputs.
    Handle edge cases (e.g., no matching policies, invalid inputs).
    Enable CloudWatch logs for Lambda debugging.
11. Deploy the Application
    Configure IAM roles and permissions for secure API access.
    Set up an AWS Cognito user authentication (optional).
    Deploy the project and document the API usage.
12. Enhancements & Portfolio Showcase
    Add a frontend UI (React or Next.js) to interact with the API.
    Host the frontend on AWS Amplify or S3 with CloudFront.

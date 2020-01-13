# serverless-microservices

Serverless Micro service(s) architecture overview:
AWS API Gateway <--> AWS Lambda <--> AWS Dynamo DB

This project includes the following files and folders:

- src - Code for the application's Lambda function.
- events - Invocation events that you can use to invoke the function.
- \_\_tests__ - Unit tests for the application code.
- template.yml - A SAM template that defines the application's AWS resources.
- buildspec.yml -  A build specification file that tells AWS CodeBuild how to create a deployment package for the function.

Automated CI / CD set up and process setps:
● Code repository would be either AWS codeCommit or GitHub 
● AWS CodeBuild builds code automatically when code check in happens 
● Verify automatic test codes and release artifacts into S3 bucket
● AWS CodeDeploy geenrates GenerateChangeSet and executes ExecuteChangeSet steps.
● AWS CodePipeline use to automate the CI/CD process from repositories changes trigger, build, and deployment without any manual intervention.

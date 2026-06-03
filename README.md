*Static Website Deployment to AWS S3 using GitHub Actions*
Project Overview

This project demonstrates a CI/CD pipeline that automatically deploys a static website to Amazon S3 using GitHub Actions.

Whenever code is pushed to the main branch, GitHub Actions automatically uploads the latest website files to the S3 bucket.


Architecture

GitHub Repository
↓
GitHub Actions
↓
AWS S3 Bucket
↓
Static Website Hosting

Technologies Used
GitHub Actions
AWS S3
IAM User & Policies
AWS CLI
HTML/CSS/JavaScript

Features
Automated deployment using GitHub Actions
Secure AWS authentication using GitHub Secrets
Static website hosting on Amazon S3
Automatic synchronization of website files
CI/CD implementation

GitHub Actions Workflow - The workflow is triggered whenever code is pushed to the main branch

Deployment Command
aws s3 sync . s3://YOUR_BUCKET_NAME --delete
GitHub Secrets

Configure the following secrets:

AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_REGION
S3_BUCKET_NAME

Deployment Steps-
Create an S3 bucket.
Enable Static Website Hosting.
Create an IAM user with S3 permissions.
Store AWS credentials in GitHub Secrets.
Create a GitHub Actions workflow.
Push code to the main branch.
GitHub Actions automatically deploys the website.

I used GitHub Actions to automate deployment of a static website to Amazon S3. Whenever code is pushed to the main branch, the workflow is triggered automatically. It authenticates with AWS using GitHub Secrets and deploys the website using aws s3 sync. For this project, GitHub Actions was a better choice than Jenkins because it required no server management and integrated directly with GitHub


# Deploying-a-Static-Website-on-AWS
## Project Overview
This project focuses on:

 1. Hosting a static website on S3
 2. Accessing the cached website pages using CloudFront content delivery network (CDN) service with error page implemented.

**The steps I took to achieve this**:
 
- Creating a public S3 bucket and upload the website files to your bucket.
- Configuring the bucket for website hosting and secure it with IAM policies.
- Speed up content delivery using AWS's content distribution network.
- Ensure website is accessible.

### Prerequisites for this project are:
 1. An AWS account
 2. Website (any language)

 ## Steps on how this was performed
 ### Step 1: Creating an S3 bucket
 Naviggating to Amazon S3 from the AWS management console, I created an S3 bucket. I also allowed public access so that the website could be accessed from anywhere on the web.
 ![s3_creation](https://user-images.githubusercontent.com/106401088/188764735-58909d0b-a571-4209-b8f8-ec6c57e330bb.PNG)
 ![s3_access](https://user-images.githubusercontent.com/106401088/188764729-d68f5960-7734-47bd-9c87-8f244844269a.PNG)
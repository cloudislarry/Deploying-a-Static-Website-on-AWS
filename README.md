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
 Navigating to Amazon S3 from the AWS management console, I created an S3 bucket. I also allowed public access so that the website could be accessed from anywhere on the web.
 ![s3_creation](https://user-images.githubusercontent.com/106401088/188764735-58909d0b-a571-4209-b8f8-ec6c57e330bb.PNG)
 ![s3_access](https://user-images.githubusercontent.com/106401088/188764729-d68f5960-7734-47bd-9c87-8f244844269a.PNG)

 ###  Step 2: Upload Website files
 Once the S3 bucket is created, I uploaded the website files into it.
 ![s3_upload](https://user-images.githubusercontent.com/106401088/188764737-05a38662-2b9b-43eb-ab98-8a43502eb0b7.PNG)

 ### Step 3: Enable Static Website Hosting
 I enable static website hosting and made the contents of the index.html file accessible by the view in order to be read at the website endpoint.
 ![s3_static](https://user-images.githubusercontent.com/106401088/188764750-679487ca-40b2-4732-8de8-c264ab0e0c98.PNG)
 ![s3_static2](https://user-images.githubusercontent.com/106401088/188764752-04281559-526d-4f06-9226-ba7a60046e5e.PNG)

### Step 4: Secure your S3 with your IAM policy.
For static website hosting, it is required to make buckets public.
![s3_policy](https://user-images.githubusercontent.com/106401088/188764736-4808dd6f-c434-430a-a335-ea766a17d4b4.PNG)

### Step 5: Distributing Website via CloudFront

I created a CloudFront distribution which attached to the S3 and S3 caching pages.
![s3_cloudfront](https://user-images.githubusercontent.com/106401088/188764731-27cda9b3-c24d-4437-b8b0-db6100e19ce5.PNG)

### Step 6: Accessing website in web browser
Pasting the CloudFront domain name in a web browser even without the index.html at the end displayed the content of the default home page.
![s3_cloudfrontpage](https://user-images.githubusercontent.com/106401088/188764732-b3f1f8b9-23eb-449c-bb36-582041e38e91.PNG)

Also, the website can also be accessed through the website-endpoint and S3 object URL.
![s3_regular](https://user-images.githubusercontent.com/106401088/188764747-ff460fb7-f8ab-4c22-b1b1-1bfce62ce33a.PNG)
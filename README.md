# AWS Static Website Hosting

This project demonstrates how to host a static website on AWS S3.

## Project Structure

- `index.html` - Main landing page.
- `styles.css` - CSS file for styling.
- `aws-s3-config.json` - Configuration file for AWS S3 bucket setup (optional).
  
## Hosting Steps

1. **Create an S3 Bucket:**
   - Create a new S3 bucket with a unique name.
   - Enable static website hosting in the bucket properties.

2. **Upload Files to S3:**
   - Use the AWS Management Console or AWS CLI to upload `index.html`, `styles.css`, and other static files to the S3 bucket.
   - Example CLI command:
     ```bash
     aws s3 cp . s3://your-bucket-name/ --recursive
     ```

3. **Set Bucket Permissions:**
   - Set the bucket policy to allow public access to the website files.

4. **Access the Website:**
   - The static website is accessible via the S3 bucket's URL.

## Deployment Commands

- Upload all files to S3:
  ```bash
  aws s3 sync . s3://your-bucket-name/ --acl public-read

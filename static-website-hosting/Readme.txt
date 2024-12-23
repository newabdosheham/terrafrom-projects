Project Description: Terraform Static Website Hosting on AWS S3

This Terraform project sets up the infrastructure to host a static website on AWS S3 with public access. Below is a detailed description of the resources and their purposes:
1. AWS S3 Bucket (aws_s3_bucket)

    Purpose: Creates a dedicated bucket to store the website's files.
    Configuration:
        The bucket is named abdosheham-terraform-project-static-website3.
        This bucket serves as the main storage for the website content, including HTML files.

2. Public Access Block (aws_s3_bucket_public_access_block)

    Purpose: Configures public access settings for the bucket.
    Configuration:
        Public access is allowed by setting all block options (block_public_acls, block_public_policy, etc.) to false.

3. Website Files (aws_s3_object)

    Purpose: Uploads the HTML files (index.html and error.html) to the S3 bucket.
    Configuration:
        index.html is the main entry point for the website.
        error.html is displayed for error cases, such as 404 (page not found).
        Both files are stored with the correct content_type (text/html).

4. Website Configuration (aws_s3_bucket_website_configuration)

    Purpose: Enables the S3 bucket's website hosting feature.
    Configuration:
        index.html is set as the default page (index document).
        error.html is configured to handle error scenarios.

5. Bucket Policy (aws_s3_bucket_policy)

    Purpose: Grants public read access to the S3 bucket.
    Configuration:
        Defines a policy that allows s3:GetObject permissions for all objects in the bucket.
        Ensures anyone can access the website files over the internet.

Features of the Project:

    Fully Automated: Automates the setup of a static website using Terraform.
    Public Access Control: Includes a bucket policy to enable public read access.
    Error Handling: Configures a custom error page for better user experience.
    Reusable Code: Can be extended or reused for similar static website projects.

This project is ideal for hosting a lightweight, static website without the need for server-side processing. Let me know if you need further details or enhancements!

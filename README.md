# cc-test-app
A test web application hosted on AWS Amplify.

1.  Url:  https://master.dkwj1b38ijbss.amplifyapp.com/

2. If you change index.html file at the root in this repository and check-in, the build will automatically kick-in and it will be deployed. 
On the above web-page you will see the change.

3. AWS Amplify is a shrink wrapped solution from AWS for Single Page Application (APA). The code (index.html, the static page) is stored in
a S3 bucket. There is NO AWS Lambda or Web Server running in this case. The page is actually cached in AWS CDN backed by Cloudfront. 

4. Since Ammazon CDN - Cloudfront - is scalable, this application simply piggyback on that; being a simple static page.

5. The DNS is default, using Amazon Certificate and that is how security is achieved. The DNS can be changed to any custom value in Amplify Studio.

6. Given the simplicity of the applcation, practically no Infrastructure Code is needed for this use case. However, you can see the Stack(s)
created for this app in CloudFormation. Various resources are (like S3 bucket or various AWS IAM Roles needed) listed.

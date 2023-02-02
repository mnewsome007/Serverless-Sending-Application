<h1>Static Website Hosting</h1>


<h2>Description</h2>
This project will guide you in hosting a static website on AWS. You will learn the steps of importing a domain name on AWS, creating a hosted zone and managing its DNS records, creating S3 buckets to host website pages, configuring Route 53 to link the domain name to the website, creating an SSL certificate for the website using AWS Certificate Manager (ACM), and creating CloudFront distributions to secure the website in HTTPS. By completing this project, you will have a comprehensive understanding of how to host a static website on AWS and the various tools and technologies involved in the process.
<br />

<h2>AWS Cloud Map</h2>
<p align="center">
<img src="https://i.imgur.com/rYKC5x2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />


<h2>Services Used</h2>

- <b>Amazon S3</b> 
- <b>API Gateway</b>
- <b>AWS Lamnda</b>
- <b>AWS Step Functions</b>
- <b>Amazon SNS</b>
- <b>Amazon SES</b>

<h2>Environments Used </h2>

- <b>AWS Management Console</b>
- <b>Software Development Kit (SDK)</b>
- <b>Python</b>

<h2>Serverless Sending Application walk-through:</h2>

- <b>Within Identity and Access Management (IAM) create a Lambda role with AWS Service as the selected trusted entity</b>
- <b>Create Lambda Function from scratch using Python in the Code source menu; AWS utiilizes "boto3" SDK toolkit to interact with Python</b>
- <b>Import "boto3" library inside your code and define the services to be interacted with (SES); define the lambda function to be used and in this case "send_email" will be used</b>
- <b>Add the variables "Source" , "Destination" , "Message" to your code </b>
- <b>Deploy and test the code</b>
- <b>Within Identity and Access Management (IAM) create a Lambda role by using an exisitng role</b>
- <b>Now utilize Code source and import "boto3" library inside your code and define the services to be interacted with (SNS); define the lambda function to be used and in this case "publish" will be used</b>
- <b>Add the variables "PhoneNumber" , "Message" to your code</b>
- <b>Deploy and test the code</b>
- <b>Within Step Functions create a state machine by writing your workflow in code</b>
- <b>Now add the ARN's of the Lambda functions "email.py and sms.py" to the corresponding states</b>
- <b>Name the state machine to finalize the creation</b>
- <b>Launch the execution</b>
- <b>Create another Lambda function from scratch for the API Handler</b>
- <b>Now utilize Code source and import "boto3" library inside your code and define the services to be interacted with (SFN); define the lambda function to be used and in this case "start_execution" will be used</b>
- <b>Add the variables "stateMachineArn" to your code</b>
- <b>Copy the ARN of the previously created state machine to your code</b>
- <b>Deploy and test the code</b>
- <b>Create a REST API using API Gateway</b>
- <b>Deploy the API</b>
- <b>Create/code a static website and upload it to S3</b>
- <b>Test the website and try sending an email and a SMS</b>




<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>

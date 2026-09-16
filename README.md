Name: Abdulazeez Adeniyi

Role: Student

Project: AWS Compute Hands-On Project
1. Introduction
The AWS Compute Hands-On Project was designed to provide practical experience with different AWS compute services. The project involved deploying and managing EC2 instances, connecting to an EC2 instance, configuring Auto Scaling and Load Balancing, deploying a serverless Lambda function, and preparing an application for deployment with AWS Elastic Beanstalk.
The project helped me understand how AWS compute services can be used to build applications that are scalable, available, and easier to manage.
2. Objectives
The main objectives of the project were to:

Launch and manage an Amazon EC2 instance.
Connect to an EC2 instance using SSH.
Configure an Auto Scaling Group and Load Balancer.
Deploy and test a serverless AWS Lambda function.
Understand application deployment using AWS Elastic Beanstalk.
Gain practical experience using the AWS Management Console.

3. EC2 Instance Deployment
I started by navigating to the Amazon EC2 service in the AWS Management Console. I launched an EC2 instance using an appropriate Amazon Machine Image and instance type.
I configured a key pair for secure access and created a security group that allowed the required traffic, including SSH on port 22 and HTTP on port 80 where necessary.
Security group: project2-app-sg
The inbound rule allowed TCP traffic on port 80. The outbound rule allowed all traffic to 0.0.0.0/0.

After launching the instance, I monitored its status to confirm that it was running successfully.
4. Connecting to the EC2 Instance
After launching the EC2 instance, I connected to it using SSH and the configured key pair.
I verified that the connection was successful by running:
uname -a
This confirmed that I had successfully established a remote connection to the Linux-based EC2 environment.
5. Auto Scaling and Load Balancer
The next stage involved creating an Auto Scaling Group and configuring a Load Balancer.
The Auto Scaling Group was configured to manage EC2 instances automatically. This provides the ability to maintain the required number of instances and replace unhealthy instances when necessary.
I also worked with an Application Load Balancer and target group to distribute incoming application traffic across the available EC2 instances.
This stage helped me understand the relationship between EC2, Auto Scaling Groups, target groups, and Application Load Balancers.
6. AWS Lambda
I then deployed a serverless function using AWS Lambda.
I created a Lambda function from scratch and selected Python as the runtime. The function was configured with the following code:
def lambda_handler(event, context):
return {
'statusCode': 200,
'body': 'Hello from AWS Lambda!'
}
Function name: hello-aws-lambda

Package type: Zip

Runtime: Python 3.14

Type: Standard

After deploying the function, I created a test event and executed the function.
The successful execution returned a status code of 200 and the message:
Hello from AWS Lambda!
This demonstrated how AWS Lambda can execute application logic without requiring me to manage a traditional server.
7. Elastic Beanstalk
The final section of the project involves deploying an application using AWS Elastic Beanstalk.
The process involves creating an Elastic Beanstalk application, selecting an appropriate platform such as Node.js or Python, and deploying application code to an environment managed by Elastic Beanstalk.
This section demonstrates how AWS can simplify application deployment by managing underlying infrastructure and deployment resources.
8. Conclusion
The AWS Compute Hands-On Project gave me practical experience deploying and managing different AWS compute services.
I learned that AWS provides multiple approaches to running applications, from directly managing EC2 instances to using Auto Scaling, Load Balancers, serverless Lambda functions, and managed deployment platforms such as Elastic Beanstalk.
Overall, the project provided a strong practical foundation for working with AWS compute infrastructure as a DevOps engineer.

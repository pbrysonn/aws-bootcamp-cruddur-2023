# Week 0 — Billing and Architecture
For Week 0 I was successfully able to go through all the tutorial videos created. From this, I've been able to carry out the following skills;
-Create AWS account and set aside root user access. Made use of MFA to secure my account with both root user and admin user.
-Had a basic understanding of 6 key security practices and understood the goal and need of security with regards to AWS 
-Reviewed and created a pdf with the AWS well architected tool to analyze best practices
-Created and Architectural diagram of the CI/CD pipeline of our crunchr application using LUCID CHARTS
-Realized a napkin concept of our business Idea
-Practiced how to make use of AWS free-tier and understand how to track spend in AWS. To do this, I practiced with the following AWS services as well(AWS Budgets, AWS Cost Explorer, Billing Alarms)
-Had my first go at monthly billing reports
-Used Cloudshell to securely access AWS 
-Generated AWS Credentials, used access keys to access AWS services from gitpod.
-Successfully created topics and made use of the SNS service to receive notifications. 

Watched the hands-on video showing how to use the CLI to create a budget and as well to create sns topics but I am still trying to get the hang of the whole process. Will eventually be able to replicate the command line codes in the following days and do these tasks from the CLI.

## CLOUD ARCHITECTURE
Here, we were able to understand what good architecture is, and the main take away of this was that Good architecture should address risks, assumptions and constraints. Also, that when considering risks, we should make use of the iron triangle (Fast, cheap or Good). 

## WELL ARCHITECTED FRAMEWORK TOOL
This tool consists of 6 main pillars, we can use these as a guide to ensure that we adhere to AWS best practices while designing our infrastructure on AWS. These pillars include
1. **Operation Excellence**
2. **Security**
3. **Reliability**
4. **Performance Efficiency**
5. **Cost Optimization**
6. **Sustainability**
Each of these pillars has questions which we can answer and use as a guide to ensure that we are following the best practices while deploying our applications in the cloud. At the end, we can download a pdf of the results and receive a grading of our Performance. 

## AWS Console 

### Creating AWS Account
- To create our AWS account, we needed an email and a password. This automatically gives us what we refer to as the root user. 
- To adhere to an AWS security best practice, I was required to keep aside my root user and create an admin user, with admin permissions, which i will use to carry out the various activities in my account. This is because the admin user is the power user and a loss of these credentials could lead to the loss of my account
- Made use of **MFA** to secure both users. 
- Also learned about Federated users 

### IAM 
- We had a rundown of the IAM console
- This included handson of the various IAM IDENTITIES(users, roles, groups)
- We also learned of the various IAM COMPONENTS(users, roles, groups, policies)
- Learned of the two types of policies, customer managed and aws managed policies 

### Tracking Spend/Billing
1. **AWS FREE TIER**: Made use of this to understand the different services AWS offers for free. Realized some are free forever, others just for a year. Some are free based on the number of runnings hours. 
2. **Billing Alert(CloudWarch Alarm & Budget)**: 
- Here, I made use of **CLOUDWATCH**. I had to make sure that I was  in the N Virginia region as it’s only within this region that we can work on this. It involved creating an SNS topic if we don’t have one already and assigning the endpoint ID. This procedure involves creating a metric. For free, we are able to set 10 cloudwatch alarms
- I made use of Budgets to receive notifications if I passed any spending thresholds. It exists under the cost exploer section. Here we are able to setup budgets for our account. It's important to note that an alarm only sends notifications when a threshold condition is met, but with budgets Youcan get a forecast of your spending, and avoid to any circumstances of overspending beforehand.. Here do not setup more than 2 budgets in order to remain in the free tier. You will be notified when *your actual spend is greater than 85%, your forecasted spend is greater than 100% and when the actual spend is greateer than 100%*
3. **Calculate AWS Estimates Cost for Services**: We did this using the AWS Cost Calculator.
4. **Cost Allocation Tags**: This is done in the cost allocation tags section under billing. You have to activate the tags here before AWS starts tracking them. These can be used to organize your resources, as well as to track your AWS costs on a detailed level.

### AWS CLOUDSHELL
We gained hands-on experience on this service. This is a service that enables us to securely access AWS services using SSH. 

## Gitpod/Github
Here, we were to generate access keys on the aws console and use these to connect to our AWS services
- Learned how to save my access key variables to ease future access. 
- Also learned numerous git commands as well as linux 
- We used github to clone the primary repository needed to execute this project.

## Business Plan & Conceptual Diagrams
We discussed about how we could successfully realize our design plans step by step. This required having to come out with the ideas in a graphic nature. We passed through three steps in doing these;
1.**Conceptual Design**
- This is Created by business stakeholders and architects
- It Organizes and defines concepts and rules
- It is popularly known as the "Napkin Design"
- Here is my napkin design: ![Napkin Diagram](https://freeimage.host/i/HGzeMXa)
2. **Logical Design**
- This Defines how the system should be implemented
- Here, we include the environment without actual names or sizes
- Here is a link of the diagram I was able to design: ![Cruddur Logical CI/CD Concept](https://lucid.app/lucidchart/80785cdc-2138-4d03-8049-036331388c9b/edit?viewport_loc=-361%2C1095%2C2848%2C1666%2C0_0&invitationId=inv_832c6c02-d666-48e7-9629-04745b0c72c0)
3. **Physical Design**
- This is the representation of the actual thing that was built
- It includes IP Addresses, EC2 instances

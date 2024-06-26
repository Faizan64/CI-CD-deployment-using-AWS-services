# CI-CD-Deployment-Using-AWS-Services
Deployed a simple node js website using AWS Services

![Screenshot 2024-06-25 151152](https://github.com/Faizan64/CI-CD-deployment-using-AWS-services/assets/91891601/9cda19b1-61e3-4771-90b2-947eb11eaf3c)

## Services Involved
- AWS Elastic Beanstalk
- AWS IAM
- AWS CodeBuild
- AWS CodePipeline

### Steps
- Setup a github repo with all the requirements to run the code
- By using Beanstalk create an application and setup the Node.js environment with all the configuration
- Once the environment is created then with AWS CodeBuild create the build project
- After build create a pipeline through CodePipeline for the deployment.

## Setup a github repo
- It is simple step you just need a github account to create a ndoejs repo or can fork it.
- If you want to do this step in AWS then AWS code commit is service which lets you commit the code onto the AWS but first connect AWS to local editor then add,commit and push
- Your repo is ready for the build step

## Creating an application and setting up the Node.js environment
- In Beanstalk create an application. You just have to give a name to your app.

![beanstalk app](https://github.com/Faizan64/CI-CD-deployment-using-AWS-services/assets/91891601/63ebb0d4-5614-4aaf-901f-a552524214ab)

- Create a Node.js environment for your application by selecting your suitable platform in my case it is Node.js
- You need to create a service role for you environment and complete your basic ec2 configurations most of them are defaults and your env is ready

![Beanstalk env](https://github.com/Faizan64/CI-CD-deployment-using-AWS-services/assets/91891601/bf6d1926-06b8-4d41-a839-c956e21dc44c)

## Build project using AWS codeBuild
- Create build project and give all the details while in the source you need to give the source provider as github.
- Then it will give an option to connect to your personal repo after all the credentials.
- Select the repo you want to use in the project and your repo is connected to AWS.
- Give a new service role it will automatically creates a new service role in IAM
- Then you have to insert some build command or you can just create buildspec.yml file in your editor and your project is created.
- You can start you build and can view the build phases

![Build phases](https://github.com/Faizan64/CI-CD-deployment-using-AWS-services/assets/91891601/47df1f87-134a-409a-b3d2-3e622978f34e)

## Deploy the application
- Create a pipeline using CodePipeline
- You need a give a name and select the new service role it will create a new role for you
- Next give source as github and it will ask to connect then connect your AWS to github and select your repo.
- You need to select github webhooks because it will ensure that whenever you edit your code in the repo the pipeline will automatically build and deploy your code
- Take build provider as code build and deploy provider as beanstalk and provide application details and your good to go your pipeline is created
- You can also deploy your application with code deploy instead of beanstalk. I choose beanstalk because it is much reliable

![pipeline flow](https://github.com/Faizan64/CI-CD-deployment-using-AWS-services/assets/91891601/000ef8d6-5b90-4484-9b89-addbec725684)

- Simple website is launched you can edit the code and deploy a flashy website as well

![Website](https://github.com/Faizan64/CI-CD-deployment-using-AWS-services/assets/91891601/14910d6c-0c87-46b4-a91c-b28780a3222e)







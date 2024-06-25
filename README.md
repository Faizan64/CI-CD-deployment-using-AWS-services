# CI-CD-Deployment-Using-AWS-Services
Deployed a simple node js website using AWS Services

![Screenshot 2024-06-25 151152](https://github.com/Faizan64/CI-CD-deployment-using-AWS-services/assets/91891601/9cda19b1-61e3-4771-90b2-947eb11eaf3c)

## Services Involved
- AWS Beanstalk
- AWS IAM
- AWS Codebuild
- AWS CodePipeline

### Steps
- Setup a github repo with all the requirements to run the code
- By using Beanstalk create an application and setup the nodejs environment with all the configuration
- Once the environment is created then with AWS codebuild create the build project
- After build create a pipeline through code pipeline for the deployement.

## Creating an application and setting up the nodejs environment
- In Beanstalk create an application. You just have to give a name to your app.

![beanstalk app](https://github.com/Faizan64/CI-CD-deployment-using-AWS-services/assets/91891601/63ebb0d4-5614-4aaf-901f-a552524214ab)

- Create a node JS environment for your application by selecting your suitable platform in my case it is nodejs
- You need to create a service role for you environment and complete your basic ec2 configurations most of them are defaults and your env is ready

![Beanstalk env](https://github.com/Faizan64/CI-CD-deployment-using-AWS-services/assets/91891601/bf6d1926-06b8-4d41-a839-c956e21dc44c)

## Build project using AWS codebuild
- Create build project and give all the details while in the source you need to give the source provider as github.
- Then it will give an option to connect to your personal repo after all the credentials.
- Select the repo you want to use in the project and your repo is connected to AWS.
- Give a new service role it will automatically creates a new service role in IAM
- Then you have to insert some build command or you can just create buildspec.yml file in your editor and your project is created.
- You can start you build and can view the build phases

![Build phases](https://github.com/Faizan64/CI-CD-deployment-using-AWS-services/assets/91891601/47df1f87-134a-409a-b3d2-3e622978f34e)





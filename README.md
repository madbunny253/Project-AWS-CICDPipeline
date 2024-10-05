# Project-AWS-CICDPipeline

AWS Continuous Integration Demo
This project demonstrates how I implemented a CI/CD pipeline using AWS services to automate the build, test, and deployment of a Python application.

**Set Up GitHub Repository**
The first step was to set up a GitHub repository to store the source code of my Python application. This repository serves as the starting point for our CI/CD process.

**Create an AWS CodePipeline**
I created an AWS CodePipeline to automate the entire integration process, ensuring that any changes pushed to the GitHub repository would trigger the pipeline to build and deploy the latest code.

Steps I followed:

Navigated to the AWS CodePipeline service in the AWS Management Console.
Clicked "Create pipeline" and provided a name for the pipeline.
For the source stage, I selected "GitHub" as the source provider, connected my GitHub account, and chose the repository and branch to use for the pipeline.
Configured the build stage using "AWS CodeBuild" as the build provider. I created a new CodeBuild project with the necessary settings for my Python application, including the build environment, commands, and artifacts.
For deployment, I configured the pipeline to deploy using AWS CodeDeploy
After reviewing the configuration, I clicked "Create pipeline," and just like that, the pipeline was set up to handle automated builds and deployments.
Configure AWS CodeBuild
Once the pipeline was set up, I configured AWS CodeBuild to automate the building and packaging of my Python application:

Went to AWS CodeBuild and clicked "Create build project."
Named the project and selected "AWS CodePipeline" as the source provider.
Configured the build environment based on the requirements of my application, specifying the operating system, runtime, and compute resources.
Defined the build commands, such as installing dependencies and running tests.
Set up artifact configuration to handle the build output for deployment.
After reviewing the settings, I created the build project.
With AWS CodeBuild in place, my project was ready for automated builds each time a change was pushed to the GitHub repository.

**Trigger the CI Process**
To test the pipeline, I made a change in the GitHub repository by updating the application's source code. After committing and pushing the changes, AWS CodePipeline automatically detected the update, kicked off the build process using AWS CodeBuild, and deployed the latest version of the application.

Watching the pipeline execute the entire CI/CD process seamlessly was a rewarding experience!

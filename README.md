# Containerised Python Application on AWS EC2
This containerised Python application uses Flask. It is a simple example for AWS EC2 Demo.

My application listens flask default port 5000.

Port mapping of our application is 5000:5000

I can dockerize this flask application by using dockerfile

I can expose my application via Elastic Load Balancer

I used nginx on this project. Network traffic go through the our python container from the nginx that uses reverse proxy. 


## CICD

 I used Github Actions used for auto building docker image and deploying it to AWS EC2. when my code is on the github, it is so easy to integrate with CI/CD by using github action. There are many predefined github action modules. By referring these modules, I can easily integrate with CI/CD. 
 
 You can find pipeline yml in the .github/workflows/flask.yml
   
   When your environment has many platforms such as AWS,Google Cloud,Openshift, I suggest you should use jenkins CI/CD tool. Because, Jenkins have so many plugins that integrate with so many platforms (AWS,Azure,Openshift,GKE etc). When your environment has only AWS platform, also, you can use AWS Codebuild,Codedeploy,Codepipeline resources. Your github account can easily sync to AWS and you can easily integrate our code with  codepipeline.  

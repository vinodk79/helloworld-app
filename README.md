# helloworld-app

A HelloWorld Application

I have created a simple node js application by creating a docker image and deploying it on AWS EKS. I have created server.js for the Helloworld application and package.json file for node server. The deployment.yaml is set up for deployment into EKS Cluster and service.yml is for exposing the kubernets services in EKS cluster which was done by using load balancer and exposed on port number 4001. 

I have set up the github actions workflow in the main.yaml file where it has all the build steps and jobs that are used for creating the docker image and deploying it on AWS EKS.

All the required credentials/access to complete the deployment are set up using the environment varibles in github secrets.
Here are the steps to deploy it:

1. Any change in the code will automatically trigger the Build in " Actions" section.
2. To do a quick deployment, Please find the server.js file in the source and click edit
3. Change the line 7 in server.js file which is "response.end('Hello world!\n')" to any reponse that you want. for example "response.end('Hello World Application\n')
4. Once the changes have been made, click "commit changes" in bottom 
5. Now it will trigger a workflow run in "Actions" section 
6. Click the latest workflow run and wait until all the taks have been completed.
7. Once All the tasks are completed , you can view your changes by accessing the Application URL below.

Application URL: http://ab4185e99876b47d7a94872b5e9e96b1-424315540.ca-central-1.elb.amazonaws.com:4001/

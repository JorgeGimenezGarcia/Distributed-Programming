# Distributed-Programming
In this repository i uploaded all my works that I used Distributed-Programming.
In this projects we scaled the projects and it started from the most easy way to configure a distributed-Programming to using Docker with Amazon Services.
All this projects are implemented on a Linux OS ubuntu server. In the last practice I used some EC2 from Amazon for the deployment.


# First Project: Connection between 2 machines creating the Server-Client version. It is written in C++. 
- There are 2 projects, the multmatrix and filemanager.
* Multmatrix: This can create random matrix, identity matrix or with your own values. And you can make also mutliplications with those matrix and the results will be saved on a txt in the server.
* Filemanager: This will create a service to manage the files, you can read the documents, write on them or delete them.
This Project was implemented using 2 virtual machines on VirtualBox.

# Second Project: Using Docker and Kubernetes to create a master/slave connection with multiple pods.
For the implementation of this project I started to use the Amazon Services to create two EC2 instances of Ubuntu Servers to create the connection master/slave.
*Important aspects for the creation of these services.
*- The ports for docker and kubernetes, the ports of http and ssh must be open to create all this connections.

- In this project we used the same code that I used in the first Project, the difference is that I implemented this to make the Docker implementation.
- For the filemanager I created three pods, because I wanted to implement a sshfs( File system to connect all the files between all pods and not create the same files in each pod) but I did not have enough time to implement it. But in the three pods you will have the files that you can do the same things like before.
- For the multmatrix I created two pods.

# Third Project: Using Docker and Kubernetes to create an Apache Service with a MariaDB database and Amazon Services.
This is the most completed Project, because I used what a learned of Kubernetes before and I implemented a unique pod that deploys an Apache Server and a database creation with MariaDB. 
I used the Amazon Services to use one of the EC2 instances before to deploy all this project in that instance. I also used Lambda functions, API Gateways and S3 connections for all the functionality that this project had.
*This project is based in create an applicaction similar to Youtube. We will have users that want to upload videos to the community. And they can manage their own videos to delete them or to upload them. All the users can see all the videos that all the users create.*
I created three Lambda functions with their own API Gateway.
*All this lambda functions were written in Python and using some extra libraries like pymsql or boto3.
1º) Login/Register: The creation or login of the users in the application.
2º) VideosCheck: The get,delete, post functions that a user can do with their own videos.
3º) AWSCredentials: To use the S3 service, we need to refersh and use your own creedentials to use this service.

# SuperMario-ECS
Deploying Super Mario Game on AWS Elastic Container Service (AWS ECS)

First create a security group for the AWS ALB with just the http port opened to the public, just like the below snap.

<img width="1100" height="490" alt="image" src="https://github.com/user-attachments/assets/9e3761a4-9aa1-4e9c-a3e9-ff0fa5904c59" />

Next create a security group for the ECS Container. Here we will be opening the port 8080, that too we are just allowing the LoadBalancer group to access the port. All other entries will be restricted.
<img width="1100" height="485" alt="image" src="https://github.com/user-attachments/assets/62f21f1b-9649-4384-be09-4237554de900" />

For LoadBalancer we will need a target group. Click on create target group and make sure to select IP Addresses from the Basic Configuration.

<img width="715" height="570" alt="image" src="https://github.com/user-attachments/assets/09472047-4e6c-48d9-8523-963b8339352f" />

In the protocol select http, so that it will be listening to 80 Port requests.

<img width="627" height="566" alt="image" src="https://github.com/user-attachments/assets/e994a424-d9f0-4716-9a6d-02a8ac3fd263" />

Let us create the ECS Cluster.

<img width="719" height="538" alt="image" src="https://github.com/user-attachments/assets/ad71b820-a3f9-4a43-8f81-5d215bee6f54" />

<img width="862" height="576" alt="image" src="https://github.com/user-attachments/assets/e6e3f17b-faca-4a66-9ab2-a8f87f0a9fc2" />

Name your container, in the image URI give the image we selected earlier. That is kaminskypavel/mario.

<img width="863" height="571" alt="image" src="https://github.com/user-attachments/assets/3a3bd321-b836-4f68-91e4-b0d376ce6d5a" />

<img width="640" height="625" alt="image" src="https://github.com/user-attachments/assets/7bfb8b8a-6de3-4e45-81fc-e3c1a49fd1fa" />

Click on Create Service.

In the Cluster section, go to the services.

<img width="1054" height="535" alt="image" src="https://github.com/user-attachments/assets/31d93804-846b-4002-84df-2e1a94be69da" />

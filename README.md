# Reddit Clone App on Kubernetes with Ingress
This project demonstrates how to deploy a Reddit clone app on Kubernetes with Ingress.

## App Credit
This application is developed by [Shadee Merhi](https://github.com/shadeemerhi), and complete code of the application can be seen at [reddit-clone-yt](https://github.com/shadeemerhi/reddit-clone-yt.git). 
 

## Prerequisites
To deploy the application on Kubernetes, one should have the following tools installed on the machine (local or remote vm): 

- Docker
- Kubernetes/Minikube cluster (Running)
- kubectl
- Git

# App Deployment Steps on K8s  
Following are the steps to deploy the Reddit Clone App on Kubernetes/Minikube cluster: 

## Step 01: Clone the App Code 
Clone the application code to the machine. 

`git clone https://gitlab.com/asadhanif3188/devops-project-reddit-clone-app-kubernetes-with-ingress.git`

## Step 02: Dockerfile 
Add a Dockerfile, in case it is not already added. 

```
FROM node:19-alpine3.15

WORKDIR /reddit-clone

COPY . /reddit-clone
RUN npm install 

EXPOSE 3000

CMD ["npm","run","dev"]
```



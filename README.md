# Capstone_Project

![image](https://user-images.githubusercontent.com/60229601/154626757-54439171-8251-4a9c-a35d-6a985810e6c3.png)

# Scope: 

The scope of the project is to display my webpage for the successful completion of the Udacity Nano Degree Capstone Project. 

# Approach: 

>> Amazon EKS was utilized for creating the cluster using eksctl utility as it is able to create a cluster within minutes with a single command. It uses AWS CloudFormation.

>> Docker was used for containerization of the application.

>> Rolling deployment strategy was utilized to move from preliminary version to the final version of the App.

>> CIRCLECI was employed for CICD pipeline creation.

>> Captured the linting error as the project requirement advised. 

# SetUp

AWS Cloud9

arn:aws:cloud9:us-east-1:116916132946:environment:9bc39d39a5214f35b2f18db3aa5f741d

Amazon EKS Cluster 

eksctl version 0.83.0 for creating Kubernetes Cluster

      Config yaml file - ./kube/cluster.yaml

      Command => eksctl create cluster -f cluster.yaml

IAM Role for the Kubernetes Cluster

      eksctl get iamidentitymapping --cluster mycluster
      
      eksctl create iamidentitymapping --cluster  mycluster --arn arn:aws:iam::106876110629:role/eksctl-mycluster-cluster-ServiceRole-TW8D1GYOMCIB --group system:masters --username Admin

Environment Variables used:

AWS_ACCESS_KEY_ID

AWS_SECRET_ACCESS_KEY

AWS_DEFAULT_REGION

DOCKERHUB_PASSWORD

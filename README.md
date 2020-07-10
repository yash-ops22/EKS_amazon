# EKS_amazon: 
# Kubernetes
 Kubernetes is an open-source container-orchestration
 system for automating computer application deployment, 
 scaling, and management. It was originally designed
 by Google and is now maintained by the Cloud Native
 Computing Foundation.

# Elastic Kuberntets Service
   Amazon Elastic Kubernetes Service (Amazon EKS) is
   a managed service that makes it easy for you to 
   run Kubernetes on AWS without needing to stand 
   up or maintain your own Kubernetes control plane.
   Kubernetes is an open-source system for automating
   the deployment, scaling, and management of containerized 
   applications.
   Amazon EKS runs Kubernetes control plane instances across
   multiple Availability Zones to ensure high availability.
   Amazon EKS automatically detects and replaces unhealthy 
   control plane instances, and it provides automated version 
   upgrades and patching for them.
   
   # Drupal
    
   Drupal is a free and open-source web content management
   framework written in PHP and distributed under the GNU
   General Public License. Drupal provides a back-end
   framework for at least 2.3% of all websites worldwide 
   – ranging from personal blogs to corporate, political,
   and government sites
   
   # Starting with the task
   
   # IAM 
   
   First we have to create IAM user which I have already created.
   
   #  Key Pairs
   
   Creating key pairs for using in our instances.
   
   # AWS Configure
   
   Configuring aws profile in from our command line.
   
   
   # EKS Cluster
   For this we have to configure eksctl, official command of AWS EKS.
   
  Launching our eks cluster on amazon cloud.
  
      apiVersion: eksctl.io/v1alpha5
      kind: ClusterConfig

      metadata:
        name: eks-cluster
        region: ap-south-1

      nodeGroups:
      - name: firstnodegroup
        desiredCapacity: 3
        instanceType: t2.micro
        ssh:
          publicKeyName: ekscloudkey22

     - name: secondng
       desiredCapacity: 3
       instanceType: t2.micro
       ssh:
         publicKeyName: ekscloudkey22
  
  Creating cluster with command 
  
          eksctl create cluster -f awscluster.yml
   
   YAML file of our cluster
   
   # DRUPAL with MY-SQL
   
   Here we are launching drupal with mysql database.
   we have to create a YAML file for our mysql database.
   
   Then launching our drupal.
   
   

**Kubernetes Cluster Setup with eksctl**

This guide explains how to create an Amazon EKS cluster using eksctl and verify the cluster nodes using kubectl.

🚀 Prerequisites

Ensure you have the following installed:

AWS CLI (configured with proper credentials)

kubectl

eksctl

An eks.yaml configuration file for your cluster

📦 Create the Cluster

Use the following command to create your EKS cluster based on the configuration defined in eks.yaml:

eksctl create cluster --config-file=eks.yaml


This command may take several minutes as it provisions the cluster, node groups, networking, and other AWS resources.

🖥️ Verifying Cluster Nodes

Once the cluster is created and your kubeconfig is updated, verify that the nodes are successfully registered:

kubectl get nodes


You should see a list of nodes in the Ready state.
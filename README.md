🚀 Kubernetes NGINX Deployment Project
📌 Project Overview

This project demonstrates the basic usage of Kubernetes by deploying an NGINX web server using Kubernetes Deployment and Service resources.

The goal of this project is to understand:

How applications are deployed in Kubernetes

How Pods are managed using Deployments

How Services expose Pods inside/outside the cluster

Core Kubernetes concepts like ports, selectors, and labels

This project is intended for DevOps beginners and students who are starting their Kubernetes journey.

🛠️ Technologies Used

Kubernetes

Docker

NGINX

kubectl

Minikube (for local Kubernetes cluster)

📂 Project Structure
kubernetes-nginx-demo/
├── nginx-depl.yaml        # Kubernetes Deployment for NGINX
├── nginx-service.yaml     # Kubernetes Service to expose NGINX
└── README.md              # Project documentation

⚙️ Prerequisites / Requirements

Make sure you have the following installed on your system:

Docker

kubectl

Minikube

A system with at least 4GB RAM

Check installations
docker --version
kubectl version --client
minikube version

🚀 Cluster Setup (Local Kubernetes using Minikube)
1️⃣ Start Minikube cluster
minikube start


Verify cluster status:

kubectl get nodes

📦 Deploying the Application
2️⃣ Apply the NGINX Deployment
kubectl apply -f nginx-depl.yaml


Check Deployment and Pods:

kubectl get deployments
kubectl get pods

3️⃣ Apply the NGINX Service
kubectl apply -f nginx-service.yaml


Verify Service:

kubectl get services

🌐 Accessing the Application

If you are using NodePort Service:

minikube service nginx-service


This command will automatically open the NGINX application in your browser.

OR manually get the URL:

minikube ip
kubectl get svc nginx-service


Then access:

http://<MINIKUBE_IP>:<NODE_PORT>

🔍 Useful Debugging Commands

Check logs of a pod:

kubectl logs <pod-name>


Describe pod or service:

kubectl describe pod <pod-name>
kubectl describe svc nginx-service


Delete all resources:

kubectl delete -f nginx-depl.yaml
kubectl delete -f nginx-service.yaml

📘 Key Kubernetes Concepts Learned

Kubernetes Deployment

Kubernetes Service

Pods and ReplicaSets

port vs targetPort

Labels and Selectors

Exposing applications in Kubernetes

Basic troubleshooting using kubectl

🎯 Future Improvements

Add ConfigMaps

Add Ingress Controller

Deploy backend + database (MongoDB / MySQL)

Add CI/CD pipeline

Deploy on cloud Kubernetes (EKS / GKE / AKS)

👨‍💻 Author

Shreyansh Saxena
DevOps & Cloud Enthusiast | Computer Science Engineering Student

⭐ Final Note

This project is a foundation-level Kubernetes project created for learning purposes.
It reflects hands-on practice with Kubernetes and serves as a starting point for more advanced DevOps projects.

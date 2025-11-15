#Docker Voting Application — Kubernetes Deployment

This project demonstrates how to deploy a complete microservices-based voting application on a Kubernetes cluster.
It includes the following microservices:

* Vote app (Frontend – Python Flask)
* Result app (Backend – Python Flask)
* Worker (Processes votes)
* Redis (In-memory queue)
* PostgreSQL (Database)

===========================================================================================================
""" Architecture Diagram: 

[Voting UI]  ---> Redis Queue ---> [Worker] ---> PostgreSQL ---> [Results UI] """


Folder Structure:

k8s-manifests/
├── namespace.yaml
├── vote-deployment.yaml
├── result-deployment.yaml
├── worker-deployment.yaml
├── postgres-deployment.yaml
├── redis-deployment.yaml

Prerequisites: 

Before running this project, ensure you have:

* Docker installed
* Kubernetes Cluster (Minikube / Kubeadm / Cloud Kubernetes)
* kubectl installed
* GitHub account

==========================================================================================================

Steps : 

Deploy to Kubernetes

Create Namespac --> kubectl apply -f namespace.yaml

Deploy Redis, PostgreSQL, Vote App, Result App, Worker --> kubectl apply -f .

==========================================================================================================

Check Pods & Services :
kubectl get pods -n voting-app
kubectl get svc -n voting-app


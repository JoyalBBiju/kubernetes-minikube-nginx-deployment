# Kubernetes Mini Project – Nginx Deployment using Minikube

## Project Overview

This project demonstrates how to deploy a containerized application on a Kubernetes cluster using **Minikube**.

The application is deployed using a **Kubernetes Deployment** and exposed using a **NodePort Service**.

The goal of this project is to practice essential Kubernetes concepts such as:

* Pods
* Deployments
* Services
* Scaling
* kubectl commands

---

## Tools Used

* Docker
* Kubernetes
* kubectl
* Minikube
* Nginx
* PowerShell (Windows)

---

## Project Architecture

User → NodePort Service → Kubernetes Deployment → Pods (Nginx Containers)

---

## Step 1 – Start Minikube

```
minikube start --driver=docker
```

Check cluster:

```
kubectl get nodes
```

---

## Step 2 – Deploy Application

Apply deployment:

```
kubectl apply -f deployment.yaml
```

Check pods:

```
kubectl get pods
```

---

## Step 3 – Create Service

Apply service:

```
kubectl apply -f service.yaml
```

Check services:

```
kubectl get svc
```

---

## Step 4 – Access Application

```
minikube service devops-service
```

This opens the **Nginx welcome page** in the browser.

---

## Step 5 – Scaling the Application

Increase replicas:

```
kubectl scale deployment devops-app --replicas=4
```

Verify:

```
kubectl get pods
```

---

## Key Kubernetes Commands

```
kubectl get pods
kubectl get deployments
kubectl get svc
kubectl describe pod <pod-name>
kubectl logs <pod-name>
```

---

## Learning Outcome

This project helped me understand:

* Kubernetes cluster setup with Minikube
* Creating Deployments
* Managing Pods
* Exposing applications using Services
* Scaling applications

---

## Screenshots

Pods running:

(screenshot here)

Service created:

(screenshot here)

Nginx running in browser:

(screenshot here)

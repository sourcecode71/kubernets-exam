# Kubernetes Exam Setup

This repository contains Kubernetes YAML configurations for creating resources such as Deployments, Services, and Ingress in the `kernelns` namespace.

## 1. **httpd Deployment (`httpd-deployment.yaml`)**
This file defines a deployment for the `httpd` web server with a single replica. It exposes the web server on port 80 inside the container.

### Command to apply:
```bash
kubectl apply -f httpd-deployment.yaml
```

## 2. **ClusterIP Service (`httpd-service.yaml`)**
This file creates a ClusterIP service to expose the `httpd` deployment internally within the Kubernetes cluster. The service routes traffic to port 80.

### Command to apply:
```bash
kubectl apply -f httpd-service.yaml
```

## 3. **Ingress Configuration (`httpd-ingress.yaml`)**
This file configures an ingress to route HTTP traffic from `httpd.local` to the `httpd-service` on port 80. The ingress uses the NGINX Ingress controller.

### Command to apply:
```bash
kubectl apply -f httpd-ingress.yaml
```

## 4. **Namespace**
All resources are created in the `kernelns` namespace. If it doesn't exist, create it using:

```bash
kubectl apply -f kernelns-namespace.yaml
```

---

This should provide a simple overview of the Kubernetes resources involved in the exam tasks. Let me know if you need any adjustments!

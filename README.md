# Wallarm Technical Evaluation Submission

## 🚀 Project Summary

This repository documents the process of deploying and testing **Wallarm's Web Application and API Protection** solution using the **Kubernetes NGINX Ingress Controller** method. The project includes the deployment of a filtering node, configuration of a backend origin, traffic simulation with GoTestWAF, and results verification.

---

## ✅ Tasks Overview

### 1️⃣ Deploy a Wallarm Filtering Node

* Used Kubernetes NGINX Ingress Controller deployed via Helm charts.
* Configured Wallarm token securely using Kubernetes secrets.
* Encountered LoadBalancer IP issue due to Minikube limitations.
* Resolved by switching to NodePort for local access.

### 2️⃣ Set Up a Backend Origin

* Deployed an HTTPBin backend service in Kubernetes.
* Created an Ingress resource to route traffic.
* Tested successful access via custom hostname using `/etc/hosts` update.

### 3️⃣ Generate Traffic Using GoTestWAF

* Pulled Wallarm's GoTestWAF Docker image.
* Simulated malicious traffic targeting the filtering node.
* Verified detection and logging in Wallarm Console.

### 4️⃣ Documentation

* Documented every step taken with screenshots and configurations.
* Provided issue resolutions and deployment decisions.

---

## ⚙️ Deployment Method

Wallarm Ingress Controller was deployed using **Helm** on **Minikube (Kubernetes v1.30.0)**. Helm charts simplified the process and allowed secure secret management. The Ingress Controller was exposed via **NodePort** due to Minikube’s lack of external LoadBalancer IP assignment.

---

## 📄 Full Documentation

For detailed deployment steps, YAML files, commands used, logs, screenshots, and troubleshooting: 👉 [View the Google Document](https://docs.google.com/document/d/1nxusQws7chyNZ5OBZQXkgtGO4r5zTunCqHuDo1ytVx4/edit?usp=sharing)

---


## 📁 Repository Structure

```
.
├── README.md                # Summary and high-level overview
├── values.yaml              # Helm values configuration file
├── ingress.yaml             # Ingress resource to route traffic
└── Diagram.png   # Visual diagram of the deployment
```

---

## 📬 Contact

**Submitted by:** Mahmoud Hossam
**Email:** Mahmoudhossam1101@gmail.com


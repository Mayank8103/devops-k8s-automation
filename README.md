# DevOps Kubernetes Automation

## Overview
This project demonstrates an end-to-end DevOps CI/CD pipeline using modern
cloud-native tools and best practices.

The application is containerized with Docker, deployed to Google Kubernetes
Engine (GKE), and fully automated using GitHub Actions with **Workload Identity
Federation** (no service account keys).

---

## Architecture

1. Terraform provisions GKE infrastructure on Google Cloud
2. GitHub Actions CI/CD pipeline is triggered on push to `main`
3. GitHub authenticates to GCP using Workload Identity Federation
4. Docker image is built and pushed to Artifact Registry
5. Kubernetes Deployment and Service deploy the application
6. Application is exposed using a LoadBalancer service

---

## CI/CD Pipeline

- **Trigger**: Push to `main` branch
- **Authentication**: GitHub → GCP via Workload Identity Federation (no secrets)
- **Container Registry**: Google Artifact Registry
- **Deployment Target**: Google Kubernetes Engine (GKE)

---

## Application URL

👉 **http://34.69.89.234**

---

## Tech Stack

- Google Cloud Platform (GKE, Artifact Registry, IAM)
- Terraform
- Docker
- Kubernetes
- GitHub Actions

---

## Security

- No service account keys stored in GitHub
- Authentication handled via Workload Identity Federation
- IAM roles follow least-privilege principle

---

## Verification

- Kubernetes Pods are running and healthy
- Service type is `LoadBalancer`
- Application is accessible via public IP
- CI/CD pipeline completes successfully on every push to `main`

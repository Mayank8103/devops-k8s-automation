# DevOps Kubernetes Automation

## Overview
This project demonstrates an end-to-end DevOps CI/CD pipeline using:
- Terraform
- Docker
- GitHub Actions
- Google Kubernetes Engine (GKE)
- Workload Identity Federation

## Architecture
- Terraform provisions GKE infrastructure
- GitHub Actions builds and pushes Docker image to Artifact Registry
- Kubernetes deploys application using Deployment and Service
- Application is exposed via LoadBalancer

## CI/CD
- Trigger: push to `main`
- Auth: GitHub → GCP via Workload Identity Federation (no secrets)
- Image Registry: Artifact Registry

## Application URL
👉 http://34.69.89.234

## Tech Stack
- GCP (GKE, Artifact Registry, IAM)
- Terraform
- Docker
- Kubernetes
- GitHub Actions

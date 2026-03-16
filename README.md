# Project 5: GitOps - ArgoCD + Kubernetes

## Overview
GitOps implementation using ArgoCD to automatically sync Kubernetes deployments from GitHub.

## Stack
- ArgoCD
- Kubernetes (Docker Desktop)
- Helm
- GitHub

## What Was Built
- Installed ArgoCD on local Kubernetes cluster
- Connected GitHub repo as source of truth
- Auto-sync deployment from Git changes
- SelfHeal demo - ArgoCD reverts manual changes
- App of Apps pattern
- Helm chart deployed via ArgoCD

## Project Structure
```
05-gitops-argocd/
├── k8s/
│   ├── deployment.yaml    # nginx app - 3 replicas
│   └── service.yaml       # ClusterIP service
├── helm-app/
│   ├── Chart.yaml
│   ├── values.yaml
│   └── templates/
│       └── deployment.yaml
└── apps/
    ├── myapp.yaml         # ArgoCD Application
    └── helm-app.yaml      # ArgoCD Helm Application
```

## Key Concepts
- **GitOps**: Git is the single source of truth
- **Auto Sync**: ArgoCD detects Git changes and applies automatically
- **SelfHeal**: Manual cluster changes are reverted to match Git
- **App of Apps**: ArgoCD apps defined as YAML in Git
EOF

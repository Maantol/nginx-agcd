# NGINX GitOps Demo with ArgoCD

This repository contains my first GitOps hands-on project, where I experimented with deploying a simple NGINX application using ArgoCD on a local Minikube Kubernetes cluster.

## Project Overview

The goal of this project was to gain a practical understanding of GitOps workflows by managing Kubernetes manifests (Deployment, ConfigMap, and Service) entirely through Git and observing how ArgoCD automatically applies changes from the repository.

### Components

- **Deployment**: Runs a basic NGINX web server.
- **ConfigMap**: Provides a custom `nginx.conf` configuration file.
- **Service**: Exposes the NGINX pod internally within the cluster.

### Tools Used

- [Minikube](https://minikube.sigs.k8s.io/docs/) – Local Kubernetes cluster for testing.
- [ArgoCD](https://argo-cd.readthedocs.io/en/stable/) – GitOps continuous delivery tool.
- [kubectl](https://kubernetes.io/docs/reference/kubectl/) – Kubernetes CLI for manual testing and debugging.

## GitOps Workflow

I configured ArgoCD to **pull** the application manifests from this Git repository and apply them to the cluster, following GitOps best practices. All updates were made in Git, and ArgoCD detected and synchronized changes automatically.


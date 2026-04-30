# GCP Infrastructure Provisioning with Terraform
VPC · Subnets · IAM · Workload Identity · GKE · Redis · Artifact Registry

This repository contains the full Terraform configuration I built as part of my self‑learning journey to design and provision a complete GCP infrastructure stack for a microservices application.

I have previously done similar work in AWS, and this project helped me explore how GCP approaches cloud identity, networking, and Kubernetes differently.

## What This Project Provisions

### 1. Networking

Custom VPC

Private and public subnets

Secondary IP ranges for GKE (Pods + Services)

Cloud NAT for outbound traffic

### 2. IAM & Workload Identity
Google Service Accounts (GSAs)

Kubernetes Service Accounts (KSAs)

Workload Identity binding (KSA → GSA)

Least‑privilege IAM roles

Note: GCP’s Workload Identity model is more explicit than AWS IRSA.
It requires a two‑step binding process, which improves clarity and security.

### 3. GKE Cluster
Private GKE cluster

No public endpoint

Workload Identity enabled

Custom node pool

Autoscaling configuration

Release channel configuration

### 4. Artifact Registry
Docker repository for microservice images

### 5. Redis (MemoryStore)
Standard tier Redis instance

Private service access

## How to Use This Repo

//bash

#### Working directory
//mkdir terraform         

#### Move into it
//cd terraform            

#### Clone the Repo
//git clone <repo-url>    

#### Create variable file
//touch terraform.tfvars   

#### Initialize Terraform
//terraform init          

#### Review plan
//terraform plan  

#### Provision resources
//terraform apply          

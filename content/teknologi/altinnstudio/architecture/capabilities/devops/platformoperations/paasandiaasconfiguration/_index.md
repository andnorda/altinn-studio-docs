---
title: Paas & IaaS Configuration & Management
linktitle: PaaS & IaaS Management
description: For a platform like Altinn 3 it is important to have good tools and processes when it comes to configuration and management of infrastructure.
tags: [architecture]
toc: true
---

Over time it is expected that the Altinn 3 platform would consist of hundreds of Kubernetes clusters and other cloud resources.

To be able to manage and configure all theese cloud resorces the architecture choosen have serveral capabilities enabled with help of various tools and processes.

## Tools

For all solutions of Altinn 3 (Altinn Apps, Altinn Platform and Altinn Studio) we use some common tools to configure and manage infrastructure.

We use [Terraform](https://www.terraform.io/) to define the infrastructure as code. Terraform allows to write declarative configuration files
defining the infrastructure we use in the different solutions.

We use the [Terraform Azure Provider](https://registry.terraform.io/providers/hashicorp/azurerm/latest) that allows lifecycle management of
Microsoft Azure using the Azure Resource Manager APIs. This is a provider maintained by the Azure team at Microsoft and the Terraform team at HashiCorp.

We use [Azure Devops Repos](https://azure.microsoft.com/services/devops/repos/) to store our Terraform scripts for the different solutions. 
We use [Azure Devops Pipelines](https://azure.microsoft.com/services/devops/pipelines/) to run the Terraform scripts. 

### Provision of new environemnts







#### Altinn Apps

Each org have their own Altinn Apps environment both for test and production. When a org sign up for using Altinn 3 the DevOps team
will provision a Altinn Apps environment for that organization.



- K8 Cluster with 3 nodes
- Storage account with blob storage for org
- Container register
- KeyVault

#### Altinn Platform





### Patching environments

Kured






## PaaS & IaaS Management Capabilities

### Automation & Scheduling (batch, scripts)

This include running scripts for infrastructure and jobs both manual and scheduled.

See [operations application components](../../../components/application/nonsolutionspecific/operations/) for details about tools and applications used. 

### Paas & IaaS Configuration & Management

This include the capability to configure all PaaS and IaaS in the cloud. 


See [operations application components](../../../components/application/nonsolutionspecific/operations/) for details about tools and applications used. 

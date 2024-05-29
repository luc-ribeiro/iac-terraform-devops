<h1 align="center">
Infra As Code - Terraform - DevOps
</h1>

<div align="right">
    Clique <a href="https://github.com/luc-ribeiro/iac-terraform-devops/blob/main/README-PTBR.md">aqui</a> para ver a versão em Português.
</div>

<div align="center">

![Terraform](https://github.com/luc-ribeiro/iac-terraform-devops/assets/69688077/c302f806-9189-4dc8-8a45-90cf307f33c6)
</div>

## 📄 Project
Infrastructure as Code (IAC) project, creating basic resources and advancing to more complex structures. Datasources, modules, and outputs were covered to facilitate maintenance. 
Cluster state management was also applied, and multiple providers were configured to create additional resources.

The purpose is to use Cloud Providers' consoles only for reading and to pass through IAC for any resource changes, keeping what is in code as the single source of truth.
And to automate infrastructure across any Cloud Provider.

## 💻 Technologies

- **Terraform**
- **AWS**
- **Google Cloud Platform**
- **Azure**

## :pencil: Terraform Concepts

- Providers
- Modules
- Outputs
- Datasources
- Variables
- _tf.state_
- Workspaces
- Versioning
- Remote Backend

## 🚀 Running the project

- Clone the project and access the directory

```bash
$ git clone https://github.com/luc-ribeiro/iac-terraform-devops.git
$ cd 
```

- **[Install Terraform CLI](https://www.notion.so/Instalando-Terraform-CLI-7dc114561ba249db8bbb92aaf23b3f12?pvs=21)**

- Choose the Cloud Provider and install its respective CLI:
  - **[AWS CLI](https://www.notion.so/Instalando-AWS-CLI-fdfc165c64e04a67b5f305771998eb68?pvs=21)**
  - **[GCloud CLI](https://www.notion.so/Instalando-gcloud-CLI-08d9667d9a5a48ed9f39c237dee6c6fd?pvs=21)**
  - **[Azure CLI](https://www.notion.so/Instalando-Azure-CLI-6511a967e1b741279172b7d1f717e446?pvs=21)**
  
- Log in to your Cloud Provider via CLI:
```bash
# GCP
$ gcloud auth application-default login

# Azure
$ az login
```

- To use AWS:
  - You need to configure an SSO token in the console (Identity and Access Management);
  - Create a user and set its permissions;
  - Execute the command below and log in via the browser:

```bash
# AWS
$ aws configure sso
```

- Running Terraform, in the directory of the chosen Cloud Provider:

```bash
# Initialize Terraform
$ terraform init

# Validate if the HCL syntax is correct
$ terraform validate

# Validate what will be created and what the final outcome will be
$ terraform plan

# Create or alter resource in the infrastructure
$ terraform apply
```

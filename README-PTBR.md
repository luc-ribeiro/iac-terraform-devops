<h1 align="center">
Infra As Code - Terraform - DevOps
</h1>

<div align="right">
  Click <a href="https://github.com/luc-ribeiro/iac-terraform-devops/blob/main/README.md">here</a> to view the english version.
</div>

<div align="center">

![Terraform](https://github.com/luc-ribeiro/iac-terraform-devops/assets/69688077/c302f806-9189-4dc8-8a45-90cf307f33c6)
</div>

## 📄 Projeto
Projeto de Infra As Code (IAC), criando recursos básicos e avançando para estruturas mais complexas. Foram abordados datasources, módulos e outputs para facilitar a manutenção. 
Também foi aplicado o gerenciamento de estado do cluster e configurado múltiplos provedores para criar recursos adicionais.

O propósito é utilizar o console dos Cloud Providers somente para leitura, e obrigatoriamente passar pelo IAC para qualquer alteração dos recursos, mantendo como a fonte única da verdade o que está em código.
E automatizar a infraestrutura em qualquer Cloud Provider.

## 💻 Tecnologias

- **Terraform**
- **AWS**
- **Google Cloud Platform**
- **Azure**

## :pencil: Conceitos do Terraform

- Providers
- Modules
- Outputs
- Datasources
- Variables
- _tf.state_
- Workspaces
- Versionamento
- Backend remoto

## 🚀 Executando o projeto

- Clone o projeto e acesse o diretório

```bash
$ git clone https://github.com/luc-ribeiro/iac-terraform-devops.git
$ cd 
```

- **[Instale o Terraform CLI](https://www.notion.so/Instalando-Terraform-CLI-7dc114561ba249db8bbb92aaf23b3f12?pvs=21)**

- Escolha o Cloud Provider e instale sua respectiva CLI:
  - **[AWS CLI](https://www.notion.so/Instalando-AWS-CLI-fdfc165c64e04a67b5f305771998eb68?pvs=21)**
  - **[GCloud CLI](https://www.notion.so/Instalando-gcloud-CLI-08d9667d9a5a48ed9f39c237dee6c6fd?pvs=21)**
  - **[Azure CLI](https://www.notion.so/Instalando-Azure-CLI-6511a967e1b741279172b7d1f717e446?pvs=21)**
  
- Faça o login em seu Cloud Provider pela CLI:
```bash
# GCP
$ gcloud auth application-default login

# Azure
$ az login
```

- Para utilizar a AWS:
  - É necessário configurar um token SSO no console (Identity and Access Management);
  - Criar um usuário e definir suas permissões;
  - Executar o comando abaixo e realizar o login pelo navegador:

```bash
# AWS
$ aws configure sso
```

- Executando o Terraform, no diretório do Cloud Provider escolhido:

```bash
# Inicie o Terraform
$ terraform init

# Validar se a sintaxe HCL está correta
$ terraform validate

# Validar o que será criado e qual vai será o resultado final
$ terraform plan

# Criar ou alterar recurso na infraestrutura
$ terraform apply
```

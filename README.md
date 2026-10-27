# TF-Test

A sandbox repository for experimenting with and testing [Terraform](https://developer.hashicorp.com/terraform) configurations.

## Overview

This repo is a place to try out Terraform modules, providers, and workflows before using them in real projects. Nothing here is intended for production use.

## Prerequisites

- [Terraform](https://developer.hashicorp.com/terraform/install) 1.5 or later
- Credentials for whichever cloud provider the configuration targets (for example AWS, Azure, or GCP)
- Git

## Getting Started

Clone the repository and initialise the working directory:

```bash
git clone <repository-url>
cd TF-Test
terraform init
```

Review the planned changes:

```bash
terraform plan
```

Apply the configuration:

```bash
terraform apply
```

Tear everything down when you are finished:

```bash
terraform destroy
```

## Project Structure

```
TF-Test/
├── main.tf          # Primary resources
├── variables.tf     # Input variables
├── outputs.tf       # Output values
├── providers.tf     # Provider configuration
└── README.md
```

Add files as the project grows and keep this section up to date.

## Conventions

- Run `terraform fmt` before committing to keep formatting consistent.
- Run `terraform validate` to catch configuration errors early.
- Never commit state files (`*.tfstate`), `.terraform/` directories, or files containing secrets such as `*.tfvars` with credentials.

## Suggested `.gitignore`

```
.terraform/
*.tfstate
*.tfstate.*
crash.log
*.tfvars
.terraform.lock.hcl
```

## License

Add a license here if this repository is going to be shared.

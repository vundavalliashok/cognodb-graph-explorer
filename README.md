# Terraform and Ansible AWS Platform

This repository is a scaffold for provisioning AWS infrastructure with Terraform and configuring instances with Ansible.

## Repository Layout

```text
.
|-- .github/
|   `-- workflows/       # Planned CI/CD workflows
|-- .gitignore
|-- ansible/
|   |-- inventory/       # Planned host inventory
|   |-- playbooks/       # Planned configuration and deployment playbooks
|   `-- roles/
|       |-- common/      # Planned base host configuration
|       |-- docker/      # Planned Docker installation and configuration
|       `-- nginx/       # Planned Nginx installation and configuration
|-- application/         # Application files
|-- scripts/             # Helper scripts
|-- terraform/
|   `-- modules/
|       |-- ec2/         # Planned compute resources
|       |-- security/    # Planned security groups and related controls
|       `-- vpc/         # Planned network resources
`-- README.md
```

## Current Status

The directories above define the intended organization, but the repository does not yet contain Terraform configurations, Ansible playbooks or inventories, application files, or helper scripts. As a result, there are no deployment commands that can currently be run from this repository.

## Intended Workflow

Once implementation is added, the expected flow is:

1. Configure AWS credentials and Terraform input values.
2. Use Terraform to create the network, security, and compute resources.
3. Populate the Ansible inventory with the provisioned hosts.
4. Run the Ansible playbooks to configure the hosts and deploy the application.

The exact commands, required variables, supported AWS region, and application deployment steps should be documented here when those configurations are added.

## Planned Prerequisites

- An AWS account and credentials with permissions for the resources being managed.
- Terraform.
- Ansible and SSH access to any hosts configured by Ansible.

Required versions and permissions depend on the Terraform and Ansible implementation and have not yet been defined.

Deployment Flow
===============
GitHub
   |
   v
Terraform
   |
   v
AWS Infrastructure
   |
   v
EC2
   |
   v
Ansible
   |
   +-- Linux Configuration
   +-- Docker Installation
   +-- Nginx Installation
   +-- Application Deployment
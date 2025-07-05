# 🚀 Azure Virtual Machine Deployment Using Terraform

Welcome to my **Azure VM Terraform project**! This repository demonstrates a modular, secure, and scalable infrastructure deployment using **Terraform** on **Microsoft Azure**. It provisions a Virtual Network with subnets and a Linux Virtual Machine, leveraging **Azure Key Vault** for secure secret management.

---

## 🔥 Project Highlights

- **Modular Terraform codebase** for reusable and clean infrastructure management
- **Remote backend** configured with Azure Storage Account for safe Terraform state management
- **Secure credentials** fetched dynamically from Azure Key Vault, eliminating hardcoded secrets
- Deploys core Azure resources: Virtual Network (VNet), Subnets, Public IP, NIC, and Linux VM
- Supports customizable VM specifications and OS images
- Proper dependency management ensures resources are provisioned in order

---

## 🏗️ Architecture Overview

### 1. Networking Module
- Creates a Virtual Network (`VNet`) with multiple subnets
- Subnets and address spaces are parameterized for flexible environment setup

### 2. Virtual Machine Module
- Provisions an Azure Linux Virtual Machine with:
  - Public IP & Network Interface Card (NIC)
  - VM size, OS image, disk caching, and storage options
  - VM credentials securely retrieved from Azure Key Vault
- Depends on subnet creation for network integration

### 3. State Management
- Terraform remote state backend configured with Azure Storage Account, container, and blob to enable collaborative state locking and versioning

---

## ⚙️ How to Use This Project

### Prerequisites
- Terraform v1.3+ installed on your local machine
- Azure CLI installed and authenticated (`az login`)
- Existing Azure Storage Account for backend state storage
- Azure Key Vault created with VM username and password secrets stored

### Steps

1. **Clone the repository:**

   ```bash
   git clone https://github.com/Gauravsharma-alt/VM.git
   cd VM/terraform_module


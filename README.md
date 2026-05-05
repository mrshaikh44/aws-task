# AWS EC2 Terraform Deployment

This project contains Terraform configuration to provision a simple AWS EC2 instance. It automatically fetches the latest Amazon Linux 2023 AMI and deploys a `t2.micro` instance tagged with the name `ajmal`.

## Prerequisites

- [Terraform](https://developer.hashicorp.com/terraform/downloads) installed (v1.0+)
- AWS CLI installed and configured with your credentials (`aws configure`)

## Files Included

- `main.tf`: The main Terraform configuration file that defines the AWS provider, fetches the AMI, and provisions the EC2 resource.
- `.gitignore`: Ensures that sensitive and unnecessary local Terraform state/cache files are not tracked by version control.

## Usage Steps

1. **Initialize Terraform**
   Downloads the required provider plugins.
   ```bash
   terraform init
   ```

2. **Plan the Deployment**
   Review what resources Terraform will create.
   ```bash
   terraform plan
   ```

3. **Apply the Configuration**
   Deploy the resources to your AWS account. You will be prompted to type `yes` to confirm.
   ```bash
   terraform apply
   ```

4. **Clean Up Resources (Optional)**
   If you want to tear down the infrastructure to avoid incurring charges, run:
   ```bash
   terraform destroy
   ```

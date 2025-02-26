# CloudFoxable---First-Flag
CloudFoxable - First Flag Write-Up and Explanation 
.
.
.
# Overview
CloudFoxable is a cloud security CTF challenge designed to simulate real-world AWS security scenarios. The goal of this challenge was to deploy the CloudFoxable environment using Terraform and retrieve the first flag by analyzing the Terraform output.

# Setup Process

# 1. AWS Environment Configuration
- Configured an AWS account (ensuring it was a playground account with no production resources).
- Created an "IAM user with administrative access" and configured the AWS CLI.
- Verified the AWS CLI configuration using:
  ```bash
  aws sts get-caller-identity
  ```

# 2. Terraform Deployment
- Installed and configured Terraform on the local machine.
- Cloned the CloudFoxable repository:
  ```bash
  git clone https://github.com/BishopFox/cloudfoxable
  cd cloudfoxable/aws
  ```
- Copied the Terraform variables file and updated it with the AWS profile:
  ```bash
  cp terraform.tfvars.example terraform.tfvars
  ```
- Initialized Terraform and applied the infrastructure:
  ```bash
  terraform init
  terraform apply
  ```

# Challenges Faced & Resolutions
During the deployment, we encountered some "minor configuration issues", but they were quickly resolved. After making the necessary adjustments, the Terraform execution completed successfully, provisioning the required AWS resources.

# Retrieving the First Flag
- Once the Terraform deployment was complete, we closely examined the output.
- The "flag format" followed the standard `FLAG{challengeName::CamelCaseText}` syntax.
- By carefully reviewing the "Terraform output logs", we successfully identified and retrieved the first flag.
- Additionally, Terraform outputs can be viewed at any time using:
  ```bash
  terraform output
  ```

# Conclusion
The "CloudFoxable First Flag challenge" provided an excellent hands-on experience in "deploying AWS infrastructure using Terraform" and understanding "security configurations in AWS environments". This was a great introduction to cloud security challenges, and we’re excited to move on to the next stage. 🚀


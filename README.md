# Terraform AWS Lambda - Python
This project demonstrates how to package and deploy a Python AWS Lambda function with pip dependencies using a Lambda layer.

# Project Structure
TBD

# **Setup and Installation**
## **Prerequisites**
Before you begin, ensure you have the following tools installed:
- Python 3.12
- **pip** (Python package installer)
- AWS CLI installed and configured
- Terraform installed ([Install Terraform]())
- An AWS IAM user with permissions to manage AWS Lambda, DynamoDB, and related resources

Ensure the AWS CLI is properly configured:
   ```shell
   aws configure
   ```

## **Installation Steps**
1. **Clone the repository**
    ```shell
    git clone https://github.com/tuonglevan/terraform-aws-lambda-python.git
    cd terraform-aws-lambda-python
    ```
2. **Set Up a Python Virtual Environment** It's recommended to use a virtual environment to manage dependencies:
   ```shell
   python3 -m venv venv
   source venv/bin/activate  # On macOS/Linux
   venv\Scripts\activate     # On Windows
   ```
3. **Install Dependencies** Install the required Python libraries:
   ```shell
   pip install -r requirements.txt
   ```
4. Check installed packages:
   ```shell
   pip freeze
   ```
5. **Verify Tools Installation** Make sure the following commands work correctly:
   ```shell
   python --version
   aws --version
   terraform --version
   ```
   
# **Deployment**
## **Using Terraform**
Terraform is used to create AWS infrastructure such as Lambda functions, DynamoDB tables, IAM roles, and more.
1. Initialize Terraform to download plugins and prepare the directory:
   ```shell
   cd terraform
   terraform init
   ```
2. Preview the infrastructure changes Terraform will make:
   ```shell
   terraform plan
   ```
3. Apply the changes to create the resources:
   ```shell
   terraform apply
   ```
   Confirm when prompted by typing `yes`.
4. To destroy the resources (cleanup after experiments):
   ```shell
   terraform destroy
   ```

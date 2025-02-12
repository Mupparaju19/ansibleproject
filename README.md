
# 🚀 **Ansible EC2 Provisioning and Configuration Management**

This project showcases the power of **Ansible** to automate the provisioning and configuration of an **EC2 instance** in **AWS**. With Ansible automation, the EC2 instance is quickly set up with **Ubuntu** and configured to run the **Apache web server**. Perfect for anyone looking to streamline cloud infrastructure provisioning!

## 🔧 **Prerequisites**

Before diving in, make sure you have the following set up:

- **Ansible** installed on your macOS machine
- **AWS CLI** configured with your AWS credentials
- A **valid SSH private key** to access your EC2 instance
- **Python** and **Boto3** libraries installed to interact with AWS via Ansible

## ⚙️ **Setup and Installation**

Follow these simple steps to get started:

### 1. **Install Necessary Dependencies**

Run the following commands to install **Ansible**, **AWS CLI**, and the **Boto3** library:

```bash
brew install ansible
brew install awscli
pip install boto3 botocore
```

### 2. **Configure AWS CLI**

Set up your AWS credentials by running:

```bash
aws configure
```

This step ensures that your AWS CLI can interact with your AWS account. Enter your **Access Key ID**, **Secret Access Key**, **Region**, and **Output Format** when prompted.

### 3. **Edit Inventory File**

Update the `inventory.ini` file with your **EC2 instance details**, such as the instance's public IP and your SSH private key.

### 4. **Provision EC2 and Install Apache**

Run the **Ansible playbook** to provision the EC2 instance and install **Apache**:

```bash
ansible-playbook -i inventory.ini create_ec2_instance.yml
```

This will automatically launch an EC2 instance, configure it, and ensure Apache is up and running.

### 5. **Verify Apache Installation**

Open your web browser and visit the **public IP** of your EC2 instance. You should see the **Apache default page**—proof that your playbook worked!

## 🔨 **Usage**

This playbook automates several essential tasks:

- **Provisioning an EC2 instance** in AWS using Ansible
- **Installing Apache** on the EC2 instance
- **Starting Apache service** to ensure it's up and running

## 🌟 **Contributing**

We encourage contributions to this project! If you have ideas for improvements, new features, or fixes, feel free to **fork this repository**, create an **issue**, or submit a **pull request**.

## 📄 **License**

This project is licensed under the **MIT License**, making it free for you to use and modify.


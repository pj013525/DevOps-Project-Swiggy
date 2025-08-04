# 🍔 Swiggy Application - CI/CD Automation Project

This project demonstrates the complete CI/CD automation pipeline for deploying a Swiggy-like application using modern DevOps tools and practices on **AWS**.

---

## 🚀 Tools Used
| Tool | Purpose |
|------|---------|
| **Terraform** | Infrastructure as Code (IaC) |
| **GitHub** | Source Code Management |
| **Jenkins** | Continuous Integration and Deployment |
| **SonarQube** | Code Quality and Static Analysis |
| **OWASP Dependency-Check** | Vulnerability Scanning for Dependencies |
| **Trivy** | File System and Docker Image Scanning |
| **Docker & DockerHub** | Containerization and Image Management |

---

## 🛠️ Deployment Steps

### ✅ Step 1: Create Terraform Files for AWS Resources
Create `.tf` files to provision VPC, Subnets, Internet Gateway, EC2, and Security Groups.

![Terraform Files](https://github.com/user-attachments/assets/b126a924-1987-4bad-9e92-6aeec63a77be)

---

### ✅ Step 2: Deploy AWS Infrastructure
Use `terraform init`, `terraform plan`, and `terraform apply` to provision the infrastructure.

![Terraform Apply](https://github.com/user-attachments/assets/2e1c79e7-f0d5-4f3a-9463-46c7a033a11f)

---

### ✅ Step 3: Access EC2 Instance
Login to the provisioned EC2 instance using **Mobaxterm** or any SSH client.

![Login EC2](https://github.com/user-attachments/assets/a1008ed1-93ee-44b9-a004-c8ae61544fbb)

---

### ✅ Step 4: Install Required Software
Install the following on the EC2 instance:
- Java 17
- Jenkins
- Docker
- Trivy
- SonarQube

![Install Software](https://github.com/user-attachments/assets/55c6ecfc-417d-40be-92d5-95a58a50350f)

---

### ✅ Step 5: Access Jenkins and SonarQube Dashboards
- Jenkins → `http://<public-ip>:8080`
- SonarQube → `http://<public-ip>:9000`

![Jenkins](https://github.com/user-attachments/assets/504e0175-8d37-4002-96f4-0aba6593aa0b)  
![SonarQube](https://github.com/user-attachments/assets/c1908dff-766c-417a-a75f-5ec84e4f1724)

---

### ✅ Step 6: Install Jenkins Plugins
Go to `Manage Jenkins → Plugins → Available Plugins` and install required ones.

![Plugins](https://github.com/user-attachments/assets/87746dec-289e-47a2-907d-d86f66633731)  
![More Plugins](https://github.com/user-attachments/assets/109e8a28-0a34-4f45-bac4-9ef180d47b1b)

---

### ✅ Step 7: Configure Tools in Jenkins
Configure all tools in `Manage Jenkins → Global Tool Configuration`.

![Tool Config](https://github.com/user-attachments/assets/a4505b7e-03d5-42c0-919a-af0e35f2acb4)

---

### ✅ Step 8: Generate SonarQube Token and Webhook
Generate a token from SonarQube → `My Account → Security` and setup webhook.

![Sonar Token](https://github.com/user-attachments/assets/2d89acdc-3e4c-4258-bda3-ccb359fac95f)  
![Webhook](https://github.com/user-attachments/assets/78f08f87-ac60-437b-84b8-8986ba516b18)

---

### ✅ Step 9: Add Credentials in Jenkins
Configure credentials for:
- SonarQube token
- DockerHub username/password

![Credentials 1](https://github.com/user-attachments/assets/4c8d326f-a0f9-46f0-8fc6-f7868eef258a)  
![Credentials 2](https://github.com/user-attachments/assets/c2452fab-c6d5-4ab0-a09b-2703f41f8ea3)

---

### ✅ Step 10: Configure SonarQube Server in Jenkins
Link the SonarQube server to Jenkins via `Manage Jenkins → Configure System`.

![Sonar Server Config](https://github.com/user-attachments/assets/1257f69e-3430-40c9-9d79-00a6db049b6e)

---

### ✅ Step 11: Create a Dockerfile in GitHub Repo
Build a proper Dockerfile to containerize the Swiggy app.

![Dockerfile](https://github.com/user-attachments/assets/18f4acbe-beb9-4524-9b89-494989c3e5a0)

---

### ✅ Step 12: Create Jenkins Pipeline Job
- Go to Jenkins Dashboard → New Item → Pipeline
- Set the name and source control

![Jenkins Job](https://github.com/user-attachments/assets/4f422367-4b76-46df-9677-2fefd9c53786)

---

### ✅ Step 13: Create a Jenkinsfile in GitHub Repo
Write stages for:
- Checkout
- SonarQube Analysis
- Dependency-Check
- Trivy Scan
- Docker Build & Push
- Deployment

📝 _Don't forget to push this Jenkinsfile to the GitHub repo._

---

### ✅ Step 14: Monitor the Pipeline Build
Wait for all stages to complete, especially **Dependency-Check** which takes longer.

![Dependency Check](https://github.com/user-attachments/assets/980fe6bb-922b-4bff-a90e-055996fba67b)

---

### ✅ Step 15: View SonarQube Code Report
Once pipeline is complete, check SonarQube for quality analysis reports.

![SonarQube Project](https://github.com/user-attachments/assets/22f44b8b-2658-439a-9c76-3547a6448bbc)  
![Sonar Dashboard](https://github.com/user-attachments/assets/b767fa89-73c2-441d-9ebd-ffb3c4858e1f)

---

### ✅ Step 16: Verify Application Deployment
Open the app in a browser via `http://<public-ip>:3000`

![Swiggy App](https://github.com/user-attachments/assets/5929fc19-2c55-473a-8add-3056e60f0330)

---

## 🎉 Application Successfully Deployed!

You’ve now successfully deployed a production-ready Swiggy clone with full CI/CD integration, security checks, and quality gates.

---

## 🧠 Author

**Padmarao Jonna**  
GitHub: [@pj013525](https://github.com/pj013525)

---

> ⭐ _Feel free to fork, modify, and improve this repository to suit your own deployment pipelines!_

This is a Swiggy Application Project
========================================
The tools used in this project are:
Terraform (Infrastructure as Code)
Github (SCM)
Jenkins (CI/CD)
SonarQube (Code quality Analysis)
OWASP (Dependency check)
Trivy (Scan the files and Docker Images)
Docker and Dockerhub (For Docker Images and Container Orchestration)

These are the Steps to Deploy the Swiggy Application:

Step 1:- Create Terraform files for AWS resource creation
<img width="1185" height="666" alt="image" src="https://github.com/user-attachments/assets/b126a924-1987-4bad-9e92-6aeec63a77be" />

Step 2:- Create AWS resources using the Terraform apply command
<img width="1366" height="599" alt="image" src="https://github.com/user-attachments/assets/2e1c79e7-f0d5-4f3a-9463-46c7a033a11f" />

Step 3:- Login to the EC2 using Mobaxterm agent
<img width="1132" height="602" alt="image" src="https://github.com/user-attachments/assets/a1008ed1-93ee-44b9-a004-c8ae61544fbb" />

Step 4:- Install Java-17, Jenkins, Docker, trivy, Sonarqube in the Instance
<img width="1138" height="600" alt="image" src="https://github.com/user-attachments/assets/55c6ecfc-417d-40be-92d5-95a58a50350f" />

Step 5:- Now log in to Jenkins using IP:port number 8080 and SonarQube using IP:port number 9000
<img width="1334" height="624" alt="image" src="https://github.com/user-attachments/assets/504e0175-8d37-4002-96f4-0aba6593aa0b" />
<img width="1365" height="678" alt="image" src="https://github.com/user-attachments/assets/c1908dff-766c-417a-a75f-5ec84e4f1724" />

Step 6:- Now install all necessary plugins in the Jenkins ==> Manage Jenkins ==> Plugins ==> Available Plugins
<img width="1363" height="679" alt="image" src="https://github.com/user-attachments/assets/87746dec-289e-47a2-907d-d86f66633731" />
<img width="1099" height="664" alt="image" src="https://github.com/user-attachments/assets/109e8a28-0a34-4f45-bac4-9ef180d47b1b" />

Step 7:- Now Configure all tools in the Jenkins ==> Mnagae Jnekins ==> Tools
Tools are Java, SonarQube Scanner, Node.js, Dependency Check, Docker
<img width="885" height="687" alt="image" src="https://github.com/user-attachments/assets/a4505b7e-03d5-42c0-919a-af0e35f2acb4" />
In the same way, configure the remaining tools also

Step 8:- Now go to SonarQube home page and generate a secret Token and webhook to configure in the Jenkins credentials
<img width="1366" height="665" alt="image" src="https://github.com/user-attachments/assets/2d89acdc-3e4c-4258-bda3-ccb359fac95f" />
<img width="1269" height="680" alt="image" src="https://github.com/user-attachments/assets/78f08f87-ac60-437b-84b8-8986ba516b18" />

Step 9:- Configure the Credentials of SonarQube and DockerHub in Jenkins
<img width="1115" height="680" alt="image" src="https://github.com/user-attachments/assets/4c8d326f-a0f9-46f0-8fc6-f7868eef258a" />
<img width="1198" height="681" alt="image" src="https://github.com/user-attachments/assets/c2452fab-c6d5-4ab0-a09b-2703f41f8ea3" />

Step 10:- Configure SonarQube server in Jenkins
<img width="946" height="673" alt="image" src="https://github.com/user-attachments/assets/1257f69e-3430-40c9-9d79-00a6db049b6e" />

Step 11:- Now, go to the project Repository on GitHub and create a Dockerfile with all the required commands in it
<img width="1334" height="615" alt="image" src="https://github.com/user-attachments/assets/18f4acbe-beb9-4524-9b89-494989c3e5a0" />

Step 12:- Go to Jenkins Dashboard and click on New job and give any name, and select Pipeline 
<img width="1198" height="670" alt="image" src="https://github.com/user-attachments/assets/4f422367-4b76-46df-9677-2fefd9c53786" />

Step 13:- Now, go to the  project repository on GitHub and create a Jenkinsfile and write the Pipeline stages in it to deploy the application with all the tools integrated in it

Step 14:- The Dependency check stage will take more time to complete, so wait for it to complete
<img width="1365" height="680" alt="image" src="https://github.com/user-attachments/assets/16e7fb9e-55f6-4dbc-8a87-5d3e79d89eb3" />


























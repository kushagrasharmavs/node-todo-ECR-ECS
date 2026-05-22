# Node.js Todo Application (Docker(ECR) + AWS ECS)

This is a **Node.js Todo Application** deployed on **AWS ECS** using **Docker images stored in AWS ECR**.  
The main goal of this project is to understand **containerization and AWS container services**.

## 🚀 Features
- Create Todo
- Read Todo
- Update Todo
- Delete Todo
- REST API using Express.js
- Containerized using Docker
- Deployed on AWS ECS via AWS ECR

## 🛠 Tech Stack
- Node.js
- Express.js
- MongoDB
- Docker
- AWS ECR (Elastic Container Registry)
- AWS ECS (Elastic Container Service)

## 🐳 Docker

### Dockerfile
The application is containerized using Docker.

### Build Docker Image
```
docker build -t node-todo-app .

docker run -p 3000:3000 node-todo-app

```

📦 AWS ECR (Elastic Container Registry)
Steps Performed:

Created an ECR repository

Authenticated Docker with AWS ECR

Tagged Docker image

Pushed image to ECR

```bash
Push Image to ECR
aws ecr get-login-password --region <region> \
| docker login --username AWS --password-stdin <aws_account_id>.dkr.ecr.<region>.amazonaws.com

docker tag node-todo-app:latest <aws_account_id>.dkr.ecr.<region>.amazonaws.com/node-todo-app

docker push <aws_account_id>.dkr.ecr.<region>.amazonaws.com/node-todo-app

```
☁️ AWS ECS (Elastic Container Service)
Deployment Overview:
~ ECS Cluster created
~ Task Definition configured using ECR image
~ ECS Service created to run the container
~ Application exposed via Load Balancer



ECS Configuration:

Launch Type: Fargate

Container Image: AWS ECR

Port Mapping: 3000



📚 Learning Outcome

Understanding Docker containerization

Working with AWS ECR

Deploying containerized applications on AWS ECS (Fargate)

Real-world cloud deployment experience.





<img width="1920" height="1080" alt="Screenshot 2026-01-14 003438" src="https://github.com/user-attachments/assets/c1f4ebb8-caf0-4ebb-80bd-c3c3a1601013" />


<img width="1920" height="1080" alt="Screenshot 2026-01-17 113246" src="https://github.com/user-attachments/assets/39648d1f-8880-45bf-81b8-545ebfe1b027" />
<img width="1920" height="1080" alt="Screenshot 2026-01-17 113316" src="https://github.com/user-attachments/assets/50e39a5a-e8b0-4f55-af29-f50526fb61cd" />
<img width="1920" height="1080" alt="Screenshot 2026-01-17 113357" src="https://github.com/user-attachments/assets/82b35c37-bbcb-400f-9ae1-5148fc675a33" />

<img width="1920" height="1080" alt="Screenshot 2026-01-14 003511" src="https://github.com/user-attachments/assets/aabf1941-b04f-489f-8127-baff6fcc8cfa" />



<img width="1920" height="1080" alt="Screenshot 2026-01-14 003524" src="https://github.com/user-attachments/assets/0d3b8d7a-62d4-46d4-82fc-a6605e1a08d6" />

<img width="1920" height="1080" alt="Screenshot 2026-01-14 003539" src="https://github.com/user-attachments/assets/5ed2e2ce-9393-464e-89a2-e7fe7fcf2bae" />

<img width="1920" height="1080" alt="Screenshot 2026-01-14 003638" src="https://github.com/user-attachments/assets/69057d8a-5a11-4883-9f07-e8fe6fb87794" />



<img width="1920" height="1080" alt="Screenshot 2026-01-14 005121" src="https://github.com/user-attachments/assets/60e247e0-2ba8-45b2-8f1f-2273cb0b7b3a" />

<img width="1920" height="1080" alt="Screenshot 2026-01-14 003702" src="https://github.com/user-attachments/assets/59e17af7-70e2-41cf-a943-3c8c9cecb120" />

<img width="1920" height="1080" alt="Screenshot 2026-01-17 113815" src="https://github.com/user-attachments/assets/c2bb817d-c338-44c7-a1de-143a2642aaff" />
<img width="1920" height="1080" alt="Screenshot 2026-01-17 113941" src="https://github.com/user-attachments/assets/d1232d81-f7f2-46b6-b678-5ad108b63326" />

<img width="1920" height="1080" alt="Screenshot 2026-01-14 004638" src="https://github.com/user-attachments/assets/575bf3b5-9412-411c-83d0-ee6cfce06c76" />













 Credits

This project is inspired by
TrainWithShubham YouTube Channel
👨‍🏫 Shubham Londhe

Original Repository:
👉 https://github.com/LondheShubham153/node-todo-cicd

# React TSX Web Application Deployed on AWS EC2

## 📌 Overview

This project is a React + TypeScript (TSX) web application deployed on an AWS EC2 Ubuntu instance. The application source code is stored on GitHub, cloned onto the EC2 instance, and executed using Node.js and npm.

For development and testing, the application runs on port **8080** using `npm run dev`. Access to the application is restricted through AWS Security Groups, allowing only my public IP address to access the application, providing a secure testing environment.

---

## 🛠️ Tech Stack

- React
- TypeScript (TSX)
- Vite
- Node.js
- npm
- Ubuntu Server
- AWS EC2
- Git & GitHub

---

## ☁️ AWS Services Used

- Amazon EC2
- AWS Security Groups

---

## 🚀 Deployment Workflow

1. Created an Ubuntu EC2 instance.
2. Installed Node.js and npm.
3. Cloned the application from GitHub.
4. Installed project dependencies using:

```bash
npm install
```

5. Started the development server:

```bash
npm run dev
```

6. Configured the AWS Security Group:
   - **SSH (22)** → Source: **My Public IP**
   - **Custom TCP (8080)** → Source: **My Public IP**

7. Accessed the application using:

```
http://<EC2-Public-IP>:8080
```

---

## 🔐 Security Configuration

To secure the development environment, the EC2 Security Group was configured as follows:

| Rule | Port | Source |
|------|------|--------|
| SSH | 22 | My Public IP |
| Custom TCP | 8080 | My Public IP |

This configuration ensures that only my laptop can SSH into the server and access the web application during development.

---

## 📊 Deployment Architecture

<img width="1774" height="887" alt="ChatGPT Image Jul 22, 2026, 10_38_45 PM" src="https://github.com/user-attachments/assets/4e9a4e5e-311f-4556-8793-94208176419b" />


---

## 📚 Key Learnings

- Launching and configuring an Ubuntu EC2 instance
- Installing and managing Node.js applications on Linux
- Cloning and managing projects from GitHub
- Configuring AWS Security Groups
- Deploying a React + TypeScript application on AWS
- Restricting application access using inbound security group rules
- Accessing applications through the EC2 public IP

---

## 🔮 Future Improvements

- Build the application using `npm run build`
- Deploy the production build with Nginx
- Enable HTTPS using Let's Encrypt
- Configure a custom domain with Route 53
- Automate deployment using GitHub Actions

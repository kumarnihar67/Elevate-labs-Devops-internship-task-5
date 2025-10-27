# 🚀 TASK 5: Build a Kubernetes Cluster Locally with Minikube

## 🎯 Objective
Deploy and manage applications in a **local Kubernetes cluster** using Minikube, kubectl, and Docker.

---

## 🛠 Tools Used
- 🖥 **Minikube v1.37.0** – Local Kubernetes cluster  
- 📦 **kubectl v1.34.0** – Kubernetes command-line tool  
- 🐳 **Docker Desktop** – Container runtime  
- 💻 **VS Code** – Editor for YAML files and terminal  
- ⚡ **PowerShell (Admin)** – Terminal for running commands  

---

## 📁 Project Structure

C:\K8sProject
│
├─ deployment.yaml # Kubernetes Deployment for Nginx
├─ service.yaml # Kubernetes Service (NodePort) for Nginx
├─ README.md # This file
└─ screenshots/
├─ pods.png # kubectl get pods
├─ services.png # kubectl get services
├─ nginx.png # Nginx welcome page
├─ scaled.png # Scaled pods
└─ logs.png # Deployment logs/describe
---

## 📝 Steps Completed

✅ Verified that the cluster is running and the control-plane node is ready.
Start Minikube Cluster
minikube start --driver=docker
kubectl get nodes

2️⃣ Create Deployment.yaml:
Created deployment.yaml for Nginx with 2 replicas:
Apply it with VS code :

kubectl apply -f deployment.yaml
kubectl get pods
📸 Screenshot: screenshots/pods.png

<img width="1920" height="1080" alt="task5 1" src="https://github.com/user-attachments/assets/768eac7b-6a3b-4fc6-8f98-ee674c991096" />

3️⃣ Expose Deployment via Service
Created service.yaml to expose Nginx on NodePort:
Apply it:
kubectl apply -f service.yaml
kubectl get services
📸 Screenshot: screenshots/services.png

<img width="1920" height="1080" alt="task5 2" src="https://github.com/user-attachments/assets/4a1036f5-0079-43bf-ae49-126bbfcf2964" />

Open the service in browser:
minikube service nginx-service
🌐 Screenshot: screenshots/nginx.png

<img width="1920" height="1080" alt="task5 4" src="https://github.com/user-attachments/assets/73638361-3418-42ef-aae1-7eb3a56fa697" />


<img width="1920" height="1080" alt="task5 3" src="https://github.com/user-attachments/assets/00293905-15ea-4948-a7b9-374c07683677" />

4️⃣ Scale Deployment
kubectl scale deployment nginx-deployment --replicas=4
kubectl get pods
📸 Screenshot: screenshots/scaled.png


<img width="1920" height="1080" alt="task5 5" src="https://github.com/user-attachments/assets/b894ad11-6ccd-4ba5-ac1a-b59b33c7a046" />



5️⃣ Describe Deployment & Logs
kubectl describe deployment nginx-deployment
📸 Screenshot: screenshots/describe.png

<img width="1920" height="1080" alt="task5 6" src="https://github.com/user-attachments/assets/60d0aad4-4e91-47dc-bcd1-06aa6b1ee213" />


kubectl logs <pod-name>
📸 Screenshot: screenshots/logs.png

<img width="1920" height="1080" alt="task5 7" src="https://github.com/user-attachments/assets/80c30e2c-c671-404f-aebe-edeecbe3dc4f" />



✅ Summary
Set up a local Kubernetes cluster using Minikube on local machine.

Deployed a simple Nginx app using deployment.yaml.

Exposed the app with service.yaml and accessed it in the browser.

Scaled the deployment from 2 → 4 replicas.

Verified cluster resources, logs, and deployment details using kubectl.
📸 Screenshot: minikube-dashboard


<img width="1920" height="1080" alt="task5 8" src="https://github.com/user-attachments/assets/6f8961db-3216-49b0-ac1d-f7d1eff9b700" />


<img width="1920" height="1080" alt="task5 9" src="https://github.com/user-attachments/assets/20c6d163-cf56-4dd9-a5e0-8b987d760ae8" />



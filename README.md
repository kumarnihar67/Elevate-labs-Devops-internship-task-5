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

## 1️⃣ Start Minikube Cluster
```powershell
minikube start --driver=docker
kubectl get nodes
✅ Verified that the cluster is running and the control-plane node is ready.

2️⃣ Create Deployment
Created deployment.yaml for Nginx with 2 replicas:
Apply it with VS code :

kubectl apply -f deployment.yaml
kubectl get pods
📸 Screenshot: screenshots/pods.png

<img width="1920" height="1080" alt="task5 1" src="https://github.com/user-attachments/assets/a2208d67-6f51-49d8-8496-5a46026ab310" />


3️⃣ Expose Deployment via Service
Created service.yaml to expose Nginx on NodePort:
Apply it:
kubectl apply -f service.yaml
kubectl get services
📸 Screenshot: screenshots/services.png

<img width="1920" height="1080" alt="task5 2" src="https://github.com/user-attachments/assets/4cba2457-6412-4476-a81c-a6e909f7a7c0" />


Open the service in browser:
minikube service nginx-service
🌐 Screenshot: screenshots/nginx.png

<img width="1920" height="1080" alt="task5 4" src="https://github.com/user-attachments/assets/4c4f321d-b4c7-442d-8fbe-9debf8acbc30" />


<img width="1920" height="1080" alt="task5 3" src="https://github.com/user-attachments/assets/f20a34d3-58c7-491c-b057-1fd6676d61a4" />


4️⃣ Scale Deployment
kubectl scale deployment nginx-deployment --replicas=4
kubectl get pods
📸 Screenshot: screenshots/scaled.png

<img width="1920" height="1080" alt="task5 5" src="https://github.com/user-attachments/assets/163fcc45-032e-4f0a-9d04-9d437a8aaac5" />


5️⃣ Describe Deployment & Logs
kubectl describe deployment nginx-deployment
📸 Screenshot: screenshots/describe.png

<img width="1920" height="1080" alt="task5 6" src="https://github.com/user-attachments/assets/98ab151d-b913-4979-a317-4804a4bf7db5" />

kubectl logs <pod-name>
📸 Screenshot: screenshots/logs.png

<img width="1920" height="1080" alt="task5 7" src="https://github.com/user-attachments/assets/26f048d3-e57d-49ef-b9c5-cb942094fd72" />


✅ Summary
Set up a local Kubernetes cluster using Minikube on local machine.

Deployed a simple Nginx app using deployment.yaml.

Exposed the app with service.yaml and accessed it in the browser.

Scaled the deployment from 2 → 4 replicas.

Verified cluster resources, logs, and deployment details using kubectl.
📸 Screenshot: minikube-dashboard

<img width="1920" height="1080" alt="task5 8" src="https://github.com/user-attachments/assets/caa6dec2-d734-40fb-a6d7-c1cc1be7357b" />

<img width="1920" height="1080" alt="task5 9" src="https://github.com/user-attachments/assets/4a6b3ef9-cc95-4777-b12e-09d2635baa30" />






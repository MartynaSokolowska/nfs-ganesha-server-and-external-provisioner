# Simple web application using NFS Ganesha server and external provisioner

### Instructions for Running the Application

To run the application follow these steps:

#### 1. Start the Selected Kubernetes Cluster

You can use any of the following tools to set up your Kubernetes cluster:

- **Minikube**
- **Kind (Kubernetes in Docker)**
- **AWS EKS (Elastic Kubernetes Service)**
- **Any other Kubernetes distribution**

#### 2. Install the required tools by running the following commands (Winodws):

```bash
choco install eksctl
choco install kubernetes-cli
choco install kubernetes-helm
```

#### 3. Deploy the Necessary Resources

Execute the following commands to deploy the required resources:

```bash
helm install nfs-deployment <path/to>/nfs-ganesha-server-and-external-provisioner/charts/nfs-server-provisioner --set storageClass.name=nfs-storage
kubectl apply -f <path/to>/nfs-ganesha-server-and-external-provisioner/config_yamls/all_resources.yaml
```

#### 4. View the Result

To view the result, open a web browser and navigate to:

```bash
http://localhost:8080/hello.txt
```

Please note that the startup process may take a few minutes to complete.

### Expected Outcome

After following the instructions and successfully deploying the application, you should see the following result when you open your browser:

![image](https://github.com/user-attachments/assets/5b4ed104-d5ba-47a7-9b71-6cbe41b5683a)



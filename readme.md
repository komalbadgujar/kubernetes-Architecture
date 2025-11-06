# 🧩KUBERNETES ARCHITECTURE 
🌐 What is Kubernetes?

Kubernetes (K8s) is a tool that helps you run, manage, and scale containerized applications easily.

It automatically takes care of:

- Starting and stopping containers

- Placing them on the right servers

- Restarting them if they fail

- And scaling them up or down when needed.

🚀 Key Features:

- Automation: Runs apps automatically.

- Scaling: Adds or removes containers when traffic changes.

- Self-healing: Restarts failed containers automatically.

- Load Balancing: Distributes traffic evenly.

- Portability: Runs on any cloud or on-premises servers.

## Diagram of Kubernetes Architecture

![Alt Text](./kubernetes%20arch%20diagram.png)

## Explanation Of Architecture Diagram  

### ⚙️ Control Plane (Master Node)

The Control Plane is responsible for managing the overall cluster — it makes global decisions about scheduling, monitoring, and maintaining the desired state of applications.

Components:

1) 🧠 API Server

- Acts as the central management point of the Kubernetes cluster.

- Exposes the Kubernetes API that developers interact with (using tools like kubectl).

- All internal components (Controller Manager, Scheduler, Kubelet) communicate through the API Server.

2) 🗂️ etcd

- A key-value store that stores all cluster data, including configuration, state, and secrets.

- Serves as the single source of truth for the cluster’s state.

3) ⚙️ Controller Manager

- Runs background processes known as controllers.

- These controllers ensure that the cluster’s actual state matches the desired state defined in manifests.

- Examples include the Replication Controller, Node Controller, and Endpoint Controller.

4) 📅 Scheduler

- Responsible for assigning newly created pods to available worker nodes.

- It decides the best node based on resource availability, affinity rules, and constraints.

### 🧱 Worker Nodes

The Worker Nodes (also called Minions) are where the actual application workloads (containers) run.

Components:

1) 👷 Kubelet

- An agent that runs on each worker node.

- Communicates with the API Server to receive pod specifications and ensures the containers are running as expected.

- Reports node and pod status back to the Control Plane.

2) 🌐 Kube-proxy

- Manages network communication between pods and external services.

- Handles load balancing, forwarding requests, and maintaining network rules on each node.

3) 🧑‍💻 kubectl

- The command-line tool used by administrators and developers to interact with the Kubernetes cluster.

- It sends commands and configuration files to the API Server, which then processes and executes them across the cluster.

### 🧱 What is a Pod in Kubernetes?

A Pod is the smallest unit in Kubernetes.
It represents one or more containers that work together and share the same network and storage

## 🔄 Pod Lifecycle in Kubernetes

![Pod Lifecycle Diagram](lifecycle%20of%20pod%20img.png)


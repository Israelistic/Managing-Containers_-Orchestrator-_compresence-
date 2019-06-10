
Docker
* Docker pages software into standardized unit called containers that have everything your software needs to run including libraries, code and runtime
* Lets you quickly deploy and scale applications into any environment  


Task Associated with containers:

* Deployment if Containers
* Redundancy and availability of containers
* Scaling up or down containers 
* Load Balancing
* Health Monitoring of containers and hosts
* Service discovery 
* and more …
 

Control plane - main entry point of orchestrator. Interface to launch an application, query the state or shout down 

Why Fargate

Pro’s:

* Its serverless version of container 
* Both ECS and EKS requires managing cluster and or some Infrastracture
* No need to create cluster or determine EC2 size, Fargare scales on-dement
* Pay for what you use

Con’s:

* One size does NOT fit ALL- Can be cheaper or pricier then ECS/EKS based on usage



|Tasks|EC2|ECS|Kubernetes|EKS|Fargate|
|-----|---|---|----------|---|-------|
|Deployment as Containers|you need to configure the container on multiple AZ’s and mange them|-Fully manage, highly available|highly scalable control plane|You have to select the host (such as EC2|pay for underlying EC2|Orchestration|
|Orchestration|   |Container orchestration created by AWS|Managed Kubernetes (open source). by AWS|   |Container on demand|
|3    |   |   |          |   |       |
|4    |   |   |          |   |       |
|5    |   |   |          |   |       |
|6.   |   |   |          |   |       |
|7.   |   |   |          |   |       |
|8.   |   |   |          |   |       |
|9.   |   |   |          |   |       |
|10   |   |   |          |   |       |
|11   |   |   |          |   |       |
|| ||||||


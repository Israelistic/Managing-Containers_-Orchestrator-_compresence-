
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
|Clustering|   |Requires creating cluster|Requires creating cluster|Requires creating cluster|No cluster require|
|Autoscaling /Redundancy - Scaling up or down containers|You have  to configure and  manage Autoscaling Groups|   |You need to take care of scaling|   |       |
|Availability (AZ)|You have to take care of Redundancy and availability|   |          |   |       |
|Health Monitoring of containers and hosts|You have to monitor and manage failed services|   |          |   |       |
|Load balancer|You have to configure and deploy load blancer|   |          |   |       |
|Service discovery|You have to manage service discovery|   |          |   |       |
|Control Plane|   |You do not pay for control plane. You pay for workers nodes|Free- Run on your own Control Plane on Host such as EC2|Cost money-Pay for AWS manage Control plane for you|Only pay for tasks based CPU and memory|
|Flexibility / Portability|AWS only|Deeper integration with other AWS services such as IAM, ALB. Good for cloud native container architechtures|Run on any cloud or on perm.  If you deploy on EC2 you manage it|Good for cloud native container architecture. Easier to move on-prem Kubernetes to AWS EKS|Fargate currently runs on ECS. Good for workload which runs for duration, Fargate is expensive if high CPU/Memory tasks runs all the time|
|Owned by ?|AMAZON - you manage|Owned by AMAZON|Fully open source by google - you manage|AMAZON|AMAZON|



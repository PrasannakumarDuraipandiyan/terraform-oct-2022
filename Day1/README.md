# Day1

## What is Cloud Computing?
- Pay as you to Go pricing
- Flexible infrastucture that can used on demand
- Highly Available (HA)
- Dynamic scaling
- Cheaper than procurring and maintaining own Servers


## Why do we need Cloud Computing?
- to avoid infrastructure maintenance

## What is an Azure Region?
- you can think as a City like Mumbai, Chennai, Hyderabad, Bengaluru

## What is an Azure Availability Zone?
- Within each Azure Region(City), there might be several Availability Zone
- Each Availability Zone represents one Data Center
- Eg: mumbai-west1a
      mumbai-west1b
      mumbai-west1c

## What is Data Centre
- a collection of many servers located in one Availability Zone under a Region
- Sever 1000s or even lakhs of Servers might be there in a single Availability Zone

## What is on-prem servers?
- On premise servers ( aka on-prem )
- Your company owned servers

## Different types of RAM
- UDIMM
- SODIMM
- RDIMM

## Multi socket Motherboards - Server Grade motherboards


## Integrated Chip 
- SCM ( Single Chip Module ) - One IC will have just One Processor ( 1 Processor per Socket )
- MCM ( Multiple Chip Module ) - One IC will have many Processors ( 1 IC may have 8 Processors )

## Multiple Cores
1 Processor - may have many numbers of CPU Cores

1 Processor - may have 256 core

MCM with 8 Processor ( Each Processor having 256 cores )
Per Socket = 8 x 256 Core =

Server Motherboardss that has 8 Sockets
MCM ( 1 IC with 8 Processors )
Each Processor having 256 Cores 

8 x 256 * 8 = 


## What are the deciding factors that control the number of Virtual Machines that can be supported by a Single Server/Desktop/Laptop?
- RAM (Memory )
- HDD/SDD (Storage)
- Number of Cores

Laptop Configuration
8 Cores, 16 GB RAM, 500 GB SSD(Storage)
How many maximum Virtual Machines(Guest OS) and Host OS you can run simultaneously ?
Host OS - 1
Guest OS - 7

Host OS - 1
Guest OS - ( 8 Physical Core x 2 Virtual Core - Each Physical core is seen as 2 Virtual Cores )

General Purpose Processors
1. AMD ( Invented 64 Bit Processors x86_64 Instructions )
 - 32 bit (AMD pays royalty for Intel's x86 Instructions set)
2. Intel (Invented 32 Bit Processors x86 Instructions )
 - 64 bit (Intel pays royalty for AMD's x64 Instruction set)
Virtualization Feature
AMD's virtualization feature
  - AMD-V (CPU Feature set)
Intel's Virtualization feature
  - VT-X (CPU Feature set)

Subnet (IP Block - Address Range)
172.17.0.0/16 (IPV4 IP Address - 32 bit wide(4 bytes))
A.B.C.D/16(Bit are Fixed from Left - 172 and 17 are fixed)
16 - CIDR

172 - 1 byte (8 bit)
17 - 1 byte (8 bit)
0 - 1 byte (8 bit)
0 - 1 byte (8 bit)

172.17.0.0
172.17.0.1
172.17.0.2
...
172.17.0.255
172.17.1.0
172.17.1.1
...
172.17.1.255
...
172.17.255.255

= 255 x 255 = 65536 IP Addresses are there in 172.17.0.0/16

172.17.0.0/24 ( 255 IP Adresses )
172.17.0.0
172.17.0.1
...
172.17.0.255






IPV4(exiting IP format) and IPV6(New type of IP)

IP Address can be Dynamic or Static IP
- Public and Private IP


Virtual Network or Network
- Each Network can be divided into many Subnets

Subnet 
- logical Network


## What is Private Cloud?
- Your on-prem data center

## What is Public Cloud?
- Azure
- AWS
- GCP

## Hybrdid Cloud
- Combination of your Private Cloud and Public Cloud

## OpenStack 
- you can manage virtual machine of different configurations on demand just like we can create VMs in Azure, AWS, GCP, etc.,
- Virtual Machines using the On-Prem Servers

## VMWare vSphare/vCenter (Bare Metal Hypervisor)

## What is Configuration Management Tools?
- Examples
  - Ansible, Puppet, Chef
- Infrastructure as a Code Tool
- Configuration Management Tools helps in automating software installation on a existing VMs, Physical Machine with OS
- For example, we can install a Webserver on a existing OS
- You can users on a existing OS

## What is a Provisioner tool?
- automation tools that can help in automating infrastructure
- can automate creating Virtual Machines(OS), Container, installing OS on a Physical Machine
- Example
   - HashiCorp Vagrant, Docker 
  
## What is an Orchestration Platform?
- container management platform
- manages containerized application/microservices
- Example
  - Google Kubernetes
  - RedHat OpenShift
  - Docker SWARM

## What is Cloudformation?

## What is Terraform?
- Infrastructure as a Code Tool
- primarily it helps in automating infrastructure (VMs, Storage, Load Balancers, etc )


You need a Virtual Machine with an CentOS 8 installed (Provisioner)
 - you could use Vagrant to provision Virtual Machine and automate CentOS 8 installation with SSH access based key pairs
 - Vagrant tools reads all the automation code from a script file called Vagrantfile ( ruby )
 - Developed by HashiCorp 

You wish to install Docker on that CentOS 8 Virtual Machine ( Configuration Management Tool)
- You could write ansible playbook to install Docker Container Engine

You wish to deploy a containerized Microservice ( Provisioner - IaC)
- You could use Docker

You wish to manage the microsevice (Orchestration Platform)
- Kubernetes/OpenShift to manage the containerized microservices

## What is Domanin Specific Language(DSL)?
- the language in which the automation code is written

Kubernetes/OpenShift
- it can be installed on your local Laptop/Desktop/Workstation/Server
- it can be installed in AWS/Azure/GCP on Virtual Machines on the public cloud
- Managed Services (SaaS - Model)
- In Azure
  - Azure Kubernetes Service (AKS) - Managed Kubernetes Cluster (Orchestration Platform)
  - Installation of Kubernetes is taken care by Azure
- In AWS
  - Elatic Kubernetes Service (EKS) - Managed Kubernetes Cluster (Orchestration Platform)
- it provides an environment to run Microservices or Container applications
- it provides an environment for containerized application or microservice and make them High Available
- it is self-healing platform ( it know how to heal itself as well as microservice that are managed by them)
- it has inbuilt 

Infrastructure as a Service (IaaS)
- Only the hardware is rented from Public Cloud (AWS,Azure,GCP,IBM Cloud, VMWare Cloud,Oracle Cloud,etc)
- OS System Licenses are managed by us

Platform as a Service (PaaS)
- We rent Hardware and Operating System from PUblic Cloud Vendors (AWS, Azure, GCP, etc.,)
- We need install software like Oracle DB Server, Oracle Weblogic ourself either manually or in automated fashion

Software as a Service(SaaS)
- AWS EKS or Auzre AKS are examples

Infrastructure as a Code Tool
- helps in automation OS installation, softwares via source code
Examples:
1. Docker
2. Vagrant
3. Kubernetes/OpenShift/Docker SWARM
4. Ansible/Puppet/Chef/Salt(SaltStack)

# Docker

## Installing Docker in Ubuntu
```
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg lsb-release
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
  
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
sudo systemctl enable docker
sudo systemctl start docker
sudo systemctl status docker
sudo usermod -aG docker $USER
newgrp docker
docker --version
docker images
```

## Docker Commands

## Create a mysql db server container
```
docker run -d --name mysql --hostname mysql bitnami/mysql:latest
```

Expected output
<pre>
jegan@tektutor:~/terraform-oct-2022$ <b>docker run -d --name mysql --hostname mysql -e MYSQL_ROOT_PASSWORD=root bitnami/mysql:latest</b>
Unable to find image 'bitnami/mysql:latest' locally
latest: Pulling from bitnami/mysql
1d8866550bdd: Pull complete 
1b8c0f27c1e5: Pull complete 
Digest: sha256:fcb08fe71a17b393852db74371be05de6bb0484aa59b0f24aa6a073174d30f48
Status: Downloaded newer image for bitnami/mysql:latest
7bb941f77d465c1c34f07f22c46e63f6f12dd87dcecb45a52e5fd813739e293f
</pre>

Listing the running containers
<pre>
jegan@tektutor:~/terraform-oct-2022$ <b>docker ps</b>
CONTAINER ID   IMAGE                  COMMAND                  CREATED          STATUS          PORTS      NAMES
7bb941f77d46   bitnami/mysql:latest   "/opt/bitnami/script…"   38 seconds ago   Up 35 seconds   3306/tcp   mysql
</pre>

## Getting inside the mysql db server container
Type 'root' as the password without quotes when prompted.
```
docker exec -it mysql sh
mysql -u root -p
SHOW DATABASES
CREATE DATABASE tektutor;
USE tektutor;
CREATE TABLE training ( id INT NOT NULL, name VARCHAR(100) NOT NULL, duration VARCHAR(200) NOT NULL, PRIMARY KEY(id) );
INSERT INTO training VALUES (1, "DevOps", "5 Days");
INSERT INTO training VALUES (2, "Terraform", "5 Days");
SELECT * FROM training;
exit
exit
```
## Installing Terraform in Ubuntu
```
wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com 

$(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install terraform
```

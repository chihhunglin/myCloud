# myCloud
## How to Install Kubernetes (k8s) on Ubuntu 20.04
### Prerequisites

 - An SSH key pair on your local Linux machine.
 - Three servers running Ubuntu 20.04 with at least 2GB RAM and 2 vCPUs each. You should be able to SSH into each server as the root user with your SSH key pair.
 - Set hostname
> $ sudo hostnamectl set-hostname "k8s-master"  // Run this command on master node  
> $ sudo hostnamectl set-hostname "k8s-node-0"  // Run this command on node-0  
> $ sudo hostnamectl set-hostname "k8s-node-1"  // Run this command on node-1
 - Ansible installed on your local machine.

### Install
> $ ansible-playbook -i hosts prerequisites.yml 

> $ ansible-playbook -i hosts initial.yml 

> $ ansible-playbook -i hosts kube-dependencies.yml 

> $ ansible-playbook -i hosts master.yml -vvvv 

> $ ansible-playbook -i hosts workers.yml -vvvv 

## References
https://www.digitalocean.com/community/tutorials/how-to-create-a-kubernetes-cluster-using-kubeadm-on-ubuntu-18-04
https://www.linuxtechi.com/install-kubernetes-k8s-on-ubuntu-20-04/

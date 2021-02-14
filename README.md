Kubernetes set up on windows 10  
1 master and 2 nodes
 

Softwares used:
 1. Virtual box - For creating virtual machines for master and nodes
 2. Ansible - For installing softwares on virtual machines; master and nodes

Softwares that are installed on virtual machines - Docker , kubernetes, calico for kubernetes networking b/w master and nodes
2 Ansible playbooks, master-playbook and node-playbook, are used for the installation of the softwares.


In the vagrant file, we are using virtual box for creating vms and ansible for software installation on them. This setup is taken from the kubernetes 
getting started guide. But, made some modifications to it, to make it work on windows. 

Listing the issues that I have encountered and the action taken to resolve them.

1. Installation of ansible did not go through.
	- Manually installed python pip, ran vagrant destroy and vagrant up 
	
2. Failed at Calico installation step
	- Updated the yaml url to the latest one
	
3. Failed at the docker installatiion step while node setup
	- Removed the docker notify step from the node playbook
	
	
With 	
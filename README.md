# Install Docker with Ansible.
A quick way to install Docker engine on several Ubuntu hosts using Ansible.  
Hosts IP addresses should be listed in *hosts.txt* file.  
Of cause you need Ansible installed on your *control node* (the machine that runs Ansible and manages other nodes). [More on Ansible.](https://docs.ansible.com/ansible/latest/index.html)  
Also the procedure of generating an SSH key pair should be done(`ssh-keygen -t rsa`) and the public key be copied to the hosts and installed in an authorized_keys file. [More info on SSH](https://docs.ansible.com/ansible/latest/index.html).

## Preparative steps involved in playbook:
- Disable password authentication on each of managed host
- Enable public key authentication
- Install aptitude using apt (optional)

## Main Docker installation steps presented in playbook:
- Install required system packages
- Add Docker GPG apt Key
- Set up the repository
- Add Docker Repository
- Update  apt package index and install docker-ce

> Additionally installation of *docker-ce-cli* *containerd.io* *docker-compose-plugin* can be added.  
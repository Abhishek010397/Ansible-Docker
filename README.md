# Ansible-Docker

setting up docker using configuration-management=ansible

steps
----------------------------------------------------------------------------------------------------------------------------------------Launch two EC2 instances of ubuntu18.04
one master and one slave

----------------------------------------------------------------------------------------------------------------------------------------
on master:
sudo apt install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt install ansible

----------------------------------------------------------------------------------------------------------------------------------------

on host:
 
 sudo apt-get update
 sudo apt-get install python

----------------------------------------------------------------------------------------------------------------------------------------
on master: ssh-keygen for keyless SSH
on slave:  sudo nano .ssh/authorized_keys

----------------------------------------------------------------------------------------------------------------------------------------
 on master:
  sudo nano/etc/ansible/hosts
   create a group_name as [production]
   
ANSIBLE COMMANDS

ansible -m ping slave1

for creating playbook: sudo nano playbook_name.yaml
for running playbook:  ansible-playbook playbook_name.yaml

----------------------------------------------------------------------------------------------------------------------------------------for server hardening switch to security groups and change the outbound rules of the instances to HTTP/HTTPS and make yur IP visible from anywhere.
 

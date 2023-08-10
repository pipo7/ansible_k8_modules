# Pre-requisite 
Python3, Docker and Kubernetes installed on preferrably Ubuntu system
https://docs.k3s.io/quick-start
https://docs.docker.com/engine/install/ubuntu/

# Ansible Kubernetes Module
https://docs.ansible.com/ansible/latest/collections/kubernetes/core/index.html

Install K8 collection using
```
ansible-galaxy collection install kubernetes.core
```

Check whether installed ok using 
```
ansible-galaxy collection list | grep kube
```
output : kubernetes.core 2.4.0  

Install other requried softwares
```
   sudo apt install python3-jsonpatch
   sudo apt install python3-pip 
   sudo pip3 install PyYAML 
```
Test the installation using 
```
python3 -m pip show PyYAML 
```

Important to install: 
``` 
pip3 install pyyaml kubernetes --user 
```
If using Openshift then use ``` pip3 install pyyaml openshift kubernetes --user ```


# Python Compatibility
Use below line in vars or in ansible.cfg as :

```
ansible_python_interpreter=/usr/bin/python3
```

  In host file as:
```
[controlVMs]
controlVM ansible_connection=local ansible_python_interpreter=/usr/bin/python3 
```

# Check that ports are allowed on Network on given nodes
```
sudo ufw allow 30007
```
on Ubuntu VM/machine you can use ufw firewall Or can have firewall disabled for this proof of concept.

# How to Run playbooks together :
ansible-playbook site.yml 

# References :
https://docs.ansible.com/ansible/latest/collections/kubernetes/core/index.html#description
https://stackoverflow.com/questions/60866755/ansible-k8s-module-failed-to-import-the-required-python-library-openshift-on

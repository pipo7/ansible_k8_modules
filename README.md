# Ansible Kubernetes Module

Install using
```ansible-galaxy collection install kubernetes.core```

Check whether installed ok using 
```ansible-galaxy collection list | grep kube```
output : kubernetes.core 2.4.0  

Install other requried softwares
```sudo apt install python3-jsonpatch```

```sudo apt install python3-pip```
```sudo pip3 install PyYAML ```
Test the installation using 
```python3 -m pip show PyYAML ```

Importatn to install: 
``` pip3 install pyyaml kubernetes --user ```


References :
https://stackoverflow.com/questions/60866755/ansible-k8s-module-failed-to-import-the-required-python-library-openshift-on
# Create Secret from file(s) in Kubernetes using the Kubernetes Ansible module

1. Create cluster with `kind`:
```
kind create cluster --name ansible-lab
```

2. Write the kubeconfig to file:
```
kind get kubeconfig --name ansible-lab > ansible-lab.kubeconfig
```

3. Source your virtual environment containing Ansible.

4. Install needed Python modules to interact with Kubernetes:
```
ansible-galaxy collection install kubernetes.core
pip install kubernetes
```

5. Run playbook:
```
ansible-playbook -i hosts playbook.yml
```
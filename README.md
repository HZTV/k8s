# k8s



## Задание 1

# 1.1
root@fhm1j15h1095nij2tpf1:/home/ubuntu/.kube# microk8s status --wait-ready
microk8s is running
high-availability: no
  datastore master nodes: 127.0.0.1:19001
  datastore standby nodes: none
addons:
  enabled:
    dashboard            # (core) The Kubernetes dashboard
    dns                  # (core) CoreDNS
    ha-cluster           # (core) Configure high availability on the current node
    helm                 # (core) Helm - the package manager for Kubernetes
    helm3                # (core) Helm 3 - the package manager for Kubernetes
    metrics-server       # (core) K8s Metrics Server for API access to service metrics
  disabled:
    cert-manager         # (core) Cloud native certificate management


root@fhmfi5uhvttfb4de70ho:~/.kube# microk8s status --wait-ready
microk8s is running
high-availability: no
  datastore master nodes: 127.0.0.1:19001
  datastore standby nodes: none
addons:
  enabled:
    dashboard            # (core) The Kubernetes dashboard
    dns                  # (core) CoreDNS
    ha-cluster           # (core) Configure high availability on the current node
    helm                 # (core) Helm - the package manager for Kubernetes
    helm3                # (core) Helm 3 - the package manager for Kubernetes
    metrics-server       # (core) K8s Metrics Server for API access to service metrics
  disabled:
    cert-manager         # (core) Cloud native certificate management

# 1.2

microk8s status
microk8s is running
high-availability: no
  datastore master nodes: 127.0.0.1:19001
  datastore standby nodes: none
addons:
  enabled:
    dashboard            # (core) The Kubernetes dashboard
    dns                  # (core) CoreDNS
    ha-cluster           # (core) Configure high availability on the current node
    helm                 # (core) Helm - the package manager for Kubernetes
    helm3                # (core) Helm 3 - the package manager for Kubernetes
    metrics-server       # (core) K8s Metrics Server for API access to service metrics
  disabled:
    cert-manager         # (core) Cloud native certificate management



#1.3
root@fhmfi5uhvttfb4de70ho:~/.kube# microk8s kubectl create token default
eyJhbGciOiJSUzI1NiIsImtpZCI6Ino0N2ZybDdqM2d0ay1naVRyNU5yY3VpdGJuT0o4U3l1cV9zSTJ5bEdONjAifQ.eyJhdWQiOlsiaHR0cHM6Ly9rdWJlcm5ldGVzLmRlZmF1bHQuc3ZjIl0sImV4cCI6MTczMTUzMTk2NywiaWF0IjoxNzMxNTI4MzY3LCJpc3MiOiJodHRwczovL2t1YmVybmV0ZXMuZGVmYXVsdC5zdmMiLCJqdGkiOiJhYTczOTE4Ny1lZTNlLTRmMDEtOTk5OC03ZGYxYzk1NDUyNzEiLCJrdWJlcm5ldGVzLmlvIjp7Im5hbWVzcGFjZSI6ImRlZmF1bHQiLCJzZXJ2aWNlYWNjb3VudCI6eyJuYW1lIjoiZGVmYXVsdCIsInVpZCI6IjlhYjA4ZDYwLWJlNzItNDJiMS05NzQ3LThmNTZmMjIyMTNlYiJ9fSwibmJmIjoxNzMxNTI4MzY3LCJzdWIiOiJzeXN0ZW06c2VydmljZWFjY291bnQ6ZGVmYXVsdDpkZWZhdWx0In0.Fa1T81lTf0WXdl6VTKqsEPFv1tCc0S1wBi5TMYzxN-ZOMo2lDnHUcYQ66uvd4oHs_-KThG7BwTG_xFoJuF3WILIXOLlVYZZc2k53Dd-OoftNFQfgunEs1CDcggh1njDhrSNbN02XUnQWYNk6wXtIC0swoWhrf6ZwciuRr0tE77hYU5qXIf5jrxuOjJgO2KZ22ML_5RH3vats4Xt7IVtU8YW-F1eGJvULjvspXn3RlecrQyf-r37U9aqvTyoY4oC7NSqGbSmHTbyrhUnDgJoFnccEpxWJGeN5eKgntuY2NoqvNjXUFdhqfPh68wuu6rlkqLgktQlp6tLMFkcyzr8SEQ

## Задание 2

# 2.1


#2.2
root@fhmfi5uhvttfb4de70ho:~/.kube# kubectl get nodes
NAME                   STATUS   ROLES    AGE   VERSION
fhm1j15h1095nij2tpf1   Ready    <none>   22h   v1.31.2

# 2.3 
root@fhmfi5uhvttfb4de70ho:~/.kube# microk8s kubectl port-forward -n kube-system service/kubernetes-dashboard 10443:443 --address 0.0.0.0
Forwarding from 0.0.0.0:10443 -> 8443
Handling connection for 10443
Handling connection for 10443
![image](https://github.com/user-attachments/assets/4f922338-8ee2-474d-b144-fe5703cfcb43)

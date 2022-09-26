# k8s-playground


# AKS Playground

## az cli ubuntu

- sudo apt-get install azure-cli

## kubectl ubuntu 

 - https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/

```bash
sudo apt-get update
sudo apt-get install -y apt-transport-https ca-certificates curl
sudo curl -fsSLo /usr/share/keyrings/kubernetes-archive-keyring.gpg https://packages.cloud.google.com/apt/doc/apt-key.gpg
echo "deb [signed-by=/usr/share/keyrings/kubernetes-archive-keyring.gpg] https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee /etc/apt/sources.list.d/kubernetes.list
sudo apt-get update
sudo apt-get install -y kubectl
```
## az aks login (win/wsl2/ubuntu)

```cmd
az login  --scope https://management.core.windows.net//.default
az account set --subscription ******
az aks get-credentials --resource-group aks-playground --name aks-playground
```
## aks get deployments

### win

```cmd
PS C:\GITHUB\k8s-playground> kubectl get deployments --all-namespaces=true
NAMESPACE     NAME                 READY   UP-TO-DATE   AVAILABLE   AGE
kube-system   coredns              2/2     2            2           4m30s
kube-system   coredns-autoscaler   1/1     1            1           4m30s
kube-system   metrics-server       2/2     2            2           4m30s
kube-system   tunnelfront          1/1     1            1           4m30s
```

### wsl2

```bash
max@LI-148:~$ kubectl get deployments --all-namespaces=true
NAMESPACE     NAME                 READY   UP-TO-DATE   AVAILABLE   AGE
kube-system   coredns              2/2     2            2           17m
kube-system   coredns-autoscaler   1/1     1            1           17m
kube-system   metrics-server       2/2     2            2           17m
kube-system   tunnelfront          1/1     1            1           17m
```

### Ubuntu 20.04 LTS 

```bash
max@aks-playground:~$ kubectl get deployments --all-namespaces=true
NAMESPACE     NAME                 READY   UP-TO-DATE   AVAILABLE   AGE
kube-system   coredns              2/2     2            2           45m
kube-system   coredns-autoscaler   1/1     1            1           45m
kube-system   metrics-server       2/2     2            2           45m
kube-system   tunnelfront          1/1     1            1           45m
```
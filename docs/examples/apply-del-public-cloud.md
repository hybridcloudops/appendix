Context "minikube":
```
Kubernetes master is running at https://192.168.39.226:8443
KubeDNS is running at https://192.168.39.226:8443/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy
```

Context "bsc-aks":
```
Kubernetes master is running at https://bscaks-1b28655a.hcp.eastus2.azmk8s.io:443
CoreDNS is running at https://bscaks-1b28655a.hcp.eastus2.azmk8s.io:443/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy
Metrics-server is running at https://bscaks-1b28655a.hcp.eastus2.azmk8s.io:443/api/v1/namespaces/kube-system/services/https:metrics-server:/proxy
```

Changed public cloud resources to unsupported to delete from AKS:

```
Installing private cloud services
======================================

Switch to private cloud environment:
Switched to context "minikube".
Client Version: v1.17.2
Server Version: v1.17.2

Apply supported services:
deployment.apps/grafana unchanged
service/grafana unchanged
namespace/monitoring unchanged
configmap/prometheus-config unchanged
clusterrole.rbac.authorization.k8s.io/prometheus unchanged
serviceaccount/default unchanged
clusterrolebinding.rbac.authorization.k8s.io/prometheus unchanged
deployment.apps/prometheus unchanged
service/prometheus unchanged
deployment.apps/rest-qkt-deployment unchanged
service/rest-qkt-service unchanged

Delete unsupported services:
No resources found

Installing public cloud services
======================================

Switch to public cloud environment:
Switched to context "bsc-aks".
Client Version: v1.17.2
Server Version: v1.15.10

Apply supported services:
error: no objects passed to apply

Delete unsupported services:
deployment.apps "azure-vote-back" deleted
service "azure-vote-back" deleted
deployment.apps "azure-vote-front" deleted
service "azure-vote-front" deleted

Switch to private cloud environment:
Switched to context "minikube".

Installing legacy services
======================================
Nothing to do
```

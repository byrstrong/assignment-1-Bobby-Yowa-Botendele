## 
## >DEPLOY A LIGHTWEIGHT KUBERNETES CLUSTER (K3S) 3 MASTERS NODES FOR HIGH AVAILABILITY ON AWS>

> For the full K3s documentation see <https://docs.k3s.io/>.

## ACHITECTURE
3 instances type: t3.large (2 vcpu / 8 GIB RAM, 50gb SSD): ubuntu 22.04 LTS Operating System.
<img width="2560" height="1440" alt="instances" src="https://github.com/user-attachments/assets/2c0efd32-d5cd-434d-a7f0-4f2992a2df6c" />
## Create new key pair and save it on your local pc.
### CREATE A SECURITY GROUP
Give a name to security group: - Authorize portS: TCP 22 for encrypted remote administration and file tranfers. to access the instance from local pc;
TCP 6443 for secure (HTTPS) communication by Kubernetes API server; TCP 2379-2380 used by etcdctl,other etcd nodes in the cluster to handle requests from external clients or other services;
TCP 10250 for communication between Kubernetes API server and kubelet running on each node; TCP 30000-32767 for NodePort to expose applications externally;
UDP 8472 for Flannel VXLAN to allow nodes to communicate accrodd a virtual Layer 2 over a Layer 3 infractructure.

## Hostname, Private IPS and Publc IPS
record the values for future use in the process
## To ACCESS NODE LOCALLY TO YOUR TERMINAL
open your local terminal
sudo 



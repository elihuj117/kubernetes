# Kubernetes

## metal-lb
MetalLB allows you to create Kubernetes services of type LoadBalancer in on-premise clusters. Documentation can be found [here](https://metallb.universe.tf/). 

##### To get started with metal-lb

Modify metallb-config.yaml to adjust the address pool to suit your network
```
kubectl apply -f https://raw.githubusercontent.com/elihuj117/kubernetes/master/metal-lb/namespace.yaml
kubectl apply -f https://raw.githubusercontent.com/elihuj117/kubernetes/master/metal-lb/metallb-config.yaml
kubectl apply -f https://raw.githubusercontent.com/elihuj117/kubernetes/master/metal-lb/metallb.yaml
```
## nfs-test
Stuff for some asshole

## vsphereCSI
vSphere Container Storage Interface (CSI). Official documentation can be found [here](https://github.com/kubernetes-sigs/vsphere-csi-driver) and [here](https://cloud-provider-vsphere.sigs.k8s.io/tutorials/enabling-vsphere-csi-on-an-existing-cluster.html).

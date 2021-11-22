# Kubernetes
Collection of artifacts for Kubernetes use in my lab.

## Elasticsearch
EFK stack deployment (Elasticsearch, Fluentd, Kibana). LoadBalancer service provided by [metal-lb](https://metallb.universe.tf/). 

Images used:
- docker.elastic.co/elasticsearch/elasticsearch:7.10.0
- docker.elastic.co/kibana/kibana:7.10.0
- fluent/fluentd-kubernetes-daemonset:v1.4.2-debian-elasticsearch-1.1

```elastic-pvc.yaml``` using ```managed-nfs``` storage class.

## Grafana
Grafana deployment with InfluxDB, and Telegraf. 

Images used:
- grafana/grafana
- influxdb:1.8
- telegraf

Persistent Volume Claims using the ```vsphere-local``` storage class. Leveraging the vSphere CSI to enable vSphere to provision Persistent Volumes. Official documentation can be found [here](https://github.com/kubernetes-sigs/vsphere-csi-driver) and [here](https://cloud-provider-vsphere.sigs.k8s.io/tutorials/enabling-vsphere-csi-on-an-existing-cluster.html).

## phpIPAM
```frontend.yaml``` contains a multi-POD deployment.

Images used:
- phpipam/phpipam-www:1.5x
- phpipam/phpipam-cron:1.5x
- mysql:5.6

## Joomla

Images used:
- joomla:3.9-php7.2-apache
- mysql:5.6

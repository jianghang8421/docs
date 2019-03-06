---
title: Using Rancher to manage ARM64 Kubernetes
weight: 50
---

Rancher currently supports the following two ways to manage ARM64 platform kubernetes clusters.

- Import ARM64 Kubernetes clusters
- Create ARM64 Kubernetes clusters with custom nodes

### Import ARM64 Kubernetes clusters

You can import an existing ARM64 platform Kubernetes cluster and then manage it using Rancher.  
The rancher agent image is published using the [docker manifest](https://docs.docker.com/engine/reference/commandline/manifest/), so when you are importing clusters you don't need to change any configurations.

About how to import Kubernetes clusters, please refer to the [Importing Kubernetes Clusters]({{< baseurl >}}/rancher/v2.x/en/cluster-provisioning/imported-clusters/) section.

### Create ARM64 Kubernetes clusters with custom nodes

Rancher supports creating ARM64 platform Kubernetes clusters with your custom nodes. 
All the images which Rancher using to create Kubernetes clusters are published using the [docker manifest](https://docs.docker.com/engine/reference/commandline/manifest/), so you don't need to change any configurations to create ARM64 platform Kubernetes clusters.

You can check what images rancher is using to create Kubernetes clusters in [this file](https://github.com/rancher/types/blob/master/apis/management.cattle.io/v3/k8s_defaults.go).

> Currently Rancher only supports using `Flannel` network plugin to create ARM64 platform Kubernetes clusters. 
> Currently only `v1.12.6-rancher1-2` and `v1.13.4-rancher1-1` versions ARM64 Kubernetes are supported.

About how to create Kubernetes clusters with custom nodes, please refer to the [Creating a Cluster with Custom Nodes]({{< baseurl >}}/rancher/v2.x/en/cluster-provisioning/custom-clusters/) section.

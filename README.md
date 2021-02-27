# hetzner-kubernetes

A learning by doing ansible repository to manage my personal kubernetes cluster on hetzner cloud.

## Usage

1. Install `hetzner.hcloud` extension and the `hcloud` library  
```
ansible-galaxy collection install hetzner.hcloud
sudo pip3 install hcloud
```
2. Create a new porject on hetzner cloud and generate an API key
3. Set the `HCLOUD_TOKEN` environment variable to your API key

## Settings/Config

- __kubernetes-config.yaml__: Configure the vm location and type, kubernetes version etc. of your cluster.


## Playbooks

- __provision-master.yaml__: Create a master node and initialize a new cluster. In case the cluster is already set up, this script can be used to reset the cluster configuration.
- __add-worker.yaml__: Create a new worker and attachs it to the existing master.
- __drain-worker.yaml__: Remove a worker.

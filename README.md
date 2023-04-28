
# Vagrantfile and Scripts to Automate Kubernetes Setup using Kubeadm [Practice Environment for CKA/CKAD and CKS Exams]
Version for libvirt
## Documentation

Current k8s version for CKA, CKAD and CKS exam: 1.26

Refer this link for documentation: https://devopscube.com/kubernetes-cluster-vagrant/

## 🚀 CKA, CKAD, CKS or KCNA Coupon Codes

If you are preparing for CKA, CKAD, CKS, or KCNA exam, **save 30%** today using code **HOMERUN30** at https://kube.promo/devops. It is a limited-time offer. Or Check out [Linux Foundation coupon](https://scriptcrunch.com/linux-foundation-coupon/) page for the latest voucher codes.

## Prerequisites

1. Working Vagrant setup
2. 8 Gig + RAM workstation as the Vms use 3 vCPUS and 4+ GB RAM


Run below commands
Install vagramt sshfs pugin:

```shell
vagrant plugin install vagrant-sshfs
```

## Bring Up the Cluster

To provision the cluster, execute the following commands.

```shell
git clone https://github.com/scriptcamp/vagrant-kubeadm-kubernetes-libvirt.git
cd vagrant-kubeadm-kubernetes-libvirt
mkdir vagrant
vagrant up --no-parallel
```
## Set Kubeconfig file variable

```shell
cd vagrant-kubeadm-kubernetes-libvirt
cd vagrant
export KUBECONFIG=$(pwd)/config
```

or you can copy the config file to .kube directory.

```shell
cp config ~/.kube/
```


## To shutdown the cluster,

```shell
vagrant halt
```

## To restart the cluster,

```shell
vagrant up
```

## To destroy the cluster,

```shell
vagrant destroy -f
```
After destroying cluster remove all files from vagrant folder

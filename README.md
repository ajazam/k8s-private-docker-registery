# Instructions to create a private docker registry in kubernete, using NFS as persistent storage
The files are based on files found in https://github.com/kubernetes/examples/tree/master/staging/volumes/nfs and https://github.com/kubernetes/kubernetes/tree/master/cluster/addons/registry

I have minor changes to the original files.

nfs-pv has a custom size, nfs server IP address and path for my specific requirements.

I have also used an upto date version of the docker registry (2.6.2 at the time of writing).

# Installation
sudo kubectl create -f nfs-pv.yaml

sudo kubectl create -f nfs-pvc.yaml

sudo kubectl create -f registry-rc.yaml

sudo kubectl create -f registry-svc.yaml

# Troubleshooting
Useful [Kubectl cheatsheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

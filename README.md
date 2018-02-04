# kubernetes-playground

# Installing K8s

- `brew install kubectl` 
    - Kubectl is a command line interface for running commands against Kubernetes clusters. 
- `brew cask install minikube`
    - Minikube is a tool that makes it easy to run Kubernetes locally.
- `brew install docker-machine-driver-xhyve`
    -  The xhyve hypervisor is a port of bhyve to OS X. It is built on top of Hypervisor.framework in OS X 10.10 Yosemite and higher, runs entirely in userspace, and has no other dependencies.
- After installing xhyve you need to execute the following
commands:
    - `sudo chown root:wheel /usr/local/opt/docker-machine-driver-xhyve/bin/docker-machine-driver-xhyve`
    - `sudo chmod u+s /usr/local/opt/docker-machine-driver-xhyve/bin/docker-machine-driver-xhyve`
    
# Starting K8s
    - `minikube start --vm-driver=xhyve`
    
# Check K8s Context

Should you wish to see which context kubectl is talking
to, you can execute the following command:

`kubectl config current-context`

Kubectl can even talk to your production cluster and you 
can even switch back to your local cluster. To do this 
you need to specify the contexts.

# Listing Nodes in the Cluster

Should you wish to list nodes in the cluster you can execute:

`kubectl get nodes`
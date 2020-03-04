# Intro to DevOps and Kubernetes: Day 1

You're welcome to run a Kubernetes cluster on your own machines but because this takes a lot of resources we're going to use a web playground for this.

1) Goto https://www.katacoda.com/courses/kubernetes/playground and follow the instructions to start your cluster

2) Run `git clone https://github.com/todaywasawesome/color-coded.git` This will make a copy of some files that we can use to setup our app on the Kuberentes cluster.

3) Run `cd color-coded/deploy/kubernetes/` This will put us into a directory with some different config files we can use. 

4) Run `kubectl apply -f  blue.deployment.yaml` 

5) Run `kubectl apply -f blue.service.yaml`

You've now deployed the Color Coded application!

6) Browse around to see what you've created using the following commands:
	- `kubectl get deployments`
	- `kubectl get pods`
	- `kubectl get services`

7) Checkout our service by clicking the "+" button next to the terminal and clicking "select port view on Host 1" and put in the port `31361` 

8) Back in your window run `watch kubectl get pods`

 
=Intro to DevOps and Kubernetes: Day 2
== Running a Kubernetes Cluster


===1) Setup a cluster with two nodes

Goto https://www.katacoda.com/courses/kubernetes/getting-started-with-kubeadm to get an environment and follow the instructions. This will all you to:

	- Create a two node cluster
	- Setup a CNI (networking) provider
	- Deploy an app
	- Start the Kubernetes Dashboard
	- View the dashboard

===2) Expand on Kubernetes concepts

While in the environment above, lets introduce namespaces. 

	- `kubectl get namespaces`
	- `kubectl create namespace test`

===3) Deploy our app again, but this time in two namespaces

	- Clone the repo `git clone https://github.com/todaywasawesome/color-coded.git`	
	- Run `cd color-coded/deploy/kubernetes/` This will put us into a directory with some different config files we can use. 
	- Run `kubectl apply -f  blue.deployment.yaml --namespace test` 
	- Run `kubectl apply -f blue.service.yaml --namespace test`
	- Run `kubectl get pods` What's wrong? No pods? Try again with the `--namespace test` flag or `-n test`

Great! Now you have an intro to namespaces!
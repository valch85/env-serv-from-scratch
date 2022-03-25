## env-serv-from-scratch
consist files to spinup k8s on AWS for some services

# terraform
spin up eks clustrer in eu-central-1 region (2 worker nodes) with kubernetes dashboard
to add creds for the cluster: aws eks --region $(terraform output -raw region) update-kubeconfig --name $(terraform output -raw cluster_name)

# metrics-server-0.3.6
kubectl apply -f metrics-server-0.3.6/deploy/1.8+/

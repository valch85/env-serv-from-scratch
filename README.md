# env-serv-from-scratch
consist files to spinup k8s on AWS for some services

## terraform
spin up eks clustrer in eu-central-1 region (2 worker nodes) with kubernetes dashboard
to add creds for the cluster:
`aws --profile env-serv-from-scratch eks --region $(terraform output -raw region) update-kubeconfig --name $(terraform output -raw cluster_name)`

## metrics-server-0.3.6
`kubectl apply -n kube-system -f metrics-server-0.3.6/deploy/1.8+/`

## deploy kubernetes dashboard
`kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.0.0-beta8/aio/deploy/recommended.yaml`

`kubectl proxy`


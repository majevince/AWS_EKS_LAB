Launch Kubectl Server
Configure Kubectl

In the curl command, I am using Kubernetes 1.23 you can use any latest

curl -O https://s3.us-west-2.amazonaws.com/amazon-eks/1.23.17/2023-05-11/bin/linux/amd64/kubectl



openssl sha1 -sha256 kubectl

chmod +x ./kubectl

mkdir -p $HOME/bin && cp ./kubectl $HOME/bin/kubectl && export PATH=$HOME/bin:$PATH

kubectl version --short --client



aws configure



See the below command and replace it with the name of your EKS cluster and with the AWS region where the cluster is located.

aws eks update-kubeconfig -- name <your-cluster-name> -- region <your-region>

kubectl get nodes



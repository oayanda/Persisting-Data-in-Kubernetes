# Persisting Data in Kubernetes


Check the current identity to verify that you're using the correct credentials that have permissions for the Amazon EKS cluster:

```bash
aws sts get-caller-identity
```

```bash
# Create a k8s cluster in AWS EKS via CLI
eksctl create cluster \
  --name oayanda-cluster \
  --version 1.24 \
  --region us-east-1 \
  --nodegroup-name Linux-node \
  --nodes 2 \
  --nodes-min 1 \
  --nodes-max 4 \
  --node-type t3.micro \
  --node-volume-size 8 \
  --ssh-access \
  --ssh-public-key instance \
  --managed
  ```



  ```bash
  # Delete EKS Cluster
  eksctl delete cluster oayanda-cluster
  ```

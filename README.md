# AWS EKS Cluster provisioning with Terraform

The terraform file is divided into two blocks:
  1. The first block is the VPC module.

  In this part, we will instruct Terraform to create:

  A VPC.
  Three private and three public subnets.
  A single NAT gateway.
  Tags for the subnets.
  The tags for subnets are quite crucial as those are used by AWS to automatically provision public 
  and internal load balancers in the appropriate subnets.

  2. Terraform EKS cluster module.
  
  The EKS module is in charge of:

  Creating the control plane.
  Setting up autoscaling groups.
  Setting up the proper security groups.
  Creating the kubeconfig file.

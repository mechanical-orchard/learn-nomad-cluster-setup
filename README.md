# Set up a Nomad cluster on GCP

This repo is a custom companion to the [Cluster Setup](https://developer.hashicorp.com/nomad/tutorials/cluster-setup) collection of tutorials, containing configuration files to create a Nomad cluster with ACLs enabled on GCP.

## From the tutorial

```
 gcloud auth login
 gcloud config set project PROJECT_ID
 gcloud config set compute/region GCP_REGION
 gcloud config set compute/zone GCP_ZONE
 cp variables.hcl.example variables.hcl
 # Update variables
 packer init image.pkr.hcl
 packer build -var-file=variables.hcl image.pkr.hcl 
 # Get new uuids
 terraform console
 > uuid()
 # Update variables
 terraform init
 terraform apply -var-file=variables.hcl
 ./post-setup.sh
 # Apply the export commands from the output.
 ...
 Profit?
```

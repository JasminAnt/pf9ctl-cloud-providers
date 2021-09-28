# pf9ctl_cloud_providers

### Purpose
   CLI tool for Platform9 cloud provider checks
   
### Usage
- Downloading the CLI 
```sh
bash <(curl -sL https://pmkft-assets.s3-us-west-1.amazonaws.com/pf9ctl_setup) 
```
- **Help** 
```sh
#pf9ctl --help

CLI tool for Platform9 cloud provider checks.

Usage:
  pf9ctl [command]

Available Commands:
  check-amazon-provider checks if user has amazon cloud permisisons
  check-azure-provider  checks if user has azure cloud permisisons
  check-google-provider checks if user has google cloud permisisons
  completion            generate the autocompletion script for the specified shell
  help                  Help about any command

Flags:
  -h, --help      help for pf9ctl
      --verbose   print verbose logs

Use "pf9ctl [command] --help" for more information about a command.
```
- **Version**

  **This command is used to get the current version of the CLI**
```sh
#pf9ctl version

pf9ctl version: v1.3
``` 

**check-amazon-provider**
```sh
#pf9ctl check-amazon-provider iamUser access-key secret-key us-east-1

✓ ELB Access
✓ Route53 Access
✓ Availability Zones success
✓ EC2 Access
✓ VPC Access
✓ IAM Access
✓ Autoscaling Access
✓ EKS Access
```
**check-google-provider**
```sh
#pf9ctl check-google-provider /home/duser/Downloads/service-account.json testProject user@email.com

✓  Success roles/iam.serviceAccountUser
✓  Failed roles/container.admin
✓  Failed roles/compute.viewer
✓  Success roles/viewer
```

**check-azure-provider**
```sh
#pf9ctl check-google-provider tenantID clientID subscriptionID secretKey

✓ Has access
```
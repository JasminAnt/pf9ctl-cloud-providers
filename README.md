# pf9ctl_cloud_providers

### Purpose
   CLI tool for Platform9 cloud provider checks
   
### Usage
- Downloading the CLI 
```sh
bash <(curl -sL https://jasmind.s3.us-west-2.amazonaws.com/pf9ctl-OS)
chmod +x pf9ctl-OS

Currently supported OS: win32, win64, linux32, linux64, mac64
Example: 
bash <(curl -sL https://jasmind.s3.us-west-2.amazonaws.com/pf9ctl-mac64)
chmod +x pf9ctl-mac64
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
#pf9ctl check-amazon-provider -i iamUser -a access-key -s secret-key -r us-east-1

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
#pf9ctl check-google-provider -p /home/duser/Downloads/service-account.json -n testProject -e user@email.com

✓  Success roles/iam.serviceAccountUser
✓  Failed roles/container.admin
✓  Failed roles/compute.viewer
✓  Success roles/viewer
```

**check-azure-provider**
```sh
#pf9ctl check-google-provider -t tenantID -c clientID -s subscriptionID -k secretKey

✓ Has access
```

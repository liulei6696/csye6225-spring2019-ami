# AWS AMI for CSYE 6225

## Team Information

| Name | NEU ID | Email Address |
| --- | --- | --- |
| Junyi Fang | 001495265 | fang.ju@husky.neu.edu  |
|  Ziyan Zhu | 001461543 | zhu.ziy@husky.neu.edu  |
|   Lei Liu  | 001443309 | liu.lei1@husky.neu.edu |

## Validate Template

```
packer validate centos-ami.json
```

## Build AMI

```
export PACKER_LOG_PATH="./centos-ami.log"
export PACKER_LOG=10
packer build centos_64.json

```

## Run Instructions
To create the application resources with AWS CloudFormation:
1. Download/Clone the repository and go to the directory /csye6225-spring2019-ami/infrastructure/aws/cloudformation
2. Set up permission for the set-up script with command: `chmod +x ./csye6225-aws-cf-create-application-stack.sh`
3. Set up the infrastructure with command: `./csye6225-aws-cf-create-application-stack.sh`

To clean up the application resources with AWS CloudFormation:
1. Go to the directory /csye6225-spring2019-ami/infrastructure/aws/cloudformation
2. Set up permission for the tear-down script with command: `chmod +x ./csye6225-aws-cf-terminate-application-stack.sh`
3. Clean up the infrastructure with command: `./csye6225-aws-cf-terminate-application-stack.sh`

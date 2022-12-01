# Installing or updating the latest version of the AWS CLI

1.Download and run the AWS CLI MSI installer for Windows (64-bit): https://awscli.amazonaws.com/AWSCLIV2.msi

2.Run command : msiexec.exe /i https://awscli.amazonaws.com/AWSCLIV2.msi

3 Verify installation with command : aws --version

# Profile configuration in CLI

For Dev account

Run command : aws configure --profile=dev

For Demo/Prod account

Run command : aws configure --profile=prod


# Setting up Infrastructure using the Cloud Formation template

aws cloudformation create-stack --stack-name assignment6 --template-body file://infrastructure.yaml --parameters ParameterKey=amiId,ParameterValue=ami-03bfd684634fdd769 ParameterKey=HostedZoneName,ParameterValue=prod.sagarmalhotra.me. --region us-east-1 --profile demo --capabilities CAPABILITY_NAMED_IAM
  
# Cleaning up the infrastructure
  
aws cloudformation delete-stack --stack-name (name of the stack you want to delete) --profile (Profile you want to delete stack with) --region (region name)
  
# command to add ssl certificate to AWS
aws acm import-certificate --certificate fileb://certificate.pem --certificate-chain fileb://ca_bundle.pem --private-key fileb://private.key --profile demo





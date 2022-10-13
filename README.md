#Installing or updating the latest version of the AWS CLI

1.Download and run the AWS CLI MSI installer for Windows (64-bit): https://awscli.amazonaws.com/AWSCLIV2.msi

2.Run command : msiexec.exe /i https://awscli.amazonaws.com/AWSCLIV2.msi

3 Verify installation with command : aws --version

#Profile configuration in CLI

For Dev account

Runn command : aws configure --profile=dev

Add account id

Add secret key

Add region

Add output type

For Demo/Prod account

Runn command : aws configure --profile=prod

Add account id

Add secret key

Add region

Add output type

#Setting up Infrastructure using the Cloud Formation template

aws cloudformation create-stack --stack-name <name of the stack you want to create> --template-body file://vpc_template.yaml --profile <Profile you want to create stack with>
  
#Cleaning up the infrastructure
  
aws cloudformation delete-stack --stack-name <name of the stack you want to delete> --profile <Profile you want to delete stack with>
  





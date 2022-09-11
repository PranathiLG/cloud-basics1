##This Cloudformation template creates an Amazon EC2 instance running the Amazon Linux AMI. The AMI is chosen based on the region in which the stack is run. This example creates an EC2 security group for the instance to give you SSH access. 

**WARNING** This template creates an Amazon EC2 instance. You will be billed for the AWS resources used if you create a stack from this template.


Steps:
1. Fork or clone this repository
2. Configure AWS CLI in your local machine
3. Run the following command to create the ec2 instance and security group in your AWS account


```
aws cloudformation create-stack \
  --stack-name my_cloudbasic_ec2 \
  --template-body ec2_securitygroup.template \
  --parameters KeyName=General
  ```

  Note: Replace "General" KeyName with your EC2 KeyPair name
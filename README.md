# Launching an EC2 Instance Using AWS CLI
### Step 1: Configure AWS CLI using IAM Credentials “ aws –version ” to confirm version installed 
### “ aws configure ” to configure AWS CLI
![Bashshell image](./pictures/1%20iamge.jpg)
### Step 2: Create key pair input: “aws ec2 create-key-pair --key-name YourKeyName --query 'KeyMaterial' -
### -output text > YourKeyName.pem”
![creating a keypair](./pictures/2%20image.jpg)

![confirm keypair created at console](./pictures/3%20image.jpg)

### Step 3: Create Security group input “ aws ec2 create-security-group --group-name --description "" ”
![Create security group](./pictures/4%20image.jpg)
![Confirm security group on console](./pictures/5%20image.jpg)

### Step 4: Launch instance 
### Add inbound rule: “ aws ec2 authorize-security-group-ingress --group-id -- protocol tcp --port --cidr ”
### Launch instance: “ aws ec2 run-instances --image-id --count 1 --instance-type -- keyname --security-groups “
![Instance result on bash shell](./pictures/6%20image.jpg)
![Instance result on bash shell](./pictures/7%20image.jpg)
![Instance result on bash shell](./pictures/8%20image.jpg)
![Confirm instance has been launched on console](./pictures/9%20image.jpg)
![Confirm instance has been launched on console](./pictures/10%20image.jpg)

### Step 5: View running Instance input “ aws ec2 describe-instances “
![View running instances](./pictures/11%20image.jpg)

### Step 6: Terminate running instance input “ aws ec2 terminate-instances --instance-ids “
![Terminate instance on CLI](./pictures/12%20image.jpg)
![Confirm instance terminated on console](./pictures/13%20image.jpg)

### Step 7: delete keypair and security group 
### Delete keypair: “ aws ec2 delete-key-pair --key-name “
![Delete keypair](./pictures/14%20mage.jpg)
### Confirm keypair has been deleted: aws ec2 describe-key-pairs
![Confirm keypair deletion](./pictures/15%20image.jpg)
### Delete security group: “aws ec2 delete-security-group --group-id YourSecurityGroupId “
![confirm security group has been deleted](./pictures/16%20image.jpg)
### confirm security group has been deleted: aws ec2 describe-security-groups
![confirm security group has been deleted](./pictures/17%20image.jpg)
![confirm security group has been deleted](./pictures/18%20image.jpg)
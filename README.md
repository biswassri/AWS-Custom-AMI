# AWS Custom AMi
This repository is create a custom AWS-AMI 

### Install Packer 
 
 wget -q https://releases.hashicorp.com/packer/1.3.4/packer_1.3.4_linux_amd64.zip 
            unzip packer*.zip  
            chmod +x packer

#### Validate Template

packer validate ubuntu-ami.json

#### Build AMI

./packer build \
            -var "aws_region=${AWS_REGION}" \
            -var "aws_access_key=${aws_access_key}" \
            -var "aws_secret_key=${aws_secret_key}" \
            -var "ami_users=${ami_users}" \
            -var "source_ami=${source_ami}" \
            ubuntu-ami.json


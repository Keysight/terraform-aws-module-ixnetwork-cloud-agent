# module-ixnetwork-cloud-agent/aws

## Description
Terraform module for IxNetwork Cloud agent deployment on Amazon Web Services

## Deployment
This module creates a single instance having two network interfaces.

## Usage
```tf
module "Agent" {
	source  = "git::https://github.com/Keysight/terraform-aws-module-ixnetwork-cloud-agent.git"
	Eth0SecurityGroupId = aws_security_group.PublicSecurityGroup.id
	Eth0SubnetId = aws_subnet.PublicSubnet.id
	Eth1SecurityGroupId = aws_security_group.PrivateSecurityGroup.id
	Eth1SubnetId = aws_subnet.PrivateSubnet.id
	PlacementGroupId = aws_placement_group.PlacementGroup.id
}
```

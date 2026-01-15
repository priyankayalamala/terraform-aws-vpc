Terraform AWS VPC

This module creates the following resources.

VPC

IGW

.2 Public subnets in us-east-1a and us-east-1b AZ

.2 Private subnets in us-east-1a and us-east-1b AZ

.2 Database subnets in us-east-1a and us-east-1b AZ.

Public Route table

Private Route table

Database Route table

EIP for NAT

NAT Gateway in public subnet 1a az

IGW route is added to public route table

NAT gateway route to private and database route tables

Route table association with subnets

VPC to default VPC peering

Public route table to default VPC route

Default VPC main route table to created VPC route


**Inputs**

vpc_cidr - (Required). User must supply the CIDR for VPC.

project_name - (Required). User must supply the project nae.

Environment is required .

tags are optional

subnet_cidrs are required






**Outputs**

vpc_id - VPC ID created

public_subnet_ids - 2 public subnet ID created

private_subnet_ids - 2 private subnet ID created

database_subnet_ids - 2 database subnet ID created




AWS VPC Module

This Terraform module creates a Highly Available (HA) VPC architecture using the first two Availability Zones (AZs) automatically.

Resources Created

The following AWS resources are created by this module:

VPC

Internet Gateway with VPC association

2 Public Subnets (AZ 1a and 1b)

2 Private Subnets (AZ 1a and 1b)

2 Database Subnets (AZ 1a and 1b)

Elastic IP

NAT Gateway in Public Subnet (AZ 1a)

Public Route Table

Private Route Table

Database Route Table

Subnet and Route Table Associations

VPC Peering (if user enables it)

Peering routes added to default VPC if acceptor VPC is not explicitly provided

Peering routes added to Public, Private, and Database route tables
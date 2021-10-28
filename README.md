# DataCenter Enviroment 2A

Source Code for this Module (https://github.com/WEEMR/terraform-aws-DataCenter_Enviroment_2A)

Terraform Registery         (https://registry.terraform.io/modules/WEEMR/DataCenter_Enviroment_2A/aws/latest)

Terraform Module that will create the AWS Networking Stack with FGT, Apache Server, Windows Server and utilize AWS Route53 for DNS. 

The module will create the below resources:

- 2 x VPCs, one of Hub and one for Spoke
- Networking Stack (VPC, Subnets, Route Tables, Security Groups and Internet Gateway) - Please refer to the diagram below.
- 2 x FortiGate with 3 interfaces (Two Interfaces in two different Public Subnets and one in the Private subnets)
- Windows Server 2019 Behind the FGT Port 3 [LAN]
- Ubunutu Server with Apache installed, iperf, fzf, pydf, firefox, lynx and elinks installed on it behind the FGT port 3 [LAN]
- Route53 DNS Public Hosted Zones
- VPC Flow Logs


![image](https://user-images.githubusercontent.com/82145296/139334227-f5c2497b-9dc0-4ce7-ab59-434e3cc0b0c6.png)


// The DNS Hosted Zones must be sub-zones for a domain that is registered or managed by AWS Route53 //

// i.e xyz.com is the domain name and you will create the subzone Lab1.xyz.com // 

![image](https://user-images.githubusercontent.com/82145296/139334161-3f79b827-28de-4e94-b5a5-f823ca0d9f80.png)

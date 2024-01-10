# Network-Hardening Using Amazon Inspector and AWS Systems Manager
## Overview
Securing an infrastructure can be a challenge for any company. Companies use many tools to audit networks and find vulnerabilities in systems and applications. This process takes significant time and effort.Amazon Inspector runs scans that analyze all your network configurations-such as security groups, network access control lists (network ACLs), route tables, and internet gateways-together to infer reachability. You don't need to send packets across the virtual private cloud (VPC) network or connect to Amazon Elastic Compute Cloud (Amazon EC2) instance network ports. It’s like packetless network mapping and reconnaissance. 

From Amazon Inspector, you will use the network reachability package to analyze your network configurations to find security vulnerabilities in your EC2 instances. The findings that Amazon Inspector generates also provide guidance about restricting access that is not secure.

## Task 1: Create Two EC2 instances
I have created one instance is a bastion server named BastionServer in a public subnet. The other instance is an application server named AppServer in a private subnet.

![task1](https://github.com/Cloud-Xplorer08/Security-Network-Hardening/assets/71820244/d4331294-7d6c-4123-a291-f3d435039a0d)


![task1b](https://github.com/Cloud-Xplorer08/Security-Network-Hardening/assets/71820244/e70e059a-01f2-4148-86bb-90f542a21d40)

## Task 2: View EC2 instances and add tags

![add tag](https://github.com/Cloud-Xplorer08/Security-Network-Hardening/assets/71820244/9a5942c3-6933-41a8-a171-00186976473e)

## Task 3: Configure and run Amazon Inspector
In this task, we created an assessment target (a collection of the AWS resources that you want Amazon Inspector Classic to analyze). Then you created an assessment template (a blueprint that you use to configure your assessment). We used the template to start an assessment run, which is the monitoring and analysis process that results in a set of findings.

![assesment target created](https://github.com/Cloud-Xplorer08/Security-Network-Hardening/assets/71820244/3f3c0efe-72d9-4fe8-829a-2cd29e2909e0)


![assesment template created](https://github.com/Cloud-Xplorer08/Security-Network-Hardening/assets/71820244/e848270a-1b57-4c75-a4ca-30794aea170c)


![assesment run completed](https://github.com/Cloud-Xplorer08/Security-Network-Hardening/assets/71820244/949ab989-693d-4a62-bd32-1242ba3332aa)

## Task 4: Analyze Amazon Inspector findings
The findings that these rules generate show whether your ports are reachable from the internet through an internet gateway (including instances behind Application Load Balancers or Classic Load Balancers), a VPC peering connection, or a virtual private network (VPN) through a virtual gateway. These findings also highlight network configurations that allow for potentially malicious access, such as mismanaged security groups, ACLs, and internet gateways.

![findings](https://github.com/Cloud-Xplorer08/Security-Network-Hardening/assets/71820244/045f4dd7-c8db-4b04-8d6d-a7848e56cc3f)








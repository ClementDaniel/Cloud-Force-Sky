# Cloud-Force-Sky
 Creating a Cloud Formation template that provisions a VPC with its necessary components and an EC2 instance within the VPC.

 ## VPC
 **What is AWS VPC?**
 Amazon Virtual Private Cloud (Amazon VPC) helps you to run Amazon resources into a virtual network that you’ve mentioned. A virtual private cloud (VPC) is a network that closely 
  matches the old network you would run in your own data center. By “allocating a logically isolated piece of Amazon Web Services (AWS) Cloud,” the Amazon Virtual Private Cloud (VPC) is a for-profit cloud computing business that offers consumers a virtual private cloud.

The Amazon Elastic Compute Cloud (EC2) is accessible to business clients via an IPsec-based virtual private network. In contrast to conventional EC2 instances, to which Amazon assigns internal and external IP numbers, customers can assign IP addresses from one or more subnets.

VPC offers considerably more granular security management by allowing the user to choose which AWS resources are public-facing and which are not. It’s “a combination of the hybrid approach, but it’s also intended to tackle the rising popularity of private clouds,” according to Amazon.

**VPC vs Private Cloud**
With the help of technology like OpenStack or HPE Helion Eucalyptus, Amazon Virtual Private Cloud intends to offer a service comparable to that offered by private clouds. Private clouds, however, frequently also employ tools like OpenShift application hosting and other database systems.

Experts in cloud security cautioned that employing public resources can expose users to compliance risks not present with internal systems, such as a loss of control or service cancellation. Amazon may not even be able to legally notify the client of the security breach of their system if transaction records for a VPC are demanded from them using a national security letter. Even if the real VPC resources were located in a different nation, this would still be true.

## Working of AWS
You have complete control over your virtual networking environment with Amazon Virtual Private Cloud (Amazon VPC), including resource placement, connectivity, and security. Setup your VPC in the AWS service panel to get going. Next, add resources to it such as Amazon Relational Database Service (RDS) instances and Amazon Elastic Compute Cloud (EC2) instances. Define the channels of communication between your VPCs across accounts, Availability Zones, and AWS Regions. 

## Type of Amazon VPC
*AWS VPC Peering:* Through the use of quick and dependable connections, AWS VPC Peering allows two private networks to communicate with one another. To transport traffic between VPC networks or to grant access to resources on one network to another, Amazon VPC peering connections can be used.
Every single AWS account includes a default VPC in every supported region. Peering really permits communication between two VPCs based on the network address of a particular resource. AWS VPC Peering does not, however, provide transitive peering. Simply said, transitive peering means that because VPC-B is connected to VPC-C, VPC-A can communicate with resources in VPC-C via VPC-B. This VPC Peering does not support this kind of networking and communication setup.

## The VPC Architecture:
 **Subnets:** A network’s division is known as a subnet. Subnetting is the process of dividing a network into smaller subnets or subnetworks. We’ll now discuss public and private subnets.

**Public subnets:** They are frequently used when the resources need to be connected to the internet, such as when web servers are involved. The primary route table routes subnet traffic intended for the internet to the internet gateway. As a result, this kind of subnet is known as a public subnet
Private subnets are utilized, on the other hand, for resources that don’t require an internet connection.
Subnet size: Typically, private subnets have twice as many instances as public subnets.
**Route Table:**
AWS’s VPC offers total control over the traffic. You can achieve that by using route tables. A routing table is made up of rules that specify how and where traffic in a network will be directed. Each subnet in the Amazon Virtual Private Cloud has to have a routing table that governs the routing for that subnet. In a network, a routing table may be connected to various subnets.

## Advantages of AWS VPC
#### AWS VPC Advantages
**Security:** Security is the most important perk of VPC. Advanced security is offered by VPC in AWS at the instance and subnet levels. You can specify which users have access to cloud resources and which ones do not with VPC. Security is the most important perk of VPC. Advanced security is offered by VPC in AWS at the instance and subnet levels. You can specify which users have access to cloud resources and which ones do not with VPC.

**Easy to Set up and Use:** As with all of AWS’s services, AWS VPC is simple to set up. The AWS Management Console makes it simple to set up an Amazon VPC. The default VPC for your account is already set up, allowing you to concentrate on developing and delivering apps.

**Application Performance:** Application performance is largely affected by the congestion on the Internet. It can slow down the application traffic or even make the application slow.

## What is Amazon EC2?

Amazon Web Service EC2 (Amazon Elastic Compute Cloud), one of Amazon Web Services' most well-known services, offers businesses the ability to run applications on the public cloud. An EC2 instance is simply a virtual server in Amazon Web Services terminology. With an EC2 instance, AWS subscribers can request and provision a computer server within the AWS cloud.

##### The use and basics of AWS EC2
**Is EC2 a virtual machine?**
Developers can create virtual machine instances and easily configure models' capacity scaling using the EC2 web interface. An Amazon EC2 instance also allows users to build apps to automate scaling according to changing needs and peak periods. It makes deploying virtual servers and managing storage simple, requiring less hardware and helping streamline development processes

*How is EC2 billed?*
EC2 pricing depends on the hours and size of an instance, region, and operating system

**How do you set up AWS EC2?**
EC2 setup involves creating an Amazon Machine Image (AMI), which includes an operating system, apps, and configurations. That AMI is loaded to the Amazon Simple Storage Service (S3) and registered with EC2. Users can then launch virtual machines as needed. Amazon offers different instance types of EC2 for varying requirements and budgets in the AWS Marketplace, including hourly, reserved, and spot rates.

*How many EC2 instances can you have per region?*
AWS has a limit of 20 instances per region.

*How much does a stopped EC2 instance cost?*
Stopped EC2 instances do not incur any charges. However, you will be charged for Elastic IP addresses, EBS volume, or used S3 storage. You'll want to pause or delete these services to mitigate extra charges.

**Amazon EC2 features**
Several benefits and features draw developers to EC2 for cloud computing. Chief among these are:

Responsiveness to changing capacity requirements: The easy scaling of EC2 eliminates development obstacles when applications require more resources.

Flexibility in configurations: Users can choose memory size, CPU, and boot partition size optimized for their OS.

Integration: EC2 can integrate with other AWS services, such as RDS, SimpleDB, and SQS.

Precise control: Users get administrative access to their instances, can stop and start instances while retaining boot partition data, and can access console output for the instance.

Security: Users can control which instances remain private and have internet exposure. EC2 leverages Amazon Virtual Private Cloud (VPC) for security, and businesses can connect their secure IT infrastructure to resources in VPC.

Cost: Among several pricing options, EC2 offers affordable hourly rates.

**AWS EC2 benefits**
EC2 has several benefits. One of the main benefits of AWS EC2 is its elastic load balancing, which automatically distributes incoming application traffic across several instances while identifying unhealthy instances, and reroutes traffic to the healthy versions until restored.

**Additional benefits include:**
EC2 reduces the time to boot new servers , Scaling capacity based on changes to computing requirements ,Complete control of servers ,Flexibility with operating systems ,Built-in security
Why Instance Connect Endpoint?
The Amazon EC2 Instance Connect Endpoint is a service provided by AWS that revolutionizes SSH access to EC2 instances. Traditionally, managing SSH access to AWS EC2 servers required solutions like bastion hosts and public IPs to the instances. However, EC2 Instance Connect simplifies this process by leveraging AWS Identity and Access Management (IAM) policies to grant temporary, time-bound access to EC2 instances.

## Why Instance Connect Endpoint?
The Amazon EC2 Instance Connect Endpoint is a service provided by AWS that revolutionizes SSH access to EC2 instances. Traditionally, managing SSH access to AWS EC2 servers required solutions like bastion hosts and public IPs to the instances. However, EC2 Instance Connect simplifies this process by leveraging AWS Identity and Access Management (IAM) policies to grant temporary, time-bound access to EC2 instances.

Previously, even with EC2 Instance Connect, having a public IP was still necessary to connect to instances. However, AWS has recently introduced a groundbreaking feature called the Endpoint Service for Instance Connect. With this service, there is no longer a need for public IPs on your instances. Instead, you can securely connect to your instances directly through the AWS console or command line from your local machine.

EIC Endpoint provides a secure solution to connect to your instances via SSH or RDP in private subnets without Public IP Address, Internet Gateway, NAT Gateway, SSM agent, or bastion hosts. Another key difference is we can stay away from SSH keys, the "ec2-instance-connect ssh" command can generate ephemeral keys for you to connect to your instance. The long-lived keys are always a big security burden on enterprise customers and with EIC Endpoint such long lived keys are no longer needed and making the whole solution more secure
Provision an EC2 Instance Connect Endpoint (EIC Endpoint) in a private subnet and it allows you to connect to any instances in any subnet in the VPC as long you have communication allowed across subnets.

**Key Features and Benefits**
Connect to EC2 instance without public IP. Internet Gateway is not required for your VPC. Access control is a combination of Security Group and Identity and Access Management. Log all connections in CloudTrail.

**How It Works**
The EIC (EC2 Instance Connect) Endpoint is a TCP proxy incorporating identity awareness. It operates in two modes.

In the first mode, the AWS CLI client is utilized to create a secure WebSocket tunnel from your workstation to the EIC Endpoint using your AWS Identity and Access Management (IAM) credentials. Once the tunnel is established, you can direct your preferred client to your loopback address (127.0.0.1 or localhost) and connect to the desired resources as usual.

In the second mode, when the AWS CLI is not used, the AWS Management Console provides a secure and seamless access experience to resources within your Virtual Private Cloud (VPC). Authentication and authorization processes are evaluated before the traffic reaching the VPC.

### Architecture Diagram
![cloud sky](https://github.com/ClementDaniel/Cloud-Force-Sky/assets/96403532/609698f8-d41f-4bdc-82fe-80895b726ec7)



## **ALTSCHOOL AFRICA**

## **Holiday Project**

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">Project Overview</a>
      <ul>
       <li><a href="#prerequisites">What is Load Balancing</a></li>
        <li><a href="#prerequisites">Application Load Balancer overview</a></li>
        <li><a href="#built-with">Virtual Private Cloud</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#steps">Creating VPC</a></li>
        <li><a href="#steps">Create a Private EC2 Instance</a></li>
        <li><a href="#steps"> Create a Bastion Host</a></li>
        <li><a href="#steps">Installation and Configuration of Nginx Server on Private EC2 Instances</a></li>
        <li><a href="#steps">Creating Target Group</a></li>
        <li><a href="#steps">Creating Application Load Balancer</a></li>
        <li><a href="#steps">Creating Application Load Balancer</a></li>
      </ul>
    </li>
    <li><a href="#contact">Contacts</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

## **Project Overview**

## What is Load Balancing?

This is a way of distributing incoming traffic efficiently across multiple servers.

## Application Load Balancer overview

Application Load Balancer Routes incoming Client HTTP/HTTPS traffic across multiple servers

## Virtual Private Cloud (VPC)

A VPC is an Isolated Private Cloud within a Public Cloud.

## TASK

## You are required to perform the following tasks

- Set up 2 EC2 instances on AWS(use the free tier instances).

- Deploy an Nginx web server on these instances(you are free to use Ansible)

- Set up an ALB(Application Load balancer) to route requests to your EC2 instances

- Make sure that each server displays its own Hostname or IP address. You can use any programming language of your choice to display this.

- Work on building a personal portfolio and CV (Check out resumeworded.com).

## Important points to note

- I should not be able to access your web servers through their respective IP addresses. Access must be only via the load balancer

- You should define a logical network on the cloud for your servers.

- Your EC2 instances must be launched in a private network.

- Your Instances should not be assigned public IP addresses.

- You may or may not set up auto scaling(I advice you do for knowledge sake)

- You must submit a custom domain name(from a domain provider e.g. Route53) or the ALB’ domain name.

## **Getting Started**

## **Step One:**

## **1. Creating VPC**

Open the Amazon VPC console at https://console.aws.amazon.com/vpc/

On the VPC Dashboard, choose Launch VPC Wizard.

![s1](/images/vpc1.png)

On the VPC configuration Dashboard choosing VPC and more automatically launches Private Subnets, Public Subnets, Routing Tables and Subnet Associations, Internet GateWay, Elastic IP, IP CIDR block, Availability Zones and Network Access Translator.

On the Auto-generate input field, write the name of your VPC

![s1](/images/vpc2.png)

Choose the number of Avalaibility Zones (AZ's) in which to create your NAT GateWay.

![s1](/images/vpc4.png)

The image below shows the auto-generated configurations i.e. Subnets, Routes Tables and Network Connections.

![s1](/images/vpc3.png)

## **2. Create a Private EC2 Instance**

Navigate to the ec2 console and click on Launch Instance

![s1](/images/e1.png)

Write the name of your instances, select the number of instances and your choice of Amazon Machine Image.

![s1](/images/e2.png)

Select your key-pair if you dont have a key-pair create one

Next, select the VPC that you previously created, and choose any of the private subnet, Disable the Auto-Assigned Public IP,  and finally Create a Security Group keeping the default settings then click on Launch Instance.

![s1](/images/e3.png)

## **Create a Bastion Host**

A bastion host is a server whose purpose is to provide access to a private network from an external network. This is necessary because our subnets are private, hence, the bastion host which is within the same VPC serves as a bridge to establibish connection to the private subnets. The best practice is that anyone who needs access to any of the computers inside the VPC must SSH into the bastion host first before doing another SSH to the instance they want to go to.

Navigate to the ec2 console and click on Launch Instance

Write the name of your instance, and your choice of Amazon Machine Image.

![s1](/images/bastion1.png)

Select your key-pair

![s1](/images/bastion2.png)

Next, select the VPC that you previously created, and choose any of the public subnet, Enable the Auto-Assigned Public IP, and finally choose a Security Group keeping the default settings then click on Launch Instance.





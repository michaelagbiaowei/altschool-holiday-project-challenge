## **ALTSCHOOL AFRICA**

## **Holiday Project**

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">Project Overview</a>
      <ul>
        <li><a href="#prerequisites">Application Load Balancer overview</a></li>
        <li><a href="#built-with">AWS ALB Basics</a></li>
        <li><a href="#built-with">VPC</a></li>
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

## What is an Application Load Balancer?

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

## Important points to not

- I should not be able to access your web servers through their respective IP addresses. Access must be only via the load balancer

- You should define a logical network on the cloud for your servers.

- Your EC2 instances must be launched in a private network.

- Your Instances should not be assigned public IP addresses.

- You may or may not set up auto scaling(I advice you do for knowledge sake)

- You must submit a custom domain name(from a domain provider e.g. Route53) or the ALB’ domain name.

## **Getting Started**

## **Step One:**

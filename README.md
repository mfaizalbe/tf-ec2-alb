# AWS WAF Hands-On Activity

This repository contains an activity introducing **AWS Web Application Firewall (WAF)**.  
The activity demonstrates how WAF rules can be applied to protect an application that is publicly accessible through an **Application Load Balancer (ALB)**.

## Prerequisites

- An existing **VPC**  
- An existing deployment accessible through a **public Application Load Balancer**

## Setup

1. **Fork the repository**  
   Fork [this repository](https://github.com/slim-sandbox/tf-ec2-alb) into a personal GitHub account.

2. **Clone the forked repository**  
   ```bash
   git clone https://github.com/<github-username>/tf-ec2-alb.git
   cd tf-ec2-alb
   ```

3. Configure Terraform variables
Set the following variables in the Terraform code:
- region
- vpc
- name_prefix

4. Deploy with Terraform
  ```bash
terraform init
terraform plan -var="name_prefix=your-name" -var="vpc_name=your-vpc-name"
terraform apply -var="name_prefix=your-name" -var="vpc_name=your-vpc-name"
```

## Learning Objectives
- Understand the purpose and functionality of AWS WAF
- Apply WAF rules to enhance application security
- Observe integration of WAF with an Application Load Balancer

## Activity Document
The full activity instructions are available [here](https://docs.google.com/document/d/1Puun7zXswj03qAXO4gtRhsg-M1EClf9l/edit)

---

## References
[AWS WAF Documentation](https://docs.aws.amazon.com/waf/latest/developerguide/what-is-aws-waf.html)
[Terraform AWS Provider](https://registry.terraform.io/providers/hashicorp/aws/latest/docs)
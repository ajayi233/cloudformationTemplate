# Auto Scaling Lab - CloudFormation Template

This CloudFormation template sets up an Auto Scaling Group (ASG) with a single instance that is accessible via an Application Load Balancer (ALB). The ASG is configured to scale out if the CPU utilization exceeds 50% for 1 consecutive period of 30 seconds.

## Prerequisites

* An AWS account
* A VPC with at least 2 subnets
* An IAM role for EC2 instances to access CloudWatch

## How to Use

1. Create an S3 bucket to store the CloudFormation template and the supporting files.
2. Upload the files in this repository to the S3 bucket.
3. Create a new CloudFormation stack using the template in the S3 bucket.
4. Fill in the required parameters, such as the VPC ID, subnets, and IAM role.
5. Click "Create Stack" to create the stack.

## What's Included

* An Auto Scaling Group (ASG) with a single instance
* An Application Load Balancer (ALB) with a single target group
* A security group for the ALB
* A security group for the EC2 instance
* A NAT gateway for the private subnet
* A private subnet for the EC2 instance
* A public subnet for the ALB
* An IAM role for EC2 instances to access CloudWatch
* A CloudWatch alarm to trigger scale out if CPU utilization exceeds 50%

## How it Works

1. The ASG is created with a single instance.
2. The ALB is created with a single target group.
3. The security group for the ALB is created.
4. The security group for the EC2 instance is created.
5. The NAT gateway is created for the private subnet.
6. The private subnet is created for the EC2 instance.
7. The public subnet is created for the ALB.
8. The IAM role for EC2 instances is created.
9. The CloudWatch alarm is created to trigger scale out if CPU utilization exceeds 50%.
10. The CPU utilization of the EC2 instance is monitored by CloudWatch.
11. If the CPU utilization exceeds 50% for 1 consecutive period of 30 seconds, the CloudWatch alarm is triggered.
12. The ASG is scaled out by 1 instance.
13. The new instance is added to the target group of the ALB.

## Troubleshooting

* Check the CloudFormation stack events for any errors.
* Check the CloudWatch logs for any errors.
* Check the security group rules to ensure that traffic is allowed to flow between the ALB and the EC2 instance.

## Cleaning Up

* Delete the CloudFormation stack.
* Delete the S3 bucket and the supporting files.

## License

This CloudFormation template is licensed under the MIT License. See the LICENSE file for details.
# cloudformationTemplate

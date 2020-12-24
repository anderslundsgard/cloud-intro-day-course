# Cloud Intro Day Course

Material and descriptions used in the *Cloud Intro Day Course*.

## Manual DEMO

1. Log in with EC2 Admin access to AWS course account.
1. Launch a Linux 2 EC2 machine with default settings except
    1. Security group port 80 for 0.0.0.0/0
    1. IAM Role: ... (to be able to run session manager)
    1. User data below to install Apache web server
    1. Proceed without key pair.
  
```
#!/bin/bash
yum update -y
yum install -y httpd.x86_64
systemctl start httpd.service
systemctl enable httpd.service
echo “Hello World from $(hostname -f)” > /var/www/html/index.html
```

## IaC DEMO

1. ...

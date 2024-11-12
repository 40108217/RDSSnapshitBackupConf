# RDSSnapshitBackupConf
Lambda Function to confirm the daily backup status for RDS Automatic Backup (Snapshot)
#Infra Details
1) RDS Created in Private Subnet
2) Lambda Deployed in same VPC
3) RDS endpoint created in same vpc
4) SNS Topic created to send the alert on e-mail
5) SNS endpoint created in same VPC

# Deployment
Complete infra is created in the private subnet. For Lambda to work with RDS in private subnet, need to create the RDS endpoint in same VPC.
SNS endpoint also created in same VPC so that Lambda can access it for sending the e-mail via SNS.
Role mapped to Lambda, should have additional RDS and SNS access.

# Test
It will validate if backup is done and snapshot is created for previous day.

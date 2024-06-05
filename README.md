# Working with AWS CloudTrail

## Activity Overview

In this activity, I created an AWS CloudTrail trail to audit actions taken in the AWS account. I then investigated to determine who modified the Café website. The activity involved several tasks to configure, analyze, and secure the AWS environment.

The architectural diagram illustrates the setup used in this activity.

![architecture](https://github.com/Mohamed-kittany/Canvas-Lab-187-CloudTrail/assets/161580792/96895b45-44de-4a07-85c8-26fe34f02563)

## Activity Objectives

After completing this activity, I was able to:

- Configure a CloudTrail trail.
- Analyze CloudTrail logs by using various methods to discover relevant information.
- Import CloudTrail log data into Athena.
- Run queries in Athena to filter CloudTrail log entries.
- Resolve security concerns within the AWS account and on an EC2 Linux instance.

## Tasks Completed

### Task 1: Modifying a Security Group and Observing the Website

1. Modified the security group settings to add an inbound rule for SSH access.
2. Observed the Café website to ensure it looked normal before proceeding with further tasks.

### Task 2: Creating a CloudTrail Log and Observing the Hacked Website

1. Created a CloudTrail trail named `monitor` to capture log data.
2. Noticed the website was hacked soon after creating the trail and observed changes in the security group settings.

### Task 3: Analyzing the CloudTrail Logs Using Grep and AWS CLI

1. Connected to the Café Web Server EC2 instance using SSH.
2. Downloaded and extracted CloudTrail logs from the S3 bucket.
3. Used the `grep` utility to analyze the logs and identify suspicious activities.
4. Used AWS CLI commands to further filter and analyze CloudTrail logs to pinpoint the source of the security breach.

### Task 4: Analyzing the CloudTrail Logs Using Athena

1. Created an Athena table to analyze CloudTrail logs using SQL queries.
2. Ran queries in Athena to filter log entries and identify the hacker responsible for modifying the security group.

### Task 5: Analyzing the Hack Further and Improving Security

1. Checked OS users on the EC2 instance and removed unauthorized users.
2. Updated SSH settings to enhance security and prevent unauthorized access.
3. Fixed the website by restoring the original graphic files.
4. Deleted the unauthorized AWS IAM user to secure the AWS account.

## Conclusion

This activity provided hands-on experience in setting up and using AWS CloudTrail for auditing and investigating security incidents. By analyzing CloudTrail logs using various tools and securing the AWS environment, I was able to identify the hacker and prevent future incidents.

To launch the EC2 instance and mount an EFS file system

Open the Amazon EC2 console at https://console.aws.amazon.com/ec2/.

Choose Launch Instance.

In Step 1: Choose an Amazon Machine Image (AMI), find an Amazon Linux AMI at the top of the list and choose Select.

In Step 2: Choose an Instance Type, choose Next: Configure Instance Details.

In Step 3: Configure Instance Details, provide the following information:

Leave Number of instances at one.

Leave Purchasing option at the default setting.

For Network, choose the entry for the same VPC that you noted when you created your EFS file system in Step 1: Create Your Amazon EFS File System.

For Subnet, choose a default subnet in any Availability Zone.

For File systems, make sure that the EFS file system that you created in Step 1: Create Your Amazon EFS File System is selected. The path shown next to the file system ID is the mount point that the EC2 instance will use, which you can change.

The User data automatically includes the commands for mounting your Amazon EFS file system.

Choose Next: Add Storage.

Choose Next: Add Tags.

Name your instance and choose Next: Configure Security Group.

In Step 6: Configure Security Group, set Assign a security group to Select an existing security group. Choose the default security group to make sure that it can access your EFS file system.

You can't access your EC2 instance by Secure Shell (SSH) using this security group. SSH access isn't required for this exercise. To add access by SSH later, you can edit the default security and add a rule to allow SSH. Or you can create a new security group that allows SSH. You can use the following settings to add SSH access:

Type: SSH

Protocol: TCP

Port Range: 22

Source: Anywhere 0.0.0.0/0

Choose Review and Launch.

Choose Launch.

Select the check box for the key pair that you created, and then choose Launch Instances

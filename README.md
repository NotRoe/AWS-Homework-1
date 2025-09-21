# AWS-Homework-1
AWS

Sign in to the AWS Console
Select your region
Go to the Dashboard and select EC2
Create Security Group

Select the security group on the left side
Click "Create Security Group"
Enter name and description (Usually they are the same)
Verify VPC is set to the default
Add inbound HTTP TCP 80 IPv4 anywhere (0.0.0.0/0)
Add inbound SSH TCH 22 ipvd anywhere (0.0.0.0/0)
DO NOT TOUCH OUTBOUND RULES - Verify it says "All traffic" is allowed
(Optional: Add tags)
CLICK "CREATE SECURITY GROUP"
VERIFY YOUR SECURITY GROUP IS CREATED AND CORRECTLY CONFIGURED IN THE CONSULE

GRAB YOUR STARTUP SCRIP

Choose from the available start-up scripts in the class (anyone's will work)
Copy the script from GitHub
LAUNCHING EC2 INSTANCE

In the left column, click on instance
Click "Launch Instance"
CREATING INSTANCE

Enter the instance name and add relevant tags if desired
AMI Selection: Review menu, ensure defaults are selected, collapse
Instance Type: Review the instance type menu, select the proper sizing, and  collapse
Key Pair: select "Proceed without key pair", Collapse (IN MOST CASES YOU WILL NEED TO GENERATE A NEW KEY PAIR)
NETWORK SETTING

Don't click "Edit"
Verify VPC selection
Note: Subnet selection is not critical for this lab
Make sure "Autho-assign public IP" is enabled
Select your created Security Group (NOT "launch-wizard")
Collapse Section
STORAGE CONFIGURATION

Review storage menu
Collapse section
ADVANCED SETTINGS

Open advanced settings
Focus on the User Data section only - ignore everything else
Paste your chosen startup script
LAUNCH

Review configuration
Click "Launch Instance"
TEST THE WEB SERVER

Wait for the instance to pass status checks
Copy the instances PUBLIC DNS ADDRESS
Open a browser
Use: TYPE http:// Then paste the Public DNS Address behind it
TEARDOWN TERMINATE THE EC2 INSTANCE

Go to the EC2 Instance
Select your instance
Click the drop-down and click TERMINATE INSTANCE
DELETE THE SECURITY GROUP (Optional)

Go to EC2 --- Security Groups
Select your security group you want to delete
Actions -- Delete Security Group Note: The security group can only be deleted after the instance is terminated

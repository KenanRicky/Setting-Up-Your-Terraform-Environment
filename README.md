# Setting Up Your Terraform Environment

# Set Up Your AWS Account
# Step 1 — Create an AWS Account

Go to Amazon Web Services

Click Create an AWS Account

Enter:

Email

Password

Account name

Add:

Phone number

Payment details (card required, even for free tier)

Verify your phone (OTP)

Choose:

Basic Support Plan (Free)

# Step 2 — Secure Your Root Account (VERY IMPORTANT)

After login:

Go to IAM Dashboard

Enable:

✅ MFA (Multi-Factor Authentication)

✅ Use Google Authenticator or similar

👉 Never use root account for daily work.

# Step 3 — Create IAM User for Terraform

Go to IAM → Users

Click Create user

Enter:

Username: terraform-user

Select:

✅ Programmatic access

# Step 4 — Assign Permissions

For learning:

Choose:

AdministratorAccess

👉 Later in real jobs, use least privilege policies.

# Step 5 — Create Access Keys

After creating user:

Go to Security Credentials

Click Create Access Key

Choose:

CLI / Local development

👉 Save:

Access Key ID

Secret Access Key

## Install and Configure the AWS CLI
Download the AWS CLI by running the bellow code:
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"

Then unzip the installer using the code:
unzip awscliv2.zip

then install the CLI using the code:
sudo ./aws/install

To verify you can use the command:
aws --version
<img width="1025" height="583" alt="Screenshot from 2026-03-17 23-02-45" src="https://github.com/user-attachments/assets/f26fe02c-b291-4ffb-a712-e4dfc1e2faab" />

# Install Terraform and Connect Terraform to AWS
Download the terraform from Hashicorp releases using the below code:
wget https://releases.hashicorp.com/terraform/1.7.5/terraform_1.7.5_linux_amd64.zip

Then Unzip it 
unzip terraform_1.7.5_linux_amd64.zip

Then install it terraform by moving it to the system path
sudo mv terraform /usr/local/bin/

Use terraform -v to confirm installation.
<img width="1025" height="583" alt="Screenshot from 2026-03-17 23-13-15" src="https://github.com/user-attachments/assets/0f295822-4a5e-44d2-90ef-7dde2fa417d0" />

To connect to Terraform to AWS, run the code:
aws configure
The paste the Access Key then
Paste the SEcret Key
Identify the Region
Then identify the output as json.

Corfirm the aws caller identity
aws sts get-caller-identity
<img width="1141" height="188" alt="Screenshot from 2026-03-17 23-20-42" src="https://github.com/user-attachments/assets/45452c83-6c72-4380-a851-e7d0983b8afb" />

Confirmation of Configure List
<img width="1141" height="188" alt="Screenshot from 2026-03-17 23-24-00" src="https://github.com/user-attachments/assets/28291904-910a-488a-bc9d-9eecb28b13d2" />


# Configuring an AWS-CLI
###### The AWS CLI is a special tool to manage your AWS services from a terminal session on your own. With just one tool to download and configure, you can control multiple AWS services from the command line and automate them through scripts. 


> First of all, we need to download and install the AWS CLI. Depending on your operating system, it will require a different method. Click [here](https://aws.amazon.com/cli/) to download and install the one which matches your operating system. The link includes the installation steps described in detail. 
 Here I am using an Amazon Linux AMI, which comes with AWS-CLI pre-installed on it.

###### Now, let us have a look into the process of configuring an AWS-CLI. 

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)


## STEPS:

After the installation of AWS CLI, we need to configure the application to be able to connect to our AWS account.  To do so, enter the following from your command prompt:
```sh
aws configure
```
Now, you will be prompted to enter the few details:

```sh
root@AG:~# aws configure
AWS Access Key ID [****************OUT6]: **************
AWS Secret Access Key [****************5LiP]: ******************
Default region name [ap-south-1]: ap-south-1 
Default output format [json]: json
```
- The default region name simply defines the Region where you requests will be sent to. Here I'm working on the 'ap-south-1' region.
- The default output format specifies how the results are formatted. Values that can be used here include: json,text and table.
- aws_access_key_id - The AWS access key part of your credentials
- aws_secret_access_key - The AWS secret access key part of your credentials
> The AWS access key ID and AWS secret access key are used to authenticate your AWS account. This authorizes you to carry out specific tasks and functions as defined by your permissions level.  The AWS access key ID is made up of 20 random uppercase alphanumeric characters and the AWS secret access key is made up of 40 random upper and lowercase alphanumeric and non-alphanumeric characters.These access keys can be created for any IAM user who requires authentication from a programmatic perspective, such as when using the AWS CLI.

##### Note:
You can generate new credentials within AWS Identity and Access Management (IAM) if you do not already have them.When the access keys are created, you are prompted to download and save the details. The secret access key ID will only be displayed once, and if you lose it, then you’ll have to delete the associated access key ID and recreate new keys for the user. 
Also, it’s not possible to retrieve lost secret access key IDs as AWS does not retain copies of these for security reasons in case they were compromised.
The values you provide for the AWS Access Key ID and the AWS Secret Access Key will be written to the shared credentials file (~/.aws/credentials).

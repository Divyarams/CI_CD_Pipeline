# CI_CD_Pipeline

The post contains automatic Integration and Deployment of a Webpage using EC2, CodeCommit and CodeDeploy. Demo uses a linux machine with static content and auto deployed using CodePipeline.

# Step 1

Create a repo in CodeCommit and clone the repo in your local machine. Add index.html and image files needed for the webpage.

# Step 2

Create an EC2 Linux instance with user-data to install CodeDeploy agent in the machine. Provide IAM role for the agent to interact with CodeDeploy. Security group should have an Inbound rule to accept SSH from Port 22 and HTTP from Port 80.

# Step 3

Configure CodeDeploy Application with targets as EC2 , Codecommit repo to refer. Choose Deployment Configuration, Agent auto updates and Auto Scaling group settings.
An appspec.yml file with steps necessary for deployment should be available in the source repo.

# Step 4

Configure a Pipeline to automate Commit and Deploy. The pipe runs everytime a new change is committed to the repo.

The details of the log files to track for error-tracking is available in checkfile.txt

# Contoso corporation is planning to lauch "Meow App" to expand their pet food business through digital transformation.
# As discussed in the meeting, contoso's CTO wants to leverage their application in the cloud and using automation practice to offload the burdens of operation matters over time.
# HelloCloud awarded the tender for this project and proposed to leverage terraform cloud and AWS for the infrastructure automation.
 
 ## procedure
 1. Create Github repo: (test,dev,prod)
 2. Terraform Cloud : Create Organization (test,dev,prod)
    2.1 Create testing workspace
    
 3. Gitgub and terraform Intergration
    3.1 Connect to VCS (TFC)
    3.2 Setup Provier (TFC)
    3.3 Setting > Develper Setting > Register a new OAuth Application
    3.4 Copy Information from VCS and paste to TFC (vice versa) , Generate Secret Key from Github
    
 4. For Terraform and AWS api integration
    4.1 Create IAM role and attach to administration policies (AWS management console)
    4.2 Create AWS-Access Key for contoso-testing-management and download the access key (csv.file)
    4.3 Create workspace (TFC)
        Version Control Workflow > Choose Organization > Choose the correct Repo > Advanced options (choose Auto apply)
    4.6 Configure environment variable for AWS access key and secret access key (TFC)
        AWS_ACCESS_KEY_ID : xxxxxxxx  (select case sensitive)
        AWS_SECRET_ACCESS_KEY : xxxxxxx
    4.7 Configure terraform VS code

    ### github testing

    ### Enter file in which to save the key (/home/vagrant/.ssh/id_rsa): github.com.contoso-test

    eval "$(ssh-agent -s)"
    ssh-add ~/.ssh/github.com.contoso-test
    ssh -T git@github.com

    git clone git@github.com:hellocloudiomtw/contoso-test.git contoso-test
    cd contoso-test
    git remote -v
    git status
    git log
    git commit -am "updated README file"
    git push
   



    
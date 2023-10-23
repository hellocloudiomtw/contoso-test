###  
 

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
        AWS_ACCESS_KEY_ID : xxxxxxxx
        AWS_SECRET_ACCESS_KEY : xxxxxxx
    4.7 

    ### github testing

    git clone git@github.com:hellocloudiomtw/contoso-test.git contoso-test
    cd hashicat-aws-bca-github-testing
    git remote rm origin
    gh repo create hashicat-aws-bca-hellocloudiomtw --private --source=. --remote=upstream --push

    eval "$(ssh-agent -s)"
    ssh-add ~/.ssh/github.com.contoso-test
    ssh -T git@github.com


Enter file in which to save the key (/home/vagrant/.ssh/id_rsa): github.com.contoso-test
    

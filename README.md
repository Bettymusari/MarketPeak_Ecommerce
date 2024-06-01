# MarketPeak_Ecommerce
I created a project directory named "MarketPeak_Ecommerce and in this directory, i initialize a git repository in it with the following commands: 
mkdir MarketPeak_Ecommerce
cd MarketPeak_Ecommerce
git init

To download a website template, i visited "Tooplate" and downloaded the specitic template (2130_waso_strategy).
I then extracted the template into my project directory "MarketPeak_Ecommerce" to prepare the website template.


Using "git add .", I added the website files to my git repository.
Then I configured both my user name and user email with the next 2 commands:
git config --global user.name "Bettymusari"
git config --global user.email "opsbabs1@gmail.com"
I commit the changes with this command: git commit -m "Initial commit with basic e-commerce site structure"

For version control and collaboration, I must push the code to a remote repository on the Github with the following step:
1. I logged into my github accounct and created a new empty repository named "MarketPeak_Ecommerce
2. I linked my local repository to Github by running this command: git remote add origin https://github.com/Bettymusari/MarketPeak_Ecommerce.git
I then tried to push my commits to Github with "git push -u origin main" . It didn't work, so i went back to Github and used the process commands outlined:
echo "# MarketPeak_Ecommerce" >> README.md
 git init
 git add README.md
 git commit -m "first commit"
 git branch -M main
 git add .
 git push -u origin main : 
 
 This was successful wit the following result:
 
"Enumerating objects: 42, done.
Counting objects: 100% (42/42), done.
Delta compression using up to 4 threads
Compressing objects: 100% (40/40), done.
Writing objects: 100% (42/42), 1.85 MiB | 41.00 KiB/s, done.
Total 42 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/Bettymusari/MarketPeak_Ecommerce.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'."

AWS Deployment:
On my AWS Management Console, I launched an instance named "MarketPeak_Ecommerce" on an AWS Linux AMI
I connected to the instance using SSH
I then cloned the Github repository to my AWS EC2 instance with the following steps:
On my EC2 instance, i generated an SSH key using "ssh-keygen"
Then I displaye and copied my public key with this command: "cat /home/ubuntu/.ssh/id_rsa.pub"
I then added my SSH public key to my Github account.
I used the SSH clone URL to clone the repository:
 "git clone git@github.com:yourusername/MarketPeak_Ecommerce.git"

I installed Apache web server on my EC2 instance with:
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd

I then configured the httpd for the website using: 
sudo rm -rf /var/www/html/*
sudo cp -r ~/MarketPeak_Ecommerce/* /var/www/html/
To apply the changes, I reloaded the server with: "sudo systemctl reload httpd"

With this, my Marketpeak-Ecormmerce Platform is live and can be accessed via:
 http://3.133.15.134/2130_waso_strategy/ 

For Continous Deployment and Integration Workflow, I created a new branch named "development" and navigated to it with the following commands: 
"git branch development"
"git checkout development"

In the index.html I made a change to the title. I changed the title from "waso strategy" to "MarketPeak_Ecomerce"

Using "git add ." I staged the changes

I then commit the stage with: "git commit -m "Add new features or fix bugs"
Then pushed the changes to Github : 'git push origin development"

I then created a Pull Request on Github, reviewed and then merged the changes using the following command:
git checkout main
git merge development





























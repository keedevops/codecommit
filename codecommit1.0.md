
# CodeCommit And SNS Notifications for Commit, Push And Pull Requests 

Step 1: Create a repository in the code commit 
![Screenshot Capture - 2024-01-21 - 23-29-15](https://github.com/keedevops/codecommit/assets/155215036/96fc1cff-e065-4b79-9374-28796ac1261c)

Step 2: Copy the HTTPS clone URL to clone your repo and copy the files
![Screenshot Capture - 2024-01-21 - 23-28-33](https://github.com/keedevops/codecommit/assets/155215036/ac4d145d-fcb4-4e53-8582-e6bda2b7714b)
Step 2: Start the ec2 instance with ubuntu AMI and follow the updating steps for git

```
sudo apt update 
sudo apt git install -y
git
git --version
git init
git clone https://git-codecommit.ap-south-1.amazonaws.com/v1/repos/Demo_code_commit (HTTPS clone)

```

```
cd Demo_code_commit/
mkdir repository
nano test1
git add test1
git status
git commit -m "test1 file added"
git push origin master

```
Step 3: When ever you try to push it always asks for your IAM credentials.Make sure you have a IAM user with the SNS and Code Commit Access
![Screenshot Capture - 2024-01-21 - 23-48-11](https://github.com/keedevops/codecommit/assets/155215036/c2c0a703-6c91-4385-a54e-f0b0628d4599)
![Screenshot Capture - 2024-01-21 - 23-47-52](https://github.com/keedevops/codecommit/assets/155215036/84c16f75-0b51-436f-82ac-44e858dab7cf)

Step 4: Make sure you add, commit and push whatever you do 
Now a file is created in your repo
![Screenshot Capture - 2024-01-22 - 01-22-27](https://github.com/keedevops/codecommit/assets/155215036/8a3d4e5f-3e6b-40a7-a024-5fd8cdb9c907)
```
git pull

```
This command pulls the updated files youve made in the codecommit 

Lets create a new branch 
```
git branch newrepo master
git checkout newrepo
git push origin master newrepo

nano demo
git add .
git commit -m "demo file added to branch"
git push origin master
git status
git merge newrepo

```
Now the changes are merged with the main branch 
Creating a file in repo adding, commiting, pushing, branching in codecommit






Project Introduction to Cloud Computing
Objective: The objective of the project is to utilize concept of version control, develop a platform in a Linux environment and deploy it on an AWS EC2 instance.
-I started by creating a folder using the command (mkdir MarketPeak-Ecommerce)
-I changed directory using (cd MarketPeak-Ecommerce).
-I then initialized git with (git init)
-I now proceeded to Tooplate.com to get, prepare and extract a web template .
-Went ahead to create a new repository on my github account named Markepeak-Ecommerce
-I then now staged and commited the template by using the blow commands.
*git add .
*git commit -m "Initial commit with basic e-commerce site structure"
* git remote add origin https://github.com/Victoronalo/MarketPeak-Ecommerce.git
* git push -u origin main

-I proceeded to log int my AWS console to create a new EC2 Instance(ID: i-00d567fb9d064aa34)
-The EC2 was launched using an Amazon Linux AMI
-it was connected to the instance by using SSH and it was successful.
-After these processes, I went ahead to clone the repository on Linux server using https (git clone https://github.com/Victoronalo/MarketPeak-Ecommerce.git).
-Then I installed Apache using the below commands.
*sudo apt update
*sudo apt install apache2
*sudo systemctl status apache2
-I then proceeded to configure website using the below commands
*sudo rm -rf /var/www/html/*
*sudo cp -r ~/MarketPeak-Ecommerce/* /var/www/html/
-The website was tested by launching the public IP of the EC2 instance and it worked.
-I then proceeded to create another branch “development” by using below commands
*git branch development
*git checkout development
-I added a new folder called documentation
-In going with version control on Gits I did the “git add .” and then use the “git commit” before the “git pus” command.
-Knowing that there is more than one branch I had to do a pull request from the github page and created a successful merge on github.
I reviewed the pull request and made sure everything was good and then proceeded to merge the pull request into the main branch incorporating the new feature by using the below commands.
*git checkout main
*git merge development
-I now pushed my merged changes to Github and I made sure my local main branch containing the changes is pushed to the remote repository on github.
-In deploying changes to the production server, I SSH into the EC2 instance and did a pull with this command(git pull origin main) and then restarted using(sudo systemctl reload apache2).
-Lastly I tested the webserver from the EC2 public IP address.
`# MarketPeak-Ecommerce

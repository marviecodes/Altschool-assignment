# Altschool-assignment
STEPS ON HOW I PROVISIONED THE SERVER, INSTALLED THE WEB SERVER (NGINX), DEPLOYED THE HTML PAGE, AND CONFIGURED NETWORKING.


I first created the Server via AWS EC2 Instance, i then logged into it.
I installed nginx and verified it using systemctl.
I created the html page.
I moved the html page from my local machine to my server using the scp command.
i.e scp -i [path-to-your-key.pem] [path-to-index.html file] (Linux distro)ec2-user@<your-ec2-public-ip>:/tmp/
This moves the file to your server on this file path: /tmp/index.html.
This is a temporary location so i will move it to nginx's default web root directory - /var/www/html/
i.e sudo mv /tmp/index.html /var/www/html/index.html
I then set the needed permissions
i.e sudo chmod 644 /var/www/html/index.html
Then i restarted the nginx service.
And accessed it on my web server.

MY PUBLIC IP ADDRESS / WEB PAGE URL
http://3.254.229.209/

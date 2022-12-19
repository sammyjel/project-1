## Awesome documentation of my first project

`I run command sudo apt update to update my serverand the image below displays the output generated`

![apache the status update](./images/apache%20status%20update.png)

`I run command sudo apt install apache2 to install appache server`

![apache install](./images/sudo%20apache%20install.png) 

I run command sudo systemctl status apache2 to check the status of the server

![ apacche systemctl status](./images/sudo%20systemctl%20status%20.png)

I run curl http://localhost:80 to access apache server locally and the output below generated

![ localhost apache server](./images/curl%20localhost1.png)
![localhost apache server](./images/curl%20localhost2.png)

I entered http://3.17.158.215:80 into my browser's address bar and hit enter to access the apache http server, which produced the output shown in the following image.

![ apache http server](./images/apache2%20default%20page.png)

I used the command "sudo apt install mysql-server" to install MySQL, and the results are shown below:

![sudo apt instal mysql server](./images/sudo%20mysql%20install.png)
![sudo apt install mysql server](./images/sudo%20mysql%20installation.png)

## Mysql secure installation

The output of an interactive script I ran with the command "sudo mysql secure installation" to set security is displayed in the photos below:

![sudo mysql secure install](./images/mysql%20secure%20install1.png)
![sudo mysql secure install](./images/mysql%20secure%20install2.png)

After adjusting the security settings, I used the command "sudo mysql -p" to test mysql to see if it would let me log in. The output is seen in the image below:

![sudo mysql password](./images/mysql%20pswd%20test.png)

## INSTALLING PHP

## installing php-mysql, a PHP module

With the command "sudo apt install php libapache2-mod-php php-mysql," the three packages were installed, and the output seen in the following image was produced.

![sudo apt install php](./images/sudo%20apt%20install%20php.png)

I used the "php -v" command to check the installed version, and the results are displayed in the image below.

![sudo php version](./images/php%20version.png)

## CREATING A VIRTUAL HOST FOR MY WEBSITE USING APACHE.

*making a directory for my samylampproject website*

I run the command "sudo mkdir /var/www/samylampproject" to create the directory for my samylampproject.

I then assign ownership to the directory by running the command "sudo chown -R $USER:$USER /var/www/samylampproject."

I then create and open a new configuration file in Apache's sites-available directory using the command "sudo vi /etc/apache2/sites-available/samylampproject.conf."

To create a new blank file, I added the following code to the output of the preceding command.

<VirtualHost *:80>

    ServerName samylampproject
     ServerAlias www.samylampproject
     ServerAdmin webmaster@localhost
    DocumentRoot /var/www/samylampproject
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>

![virtual file output](./images/vitual%20file%20otuput.png)

To view the new file in the sites-available, I then run the command "sudo ls /etc/sites-available," and the output is displayed in the below-image:

![sites available](./images/site%20available%20directory.png)

I run the command "sudo a2ensite samylampproject" to enable the new virtual host, and I received the output shown below:

![ sudo a2ensite enable](./images/sudo%20a2ensite.png)

I use the command sudo a2dissite 000-default to disable the default website.
![sudo a2dissite default](./images/sudo%20a2dissite.png)

I run "sudo apache2ctl configtest" to make sure my setup didn't have any syntax errors, and the output indicated that everything was in order.

![sudo configtest](./images/syntax%20check%20up%20.png)

I run Sudo Echo LAMP to create index.html .

![Sudo echo lamp](./images/hello%20lamp.png)

to enable PHP on the website I change the directory with this stament "DirectoryIndex index.php index.html index.cgi index.pl index.xhtml" 

![sudo vim apache2](./images/php%20enable.png)
![sudo vim apache2](./images/php2%20version%20display.png)
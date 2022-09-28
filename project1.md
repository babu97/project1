# **lamp implementation procedure**
after succesfully implementing LAMP in project1 the following is the procedure used 
### step1
installed apache using  ubuntu*apt* 
```
#update a list of packages in package manager
sudo apt update

#run apache2 package installation
sudo apt install apache2
```
To verify that apache2 is running as a service in our ubuntu OS, we run the following command
```
sudo systemctl status apache2
```
If it is green and running, then you did everything correctly

Before we can receive any traffic by our Web Server, we need to open TCP port 80 which is the default port that web browsers use to access web pages on the Internet

we need to add a rule to EC2 configuration to open inbound connection through port 80

![Image](C:\Users\admin\Desktop\Dare.io\project1\iinbound rules.PNG)

our server is running and we can access it locally and from the internet. 
first, let us try to check how we can access it locally in our Ubnutu shell, run : 
```
 curl http://localhost:80
or
 curl http://127.0.0.1:80
 ```
 Now it is time for us to test how our Apache HTTP server can respond to requests from the Internet.
Open a web browser of your choice and try to access following url

```
http://<Public-IP-Address>:80
```
Another way to retrieve your Public IP address, other than to check it in AWS Web console, is to use following command:
```
curl -s http://169.254.169.254/latest/meta-data/public-ipv4
```

### step 2-installing MYSQL 
again use 'apt' to acquire and install this software
```
$ sudo apt install mysql-server
```
when prompted,confirm installation by typing Y and then ENTER when the
installation is finished,log in to the mySQL console by typing
```
$ sudo mysql
```
This will connect to the MySQL server as the administrative database user **root**, which is inferred by the use of sudo when running this command. You should see output like this:
```Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 11
Server version: 8.0.22-0ubuntu0.20.04.3 (Ubuntu)

Copyright (c) 2000, 2020, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql>
```




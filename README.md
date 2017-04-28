# COMPUTER ARCHITETURE 

## virtual machine

A virtual machine is a computer environment software in which an operating system or program can be installed and run. In a more simplified way, we can say that the virtual machine functions as a "computer inside the computer". 
Virtual machines are extremely useful on a daily basis as they allow the user to run other operating systems within a window, having access to all the software they need. They are used in a number of cases, such as launching programs and OSs that are still in the development stage. That way, you do not become hostage to unfinished applications that may have multiple bugs.
The virtual machine will allocate, during the execution of operating systems, a defined amount of RAM. It typically emulates a physical computing environment, but CPU, memory, hard drive, network, and other hardware resources will all be managed by a "virtualization layer" that translates these requests to the hardware present on the machine.
Virtual machines are able to "trick" programs and operating systems because they believe they are running directly on physical hardware, not within a simulation. Therefore, they can be installed the same way they would be inside the operating system.

## Web Server

A web server or web server is a computer that contains a special program to "serve" web pages, that server. When accessing any site, there is a server behind that address responsible for making the pages available and all other resources that you can access. So when you send an email through a form, put a message on a discussion board, make an online purchase, etc., a Web server (or a set of servers) is responsible for processing all of this information.

To be clear, a Web server is a computer that processes HTTP requests ( H yper- T ext T ransfer P rotocol), the standard Web protocol. When you use a web browser to access a website, this is due to the requests Web server through HTTP and then receives the corresponding content. In the case of Apache, it not only performs HTTP, and other protocols such as HTTPS (HTTP combined with SSL security layer - S ecure S ocket L ayer), FTP ( F ile T ransfer P rotocol) among others.
As a web server, Apache is the best known and most used. The reasons include its excellent performance, security, cross-platform compatibility and all of its features.


## Ubunto

Running the Ubuntu

- Step 1. Run VirtualBox. On the program start screen, click the "New" button;

- Step 2. At the first screen of the virtual machine creation wizard, enter a name for the new machine. Then select "Linux" in the "Type" field. Under "Version", choose the operating system, in this case, "Ubuntu". Click the "Next" button;

- Step 3. On the next screen, choose the amount of memory to be used by the virtual machine and then click the "Next" button;

- Step 4. Under "Hard disk", check the "Create a new virtual hard disk now" option. Click the "Next" button;

- Step 5. On the "Hard Disk Type" screen, check the "VDI (VirtualBox Disk Image)" option and click the "Next" button;

- Step 5. Under "Physical hard disk storage" check the "Dynamically allocated" option, so the disk file will take up little space and grow as needed. Click the "Next" button;

- Step 6. Under "Location and file size", enter the name of the file to be created, and then select the maximum file size. To confirm everything and create the disk, click the "Create" button;

- Step 7. Back in the main VirtualBox window, click on the new virtual machine created and then on the "Settings" button;

- Step 8. Under "Settings", click the item "Storage";

- Step 9. Within "Storage", click on the "Empty" item below the optical disc controller (CD / DVD icon). Once this is done, click the arrow next to the "Optical Drive" field. In the menu that appears, press the "Host Drive" option to use the physical CD / DVD drive. If you are going to use an ISO image, click the "Select Virtual Optical Disk File ..." option;

- Step 10. If you clicked on the "Select Virtual Optical Disk File ..." option, a screen will be displayed where you should indicate where the ISO image is, select and then click the "Open" button;

- Step 11. Finally, click on the virtual machine and then the "Start" button.

Installing Ubuntu Server was basically following installation options according to the following screens
Enter the name of your server.
Type your name.
Enter the user name to create a new account.
Enter the password for this new user and repeat the password on the next screen.
To check if the webserver is working. First I have to know the IP of the 
VM. Type:

ifconfig 

for Ubuntu instructions I used the following commands:

sudo apt-get upgrade
sudo apt-get install xorg lxde

I could not execute the last command successfully. This was because using different configurations or other versions of Ubuntu or other Linux distributions. May not work with the commands, so I used the command:

apt-get update

It will update the Ubuntu package index. That way it will know the latest versions of all its components and programs. After typing the command, the system will prompt for the user's password and then perform the action.

Everything after that was fine, till I started to have problems with the server. At first I thought the problem would be with the installation of the MSQL which the commands are:

Sudo apt-get install mysql-client mysql-server

I stalled it again but at the end my website still not working properly, instead images it is showing codes. So with the help of the teacher I realize the problem would be the PHP modules, so I tried the commands:

Sudo apt-get install php7.0 php7.0-mysql libapache2-mod-php7.0-cli php7.0-cgi php7.0-gd

After the installation, the page containing the information configuration were working properly, I could check it using the command:

<?php
Phpinfo();
?>

After installing the PHP I could start work again on MSQL and the wordpress (the password and etc…)
I went to the root of mysql using the command:

Mysql –u root –p

And then I have to change the archive config, using the command:

Sudo mv wp-config-sample.php wp-config.php

And to make my webserver work. I had to remove the index.htm from /var/www/html/, using the command:

Sudo rm index.htm

## Conclusion

After that my webserver was working properly. Although I couldn’t finish my project in class, I should have done the project since the beginning in my own computer because all the updating and installations programs take a lot of time. When I start to work by my own it was much easier to understand and complete the project


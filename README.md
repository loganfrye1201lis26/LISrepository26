# LISrepository26
This repository will be used to document my work throughout the semester.

## Contents
- Weekly lab notes
- Configuration steps
- Reflections on what I learned

## Tools
- Google Cloud VM
- Git & GitHub
- Command line tools

# Module 2 Learning Journal

## Virtual Machines w/ Google Cloud
I created & configured a virtual machine using Google Cloud. This allowed me to work in a remote Linux environment. I learned how cloud computing provides flexible infrastructure for hosting applications.

## Linux Command Line Interface
I practiced basic Linux commands to navigate the system, check updates, and view files. Commands such as:
- cat
- ls
- apt update

# Google Cloud Notes

## What is Google Cloud?
Google Cloud provides virtual computing resources that allow users to run servers remotely.

## What I Did
- Created a virtual machine
- Accessed the VM through terminal
- Verified operating system
- Checked system updates

## Key Benefit
Cloud environments allow scalable infrastructure for hosting applications like library systems.

# Managing Softwar & Library Search
## Install yaz Client
[apt search yaz]
- Found [yaz]
[man yaz-client]
- Very detailed documentation
- Commands & syntax explained
- Some parts easy, some overwhelming
Exit manual
[q]

## Using yaz-client
- Start client = [yaz-client]
      Prompt shows: [Z>]
- Connect to library catalog = [open z3950.loc.gov:7090/Voyager]
- Title search = [find @attr 1=4 "ancient egypt"]
- Author search = [find @attr 1=1003 "Herodotus"]

## Key takeaways
- APT manages software installation and updates
- Command line shows informational and confirmation messages
- yaz-client connects to real library catalogs
- Documentation helps understand commands

## Install & Test Apache
First, I updated the package list and upgraded installed software to ensure the system was current.
- sudo apt update
- sudo apt upgrade -y
This step refreshed available packages and installed updates for system stability and security.

# Apache Web Server
- sudo apt install apache2 -y
The installation downloaded and configured Apache and its dependencies.
# Create New Webpage
- sudo nano index.html
- <!DOCTYPE html>
<html>
<head>
    <title>My First Web Page</title>
</head>
<body>
    <h1>Welcome to My Apache Server!</h1>
    <p>This page is running on my Ubuntu virtual machine for my SYSlib assignment.</p>
</body>
</html>

## Key Concepts Learned
- Updating Ubuntu systems using apt
 Installing and managing services with systemctl
- Testing local vs external server access
- Cloud firewall configuration and HTTP traffic rules
- Apache document root structure (/var/www/html)
- Deploying basic HTML content to a web server
- Differences between Google Cloud Shell and a virtual machine environment

# Reflection
This activity provided practical experience with server deployment and web hosting fundamentals. A major challenge was initially working in Google Cloud Shell instead of the virtual machine, which prevented service management commands from functioning properly. Once inside the VM, the installation process was straightforward. Troubleshooting firewall settings also helped demonstrate how infrastructure configuration impacts service accessibility. Overall, the assignment improved my understanding of how web servers operate and how cloud-based systems manage hosted services.

## Installing PHP & Configuring Apache
In this module, I installed PHP on my Ubuntu server and configured Apache to properly process PHP files. This verified that my server can deliver dynamic content rather than just static HTML.
# PHP & Apache PHP Module
- sudo apt install php libapache2-mod-php
This installs:
The PHP runtime
The Apache PHP module that allows Apache to process .php files

# Important Troubleshooting Lesson
At first, I attempted to use systemctl from Google Cloud Shell, which produced this error:
- System has not been booted with systemd as init system (PID 1)
This happened because Cloud Shell is not the VM instance. I needed to SSH directly into the Compute Engine VM. Once inside the VM, systemctl worked properly.
This reinforced the importance of understanding environment context when administering servers.

# Testing PHP with inf.php
- sudo nano /var/www/html/info.php
  Inserted:
  - <?php
    phpinfo();
    ?>
The PHP configuration page loaded successfully, confirming:
- PHP is installed
- Apache is processing PHP
- The server is returning dynamic output

# Reflection
This module reinforced several key concepts:
1. The difference between static and dynamic web content.
2. How Apache integrates with language modules.
3. Why configuration order (DirectoryIndex) matters.
4. The importance of testing configuration changes before restarting services.
5. The necessity of understanding server context (Cloud Shell vs VM).
The most significant troubleshooting moment was realizing that systemctl must be run inside the VM, not in Cloud Shell. That distinction clarified how cloud infrastructure layers operate.

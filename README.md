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

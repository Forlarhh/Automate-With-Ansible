# Automate-With-Ansible

## Project Summary
In this hands-on project, I'll use Ansible to automate the setup of a simple web application environment on four virtual machines hosted in AWS. All four VMs are configured within the same local VPC (Virtual Private Cloud) network, ensuring secure and efficient communication between the servers.

The setup is as follows: <br>
Ansible Controller: This server is responsible for managing and orchestrating the automation tasks across the environment. <br> 
Two Web Servers: These servers will host the web application using Nginx as the web server software. They serve as the front-end for delivering the web content. <br>
One Database Server: This server will run MariaDB, handling all database operations for the application. <br>

## Implementation

### VMs Setup
![image](https://github.com/user-attachments/assets/ef127f12-6056-4b31-a910-5150ba49f4ea) <br>

### Ansible controller setup
### Login(SSH) to the ansible_controller VM and install ansible<br>
```
  sudo apt update
  sudo apt install software-properties-common
  sudo add-apt-repository --yes --update ppa:ansible/ansible
  sudo apt install ansible
```
![image](https://github.com/user-attachments/assets/2c0eeef8-a5da-41b9-bbe8-b29af074359d) <br> <br>

### Create an Ansible configuration file to specify the inventory <br>
![image](https://github.com/user-attachments/assets/65ef10ae-602d-4307-b61c-4891f47cecb6) <br> <br>


### Write inventory files
Write the inventroy files in the ansible_controller VM that will provide information (e.g. IP address, username, passwords etc) to ansible about it's targets. <br>
![image](https://github.com/user-attachments/assets/29519cd7-f221-4138-bf02-03671c6cdda6) <br> <br>


### Test Connections
![image](https://github.com/user-attachments/assets/e1f3ee0e-3605-4461-a512-2d33b0054357) <br> <br>
![image](https://github.com/user-attachments/assets/c443cde1-51a8-4498-8e6c-802873cc952e) <br> <br>


### Playbook for Web Server Setup
Create a playbook file webserver.yml for setting up Nginx on the webservers <br>
![image](https://github.com/user-attachments/assets/4198b65c-e99b-4bd6-8ff1-08490f1895ad) <br> <br>

### Playbook for Database Server Setup
Create a playbook file dbserver.yml for setting up MariaDB <br>
![image](https://github.com/user-attachments/assets/a95f6892-1506-4c4b-bf89-ac4c51815368) <br> <br>


### Run the Web Server Setup
![image](https://github.com/user-attachments/assets/dedb8e48-46c5-44e8-a494-864383942f4a) <br> <br>
![image](https://github.com/user-attachments/assets/840e0f92-20f7-422d-ba3a-19e41d6ca0ec) <br> <br>


### Confirm web server is running
![image](https://github.com/user-attachments/assets/34be11c5-7989-4d41-a429-c4f5ee4330fd) <br> <br>

![image](https://github.com/user-attachments/assets/de3a3b9f-198a-4431-a572-bbc532ef88d0) <br> <br>



### Run the Database Server Setup
![image](https://github.com/user-attachments/assets/f6c737aa-4331-40c2-a8b5-3149b4d31f05) <br> <br>
![image](https://github.com/user-attachments/assets/17c17650-3860-4533-a40d-040d1bfffbf9) <br> <br>

### Confirm database server is runnning
![image](https://github.com/user-attachments/assets/de8bdfb8-40ad-49d5-9938-7003ead09ee9) <br> <br>

Done.















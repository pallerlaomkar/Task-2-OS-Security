# Task 2: Operating System Security Fundamentals (Linux & Windows)

## Objective
The purpose of this task is to understand Operating System–level security fundamentals by performing hands-on activities in Linux (Ubuntu) and learning core concepts such as user management, file permissions, firewall configuration, service monitoring, and OS hardening best practices.

---

## Tools Used
- VirtualBox  
- Ubuntu Linux (20.04 LTS / 22.04 LTS)  
- Linux Terminal  
- UFW (Uncomplicated Firewall)  

---

## Step 1: Set Up Ubuntu Linux in a Virtual Environment
Ubuntu Linux was installed in a VirtualBox virtual machine with the following configuration:
- RAM: 2–4 GB  
- Storage: Minimum 25 GB  

The installation included selecting the keyboard layout, time zone, and creating a user account with a strong password. After installation, the Ubuntu desktop loaded successfully, confirming the setup.

---

## Step 2: Investigate User Accounts and System Identity
The following commands were used to examine user information:

```bash
whoami
id
cat /etc/passwd

## Step 3: Examine and Modify File Permissions

File permissions were inspected using:

```bash
ls -l

Permissions and ownership were modified using:

chmod 700 testfile
sudo chown root:root testfile

This demonstrated Linux access control and ownership management.


## Step 4: Differentiate Between Root and Normal Users

Root access was obtained temporarily using:

sudo su

The elevated session was exited safely using:

exit

This step showed why root access should be used cautiously.

## Step 5: Enable Firewall (UFW)

Firewall status was checked and enabled using:

sudo ufw status
sudo ufw enable
sudo ufw allow ssh

This improved the system’s network security.

## Step 6: Monitor Running Processes and Services

System processes and services were monitored using:

ps aux
top
systemctl list-units --type=service

This helped identify active processes and background services.

## Step 7: Disable Unnecessary Services

Unused services were disabled to reduce the attack surface:

sudo systemctl stop bluetooth
sudo systemctl disable bluetooth


## Step 8: Operating System Hardening Best Practices

Use strong and unique passwords

Apply the principle of least privilege

Keep the firewall enabled

Disable unused services

Regularly update the system

Monitor running processes and services

Avoid direct root login

 ## Final Outcome

Understanding of OS-level security concepts

Hands-on experience with Linux security

Knowledge of OS hardening techniques

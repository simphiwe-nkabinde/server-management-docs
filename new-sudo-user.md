# Create A New Sudo Enabled User on Ubuntu
[resource](https://www.digitalocean.com/community/tutorials/how-to-create-a-new-sudo-enabled-user-on-ubuntu)

## 1. Log into Server
SSH in to your server as the root user:
## 2. Add New User to the System
```
adduser new_user_name
```
You will be prompted to create and verify a password for the user
## 3. Add User to Sudo Group
```
usermod -aG sudo new_user_name
```
## 4. Test Sudo User Access
switch to the new user account. You may be prompted for the new user's password
```
su - new_user_name
```
prepend sudo to a command that you want to run with superuser privileges. eg:
```
sudo ls -la /root
```

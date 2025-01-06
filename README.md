# Installing-and-Configuring-IBM-QRadar

## Prerequisites
1. Install Oracle Virtual Box: 
2. Download QRadar Community Edition: https://www.ibm.com/community/101/qradar/ce/
## Architecture of IBMQRadar
I have explained in detail about the various components in QRadar which is used in log analysis, event processor, event collector, flow collector and network sources along with vulnerability scanner on my blog.
Blog: https://medium.com/@shreyassrinivasa297/architecture-of-ibm-qradar-siem-3ae0d4e56a41
## Configuring IBM QRadar
1. Enter the admin name and password.
2. Run this command to update the repositories.
```
yum update -y
```
![1](https://github.com/user-attachments/assets/2179e3f5-2a6f-4ea9-9c71-c2d7dbf7937f)

3. Rebbot.
4. Change the host name and configure the date.
![2](https://github.com/user-attachments/assets/25dd69c0-3184-4de7-a3fe-f7f7574bf56f)


## Setting up Static IP Address
- Check the network range and note down the Gateway IP and Network ID.
![3](https://github.com/user-attachments/assets/25af68d5-65db-4644-9d20-3090b78e6279)

- To assign IP address, execute this command.
```
nmtui
```
![4](https://github.com/user-attachments/assets/17de707a-f5d6-4232-9eda-4e0cf6fe458d)

![5](https://github.com/user-attachments/assets/1a30a8c0-3e0f-4994-a76e-3865dde8ad5d)

- GUI opens up and select 'Edit Connection'.
- Set the profile name as 'enp0s17'.
- Change the IPV4 config to 'Manual'.
![6](https://github.com/user-attachments/assets/2410e9f3-26d1-4315-9ad4-af6a6dd311a0)

![7](https://github.com/user-attachments/assets/44f80a89-fc10-42cd-a5dd-b103362bcad0)
- CHnage the IP address. Edit DNS servers as Gateway IP address.
- Select 'Ignore' for IPV6.

## Configuring OS
- Run this command in order to change the version to 7.5.1804.
```
cat /etc/redhat-release
vi /etc/redhat-release
```

## Install the application
- Execute the commands.
![8](https://github.com/user-attachments/assets/612a7253-dde6-486b-81fd-c11b4a86a8e9)

```
ls -> to view the contents in present directory.
./setup
```
![9](https://github.com/user-attachments/assets/a479a673-1795-4033-a7d9-9a601389a486)
The installation takes a while, so you can go grab a coffee and relax.

Once the installation is complete, reboot the system.
![10](https://github.com/user-attachments/assets/7d9d8d1a-0a5e-4348-87b3-ed1bffbb28de)

And to interact with the console, search for the IP address on your favourite browser and login with the credentials.

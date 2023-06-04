# Local_Remote_Control

X: device with W11
Y: device with linux (Pop!_OS)


Goal: use Y's terminal through X's.

# To Do: Y (Pop!_OS)

1. Open terminal and install SSH server: 
```
sudo apt update
sudo apt install openssh-server
```

2. When installed, it should be automatically running, check it with:
```
sudo systemctl status ssh
```

3. You need to know the ip of this device, get it with:
```
ip addr show
```
Look for he IP Address in 'inet' section, under 'eth0' or 'wlan0' (it depends if you are onlineby Ethernet or Wi-Fi).

# To Do: X (Windows 11)

1. Open PowerShell

2. SSH client should be already installed in W11. You can connect to the SSH server through this command:
```
ssh <username>@<IP>
```
<username> is the user you want to connect in Y (Pop!_OS)
<IP> is the local IP of Y

3. You'll have to accept the security key this first time. Type 'yes' and  press Enter.
You must know that this can take a while if it is the first time you are connecting both devices.
But, if it takes a lot longer, consider some of the next issues:
 - Check the IP is correct
 - Check SSH server is running in Y ```sudo systemctl status ssh````
 - Check you can ping the IP you want to connect ```ping 192.168.1.1```
(if you cannot connect after this... good luck XD)

4. Now, type the password of the <username> you are connecting to.



# Recommendations
Just for security reasons, remember to enale SSH only if it is necessary and consider other sucurity measurements:
1. Use a SSH key instead of a password
2. Change SSH default port

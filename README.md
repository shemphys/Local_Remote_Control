# Local_Remote_Control

X: device with W11
Y: device with linux (Pop!_OS)


Goal: use Y's terminal through X's.

# Y (Pop!_OS)

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
Look for he IP Address in 'inet' section


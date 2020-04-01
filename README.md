# Robohand (raspberry pi part)
### All steps did in the ROS melodic on raspberry pi 3 with ubuntu mate 18
***Languages: C++***
## In order to run last node make ten steps:
1. You need download ubuntu on your rapberry pi
2. Create ssh keys and send public key to your raspbery by command
```
ssh-copy-id -i your_key.pub raspberry_account@raspberry_ip
```
3. On yout main PC create file in ~/.ssh folder (call it **config**) and put information about you secret key and 
```
Host raspberry_account@raspberry_ip
    IdentityFile path_to_your_secret_key
```
4. Then enter to your raspberry with the ssh
5. After all mentioned above download ROS melodic (you can find tutorial in the robohand repository)
6. Create project (you can find tutorial in the robohand repository)
7. Clone this repository and insert it instead of your project folder
8. Now you need include in /etc/host this string
```
your_main_PC's_IP name_of_account
```
Example
```
192.168.0.10 my_pc
```
9. Write that command (insert you IP instead of frase <IP>)
```
export ROS_MASTER_URI=http://IP:11311/
```
10. Now you can run last node (if you run rosnode on your main PC)
```
rosrun arm pwm_sender
```

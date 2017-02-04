# torrentinthecloud
<img src="https://cloud.githubusercontent.com/assets/633843/9855504/f30a715c-5b51-11e5-83f3-f4fab03e5459.png" alt="screenshot"/>

JPillora's **cloud torrent** on Microsoft Azure! 
This will make you use microsoft's Azure free trial (200$) for one month will the infamous cloud torren

### Install -

**Microsoft Azure**

1. [Sign up](https://azure.microsoft.com/en-in/offers/ms-azr-0044p/) for the free trial that gives 200$ of usage for one month. If you want more, just use different email accounts.
2. After creating, create a virtual machine with Ubuntu (any ubuntu).
3. Complete the required details. Use a password and not an SSH key. REMEMBER the password and the username! 
4. Select the smallest storage and other options. And finish it. Wait for it to deploy. 
5. After azure finishes the deployement, open the virutal machine. Note down the IP adress. You already know the Username and Password. 
6. Download and run PUTTY. Use the IP given in the virtual machine as the HOST name and connection type as SSH. the port is 22 and click on open.
7. Then use the credentials to login to the virtual machine. 
8. First to keep the app running even after we close the session, we nee to run the screen command. 

Do the exact same thing what's down below. 

```
     screen
    curl https://i.jpillora.com/cloud-torrent! | sudo bash
    cloud-torrent -p 3000
```
ctrl+a and then press d

This will "disconnect" you from the screen session. At this point, you can log out or do anything else you'd like.

When you want to re-connect to the screen session, just run screen -RD from the shell prompt (as the same use user that created the session).


Now, we need to forward the IP. For this, 

Go to - All resources. Select the "network security group" of your machine. Now click on "Inbound security rules". Select ADD. give a name, source = any, protocol = any, and port range = 10-65535. action = allow and the save.

You're done! Now open the given IP in you machine with port 3000 (or the port you used in the code. 3000 in this case). 

xxx.xxx.xxx.xxx:3000

Done. 

### Notes
Thanks to jpillora for saving all our lives! see his original work at [jpillora's Cloud Torrent](https://github.com/jpillora/cloud-torrent)

#### License

Copyright (c) 2016 Jaime Pillora

[Creative Commons Legal Code - Attribution-NonCommercial 3.0 Unported](LICENSE)


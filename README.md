![ubuntu](/docs/img/ubuntu.png)
# Guide to installing Ubuntu and bash in Windows 10

1. Search for windows settings - windows icon bottom left > space bar key will open search. Search for ```Use developer features``` and open this

2. Choose the option Developer mode

3. Search and open the app ```Microsoft Store```

4. In the Microsoft Store app search for Ubuntu 18.04

5. Install Ubuntu. Pin the program to your windows task bar at the bottom of the screen.

6. Use Windows search again and look for a program called ```Windows PowerShell```. Right click to ```run as administrator```

7. Run the command: 
    ```
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```
    and then close PowerShell.

8. Open the Ubuntu app and follow the propts to create a username and password. It's highly reccommended to use your firstname as a username all in lowercase. NOTE: this is permanent so don't rush this. The password will not show as you type so expect not to see anything until you press enter.

9. type ```pwd``` you should be in your home directory ```/home/yournamehere```

10. Navigate to your windows home directory by typing:
    ```linux
    cd /mnt/c/users/
    ```
    then type:
    ```
    ls
    ```
    which will show you the name of your Windows user folder (most likely your name). Change into this directory:
    ```
    cd yourwindowsusername
    ```
    create a new folder here:
    ```
    mkdir apps
    ```
    change directories into apps
    ```
    cd apps
    ```
    print the current directory:
    ```
    pwd 
    ```
    You should see your directory path similar to this: ```/mnt/c/users/yourname/apps```
    Copy this for later. Now go back to your Ubuntu home directory:
    ```
    cd
    ```
    If you type ```pwd``` again you should see ```/user/yourname```

11. Now create a link to your apps folder using the path you copied earlier:
    ```linux
    ln -s /mnt/c/users/yourname/apps
    ```

12. View the link to apps using ```ls```, you should see:
    ```
    apps
    ```

13. Now whenever you use Ubunut you can cd directly to your apps directory held in the Windows user folder!
    ```
    cd apps
    ```


   
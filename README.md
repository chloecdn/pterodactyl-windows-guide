# pterodactyl-windows-11-guide

# This is a Guide for how to install Pterodactyl on your Local windows machine without having access to a second pc, vps, or similar to run linux on.

<h2>NOTE: For this, Your CPU and Motherboard REQUIRE support for either AMD-V (or AMD-SVM on some Boards) or Intel VT-X respectively. Without it, it won't work.</h2>
<h2>NOTE 2: DONT USE THIS FOR ACTUAL PUBLIC SERVER HOSTING. For that, you are required to forward your router-ports, which will eventually put you in danger. Only use this for Cases like Theme-Development, Plugin/Mod-Testing, etc. Don't say i didn't warn you...</h2>

  - If your PC supports this, go into your UEFI, enable it, and reboot.
  - Additionally, you need to Enable HyperV inside Windows by searching for `Optional Features` in the Start-Menu:<br>

  ![image](https://user-images.githubusercontent.com/80840951/224378299-b7a8c90c-cb20-453c-8607-847117aad762.png)
  ![image](https://user-images.githubusercontent.com/80840951/224378457-5b24cf39-c977-459d-a5d0-f27c661533f1.png)
  
  - After doing that, reboot again, and you're done.
  
<h2>After that, open a Terminal and run `wsl --install -d ubuntu-22-04` to install a Virtual Machine via WSL.</h2>

  - It's going to ask you for a username and password, just enter something you remember.
  - Now inside the VM, you're ready installing the Panel. This consists of essentially the exact same steps from the DOCS, EXCEPT:
    - You don't want to use SSL/HTTPS. It's going to be local-only anyway.
    - Everytime you're beeing asked for either an FQDN or domain, just use your wsl's actual ip address. You can find it out by running `ip addr` inside WSL):
    
    ![image](https://user-images.githubusercontent.com/80840951/224380524-1a3689a4-d02a-43ad-a52a-955a1d5f5f19.png)

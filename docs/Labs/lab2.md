---
id: lab2
title: Lab 2 - Installing Virtual Machines
sidebar_position: 2
description: Installing 3 virtual machines that will be used for the rest of the course.
---

# Lab 2: Installing Windows Server 2025 and Windows 11 Virtual Machines

## Overview

This week's lab will cover the following:

- Accessing VMWare Workstation Pro
- Installing the following 3 Virtual Machines:
  - Server1: Windows Server 2025 Datacenter (with GUI)
  - Server2: Windows Server 2025 Datacenter Core (without GUI)
  - Client1: Windows 11 Education   
- Performing post-installation tasks on all 3 virtual machines

## Lab 2 Notes



## Objectives

By the end of this lab, you will be able to:

- use VMWare to install virtual machines
- install a GUI version of Windows Server 2025
- install a GUI-less version of Windows Server 2025
- install an Education version of Windows 11
- recognize the differences in these installations and the time/resources needed for each

## Investigation 1: Installing your VMs

In this investigation, you will install all 3 virutual machines using VMWare Workstation Pro on a Seneca lab computer.

1. Begin by logging into a Seneca lab computer and then plugging in your external hard drive (which should have your ISO files and Keys text file on it from Lab 1)
2. Check to make sure your external hard drive is recognized by the computer by opening the File Explorer and navigating to your external hard drive.
3. Double check that the directories you created in lab 1 are there.
4. Open VMWare Workstation Pro from the desktop.


### Part 1-1: Installing Windows Server 2025 Datacenter (GUI)

In this part, you will install Windows Server 2025 Datacenter with a GUI.

1. Click "Create a New Virtual Machine" on the Home tab in VMWare Workstation Pro.
2. Select "Typical" and click "Next".
3. Select "Installer disc image file (iso)" and then click "Browse".
4. Navigate to the ISOs directory on your external hard drive and open the Windows Server 2025 ISO. 
5. You should notice a message below the path to the ISO that says "Windows Server 2025 detected. This operating system will use Easy Install". Click "Next"
6. Enter your Windows Server 2025 product key (which should be in your "Keys" file on your external hard drive).
7. For "Version of Windows to Install" leave the default (should be "Windows Server 2025 Datacenter").
8. For "Full name", enter "Administrator".
9. For "Password", enter "P@ssw0rd".
10. Do **NOT** check "Log on automatically". Click "Next".
11. For "Virtual Machine name", enter "Server1".
12. For "Location", click "Browse" and navigate to and select the directory called "Server1" in your external hard drive and click "OK". Confirm the path to your "Server1" directory has been selected (this is important, if you create your VM on the lab computer and not your external hard drive, it will be lost when you turn off the computer). Click "Next". 
13. Leave the disk size at 60 GB and select "Store virtual disk as a single file". Click "Next"
14. Click "Customize Hardware".
15. Change "Memory" to 4096 MB.
16. Change "Processors" to 1 Processor and 4 cores per processor. Click "Close". Click "Finish".
17. The virtual machine will launch and the installation will begin. You will be asked to put your product key in once again. Do so and click "Next".
    - *to "paste" into the VM, click inside the Product Key box so that the cursor is seen inside it, then click "Edit" in VMWare and select "Paste".
18. From here, most of the installation will be automatic. The VM will restart several times during the installation.
19. Eventually you will land on the Windows Server 2025 desktop and VMWare Tools will auto-install. When it is finished, it will ask you to restart the system. Click "Yes" and your VM will reboot. 

### Part 1-2: Windows Server 2025 GUI Post-Installation Tasks

Now that our Server1 is installed, there are a few things we need to do to prepare it for our labs. We are going to ensure our Time Zone is correct and we are going to name our system appropriately. Then we are going to make sure our system is completely updated. FInally, we will confirm internet connectivity and download a better web browser.

1. Log into your Server1. To use Ctrl+Alt+Del in your VM, click "VM" in VMware and select "Send Ctrl+Alt+Del".
2. You should be met with the Server Manager Dashboard. If not, click on the Server Manager icon at the bottom of the screen.
3. A pop up will appear asking you to "Try Windows Admin Center/ Azure Arc". Click "Don't show me this message again" and close the pop-up.
4. Click "Local Server" on the left side of the screen. 
5. In the "Properties" window, look for "Time Zone" and make sure it is set to "UTC -05:00 Eastern Time". If it is something else, change it to our time zone.
6. Next, click on the semi-randomized name next to "Computer Name". Then click "Change".
7. Change the computer name to "S1-SenecaID" (for example, my Seneca ID is hheim so my Server1 computer name would be "S1-hheim").
8. Leave the default Workgroup selected and click "OK". A message will pop up saying the computer name will not change until the system is restarted. Click "OK".
9. Close the Computer Name window and another message will pop up asking if you want to restart the computer now. Click "Restart Later".
10. Next, find "Windows Update" in the "Properties" window and click the blue text beside it. Click the blue "Check for updates" button.
11. Windows Server will now download and install all necessary updates.
12. While they are downloading, scroll down and click on "Advanced Options".
13. Turn the "Receive updates to other Microsoft products" toggle from **Off** to **On**.
14. Click "Windows Update" at the top of the screen to get back to the main Updates window.
15. You will likely need to wait a little while for the updates to finish downloading and installing. Eventually, all the updates listed will say "Pending restart". Once you see this, click the blue "Restart now" button.
16. Server1 will reboot and install updates. This will likely take a while and it will likely reboot a few times but just let it do its thing. Do not turn off the VM while it is updating. If your VM freezes during the updates, check with you teacher before moving forward.
17. When you are met with the login screen, log in and return to the Updates window.
18. Click the blue "Check for updates" button. If any remaining updates are available they will install. Repeat this cycle until you are met with a "You're up to date" message.
19. Next, we are going to confirm internet connectivity and download a different web browser that MS Edge.
20. Open MS Edge (the icon will be at the bottom of your screen).
21. Go through the first-run questions (just say no to everything).
22. Go to the Mozilla Firefox website: www.firefox.com
23. Download Firefox and install it.
24. Once it is installed, open Firefox and go to google.com to make sure everything is working.
25. Shutdown your Server1.



### Part 2-1: Installing Windows Server 2025 (No GUI)

Now we are going to install our second server, Server2. This installation will be very similar to the first, although the server will look quite different when we are done. 

1. Click "Create a New Virtual Machine" on the Home tab in VMWare Workstation Pro.
2. Select "Typical" and click "Next".
3. Select "Installer disc image file (iso)" and then click "Browse".
4. Navigate to the ISOs directory on your external hard drive and open the Windows Server 2025 ISO. 
5. You should notice a message below the path to the ISO that says "Windows Server 2025 detected. This operating system will use Easy Install". Click "Next"
6. Enter your Windows Server 2025 product key (which should be in your "Keys" file on your external hard drive).
7. For "Version of Windows to Install" change it to "Windows Server 2025 Datacenter Core". **VERY IMPORTANT!!**
8. For "Full name", enter "Administrator".
9. For "Password", enter "P@ssw0rd".
10. Do **NOT** check "Log on automatically". Click "Next".
11. For "Virtual Machine name", enter "Server2".
12. For "Location", click "Browse" and navigate to and select the directory called "Server2" in your external hard drive and click "OK". Confirm the path to your "Server1" directory has been selected (this is important, if you create your VM on the lab computer and not your external hard drive, it will be lost when you turn off the computer). Click "Next". 
13. Leave the disk size at 60 GB and select "Store virtual disk as a single file". Click "Next"
14. Click "Customize Hardware".
15. Change "Memory" to 4096 MB.
16. Change "Processors" to 1 Processor and 4 cores per processor. Click "Close". Click "Finish".
17. The virtual machine will launch and the installation will begin. You will be asked to put your product key in once again. Do so and click "Next".
    - *to "paste" into the VM, click inside the Product Key box so that the cursor is seen inside it, then click "Edit" in VMWare and select "Paste".
18. From here, most of the installation will be automatic. The VM will restart several times during the installation.
19. Eventually you will land on the Windows Server 2025 desktop and VMWare Tools will auto-install. When it is finished, it will ask you to restart the system. Click "Yes" and your VM will reboot. 

### Part 3: Creating Your MST100 Working Directories and Storing the ISOs Inside

Now that we have our ISOs we are going to store them on our external hard drive so that we can use them to create our virtual machines in Lab 2. Before we actually move them, we are going to create a nice, organized directory structure for all of our MST100 lab work.

1. Plug your external hard drive into the computer you downloaded your ISOs onto and open the File Explorer.
2. Navigate to your external hard drive.
3. Create a directory called "MST100" and move into that directory.
4. Inside the MST100 directory create the following 5 directories:
  - "ISOs"
  - "Notes"
  - "Server1"
  - "Server2"
  - "Client1"
5. Finally, find the Windows Server 2025 Datacenter and Windows 11 Education ISOs on your computer (probably in your Downloads directory) and copy them into your newly created "ISOs" directory.

Now you have your ISOs in the right place and you have your directories ready to install to in next week's lab.

## Investigation 2: MST100 Pre-Lab Chart

The last thing we have to do is gather some information about our virtual machines and virtual network that we will be using later in the semester.

Below this picture of the chart, you will find a link to a downloadable file of the MST100 Pre-Lab Chart.

![MST100 Pre-Lab Chart](/img/mst100prelabchartpic.png)

[Download MST100 Pre Lab Chart](/files/MST100PreLabChart.docx)

You must download this file and fill it out completely.

## Lab 1 Sign Off

Upload your fully completed MST 100 Pre-Lab Chart to the Lab 1 submission page in Blackboard.



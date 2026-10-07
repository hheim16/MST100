---
id: lab3
title: Lab 3 - Configuring Windows Server
sidebar_position: 3
description: Configuring basic settings in Windows Server and Windows 11
---

# Lab 3: Configuring Windows Server

## Overview

This week's lab will cover the following:

- Adding and removing roles in Windows Server
- Learning about and editing the registry


## Lab 3 Notes

The primary method to run do the labs in MST100 is to use virtual machines running on 

## Objectives

By the end of this lab, you will be able to:
- Add roles in Windows Server
- Remove roles in Windows Server
- Export Registry entries for backup
- Add registry entries
- modify registry entries

## Investigation 1: Installing and Removing Roles

### Part 1: Installing Roles

In this investigation, you will install 3 new roles into Server1 and then remove 1.

1. Begin by logging into Server1 and open Server Manager.
2. Click on "Add roles and features".
3. The "Add Roles and Features" wizard window will appear. Click "Next".
4. Select "Role based or feature-based installation" and click "Next".
5. Select your server (it should be the only one there) and click "Next".
6. The next screen will have a listing of all he available roles that can be installed onto your Windows Server. Check the following 3 roles (*NOTE: As you select each role, it will prompt you to add necessary features for that role. Accept what it gives you to install and click "Add Features"*):
  - Print and Document Services
  - Web Server (IIS)
  - DNS (When selecting DNS you will get a Validation Results warning. Do not worry about this. We will be fixing this issue in lab 4. Just click "Continue" when it appears)
7. With all 3 roles selected, click "Next".
8. Click "Next" on the next few windows, accepting the default options each one gives you until you arrive on the "Confirm installation selections" window.
9. Check the "Restart the destination server automatically if required" box and then click "Install".
10. Your roles will now be installed onto Windows Server. Wait for the installations to all complete and then click "Close".

You should now see the new roles you installed have been added as tiles in your Server Manager listed under "Roles and Server Groups". They will also appear in the top-left area of Server Manager listed under "Dashboard", "Local Server", and "All Servers". We will leave them for now but we will come back to DNS and IIS in lab 4.


### Part 2: Removing Roles

Now that we have roles 

1. Click "Create a New Virtual Machi

## Lab 3 Sign Off

Take the following 3 screenshots:
- Log into Server1. Go into the Server Manager on Server1, click on "Local Server", and take a screenshot of the entire "Properties" window.
- Log into Server2. Take a screenshot of the "Welecome to Windows Server 2025 Datacenter" screen.
- Log into Client1. Go into the Windows Update window and take a screenshot that shows the "You're up to date" message.

Put all 3 of these screenshots into a text document and upload it to the Lab 2 Submission page in Blackboard.



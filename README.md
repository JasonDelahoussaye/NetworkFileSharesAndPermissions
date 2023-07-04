<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [Network File Shares and Permissions](https://drive.google.com/file/d/1V_4tRnOFsca0z34e6vLhDkQvt7F80qUj/view?usp=drive_link)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

# Setting Up Network File Shares and Permissions Tutorial

This tutorial will guide you through the process of setting up network file shares and permissions using Windows Server and Active Directory.

## Prerequisites

To follow along with this tutorial, you will need the following:

- Windows Server installed and configured.
- Active Directory domain set up.
- Two client machines connected to the domain.
- Administrative access to the server and clients.

## Part 1: Creating Security Groups

In this section, we will create a security group that will be used to assign permissions to the network file share.

1. Open the Active Directory Users and Computers management console on the server.
2. Expand the domain and navigate to the "Users" container.
3. Right-click on the container and select "New" > "Group".
4. Enter a name for the group (e.g., "Accountants") and click "OK" to create the group.
5. Once the group is created, you can add users to it by double-clicking on the group, selecting the "Members" tab, and clicking "Add".

![Screenshot 1](screenshot1.png)
*Screenshot 1: Creating a Security Group*

## Part 2: Creating a Network File Share

Now, let's create a network file share that will be accessible to the security group we created.

1. Open the File Explorer on the server.
2. Right-click on the folder you want to share and select "Properties".
3. In the Properties window, go to the "Sharing" tab.
4. Click on the "Advanced Sharing" button.
5. Check the box that says "Share this folder" and click "Permissions".
6. In the Permissions window, click "Add" to add the security group.
7. Type the name of the security group in the text field and click "Check Names" to verify it.
8. Once the group is verified, click "OK" to add it.
9. In the Permissions window, select the security group and assign the desired permissions (e.g., read, write, modify).

![Screenshot 2](screenshot2.png)
*Screenshot 2: Creating a Network File Share*

## Part 3: Assigning Permissions to a Folder

In this section, we will give the security group read and write permissions to a specific folder.

1. Go to the folder you want to assign permissions to on the server.
2. Right-click on the folder and select "Properties".
3. In the Properties window, go to the "Security" tab.
4. Click on the "Edit" button to modify the permissions.
5. In the Permissions window, click "Add" to add the security group.
6. Type the name of the security group in the text field and click "Check Names" to verify it.
7. Once the group is verified, click "OK" to add it.
8. Select the security group from the list and check the boxes for the desired permissions (e.g., read, write) under the "Allow" column.

![Screenshot 3](screenshot3.png)
*Screenshot 3: Assigning Permissions to a Folder*

## Testing the Permissions

To test the permissions, go to the client machine and try accessing the shared folder using a user account that is a member of the security group.

## Clean Up

Once you have completed the lab and no longer need the resources, make sure to shut down or delete the virtual machines to avoid unnecessary usage of your resources.

---

I hope this tutorial helps you understand network file shares and permissions better!

<p align="center">
<img src="https://i.imgur.com/SxDwnok.jpg" alt="osTicket logo"/>
</p>

<h1>Understanding File Shares</h1>
This tutorial outlines File Shares and how they work. We will create and test file shares and also, talk about security groups. We will also create and test Security groups as well. <br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Active Directory

<h2>Operating Systems Used </h2>

- Windows 10</b> 
- Windows Server 
 
<h2>List of Prerequisites</h2>
This is a continuation of the previous tutorial. You must have completed the previous tutorials in order to proceed with this one. 

<h2>What Is It?</h2>

<p>
<img src="https://i.imgur.com/mnez83t.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
File sharing is the public or private sharing of files or folders on a computer connected to a network.
</p>
<br />

<h2>Create some sample file shares with various permissions</h2>

<p>
<img src="https://i.imgur.com/pwgiPwZ.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
Let us go back into our Active Directory and select a random user that we created from the previous tutorials. I picked one named "bas.pag" but you can pick whoever you like. We used a script to generate all these random users and gave all of them the same password (Password1). I will now go log into my Client-1 Virtual Machine using the credentials for bas.pag (mydomain.com\bas.pag | Password1).

</p>
<br />

<p>
<img src="https://i.imgur.com/Bnjabwx.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
On DC-1, on the C:\ drive, create 4 folders: “read-access”, “write-access”, “no-access”, “accounting”. <br>
Set the following permissions (share the folder) for the “Domain Users” group:<br>
Folder: “read-access”, Group: “Domain Users”, Permission: “Read”<br>
Folder: “write-access”,  Group: “Domain Users”, Permissions: “Read/Write”<br>
Folder: “no-access”, Group: “Domain Admins”, “Permissions: “Read/Write”<br>
(Skip accounting for now)<br>

</p>
<br />

<h2>Attempt to access file shares as a normal user</h2>

<p>
<img src="https://i.imgur.com/wyYa5uO.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
On Client-1, navigate to the shared folder (start, run, \\dc-1). Try to access the folders you just created. Which folders can you access? Which folders can you create stuff in? Does it make sense?


</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />


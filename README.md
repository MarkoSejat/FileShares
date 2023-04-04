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
On DC-1, on the C:\ drive, create 4 folders: “read-access”, “write-access”, “no-access”, “accounting”. 
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
 

 <h2>Create an “ACCOUNTANTS” Security Group, assign permissions, an test access</h2>
 
</p>
<br />


<p>
<img src="https://i.imgur.com/92JLYqj.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/iLJb9f2.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back to DC-1, in Active Directory, and create a new Organizational Unit called "_SECURITY_GROUPS". Once we did that, we can right-click +SECURITY_GROUPS, click new, then groups, and create a security called “ACCOUNTANTS”. We won't add anyone to this group yet but we will use it to assign permissions. 

</p>
<br />


<p>
<img src="https://i.imgur.com/l5lOCMe.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
While still in DC-1, On the “accounting” folder you created earlier, set the following permissions:<br>
Folder: “accounting”, Group: “ACCOUNTANTS”, Permissions: “Read/Write”
</p>
<br />


<p>
<img src="https://i.imgur.com/31qi4QQ.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
On Client-1, as  <someuser>, try to access the accountants folder. It should fail. Now let us log out of Client-1.

</p>
<br />


<p>
<img src="https://i.imgur.com/NCWeK8w.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/q6dn026.jpg" height="100%" width="100%" alt="Disk Sanitization Steps"/>
</p>
<p>
On DC-1, make (in my case it was "bas.pag") a member of the “ACCOUNTANTS” Security Group. To do this just click on the ACCOUNTANTS security group we created in AD and then click members and then add. From there you can add the user you were trying to access the accountants file with before.
 Restart the Client-1 VM, Sign back into Client-1 and try to access the “accounting” share in \\DC-1\ - Does it work now?
</p>
<br />


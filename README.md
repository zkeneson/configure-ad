<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Set Up Windows 10 VM (Client) and Windows Server VM (Domain Controller)
- Configure IP settings for Domain Controller
- Make DC IP Address Static
- Create userbase of employees in Active Directory
- Set Group Policy parameters

<h2>Deployment and Configuration Steps</h2>

<p>
<img width="1919" alt="image" src="https://github.com/user-attachments/assets/f4a4f3ff-4ea8-4e80-bf1d-ef24d16d57da" />

</p>
<p>
In Azure, configure the IP settings for the Domain Controller's Network Interface Card.
</p>
<br />

<p>
<img width="1915" alt="image" src="https://github.com/user-attachments/assets/c94d7884-05ae-4d50-864c-9b9345b2436e" />

</p>
<p>
Set the DC's DNS server to custom and use the static Private IP address. 
</p>
<br />

<p>
<img width="808" alt="image" src="https://github.com/user-attachments/assets/0da707ec-738c-4488-a035-ce2e92c5a6aa" />

</p>
<p>
From the Windows VM (Client-1), open PowerShell and ping the static IP address. Then, run ipconfig /all and observe the DNS server address is the static IP of the DC.
</p>
<br />

<p>
<img width="1550" alt="image" src="https://github.com/user-attachments/assets/225dc840-a1bb-4912-b22f-c166d6f354aa" />


</p>
<p>
Create Active Directory Employees using PowerShell script and observe the new list of generated Employees. 
</p>
<br />

<p>
<img width="1578" alt="image" src="https://github.com/user-attachments/assets/a39ed57a-a399-4abd-95e8-9ca4d6779ed9" />

</p>
<p>
In the Domain Controller VM, create an Account Lockout Policy within the Group Policy Management Editor. 
</p>
<br />

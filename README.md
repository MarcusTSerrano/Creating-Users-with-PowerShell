<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Creating Users with PowerShell</h1>
This tutorial outlines using a script in PowerShell to create multiple user accounts at once<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1 Setup Remote Desktop for non-administrative users on Client-1
- Step 2 Create a bunch of additional users and attempt to log into client-1 with one of the users

<h2>Setup Remote Desktop for non-administrative users on Client-1</h2>

![image](https://github.com/user-attachments/assets/0d6159fe-1ff5-4961-8573-dfcdd3014872)

<p>
Log into Client-1 as mydomain.com\jane_admin
</p>

![image](https://github.com/user-attachments/assets/609de193-d38a-4dde-8ac3-0005025dbe8d)

<p>
Open system properties and click “Remote Desktop”
</p>

![image](https://github.com/user-attachments/assets/726def38-a5f3-423c-83a8-78e415ff5823)

<p>
Allow “domain users” access to remote desktop
</p>

<h2>Step 2 Create a bunch of additional users and attempt to log into client-1 with one of the users</h2>

![image](https://github.com/user-attachments/assets/5d786791-7f9a-414f-b2bb-f5ce4eb46b66)

<p>
Login to DC-1 as jane_admin
</p>

![image](https://github.com/user-attachments/assets/ad2b6da2-87c4-48d0-8b9a-3e752a661b02)

<p>
Open PowerShell_ise as an administrator
</p>

![image](https://github.com/user-attachments/assets/d72a83eb-1e83-41db-ae39-08877d96a426)

<p>
Create a new File and paste the contents of the script into it
</p>

![image](https://github.com/user-attachments/assets/3ca7f907-bf75-4d3f-83dc-5c847f89b1d3)

<p>
Run the script and observe the accounts being created
</p>

![image](https://github.com/user-attachments/assets/0376d237-631c-48c5-990f-d8b625293a01)

![image](https://github.com/user-attachments/assets/b783f86c-0b35-43a0-9428-921f9dc57ed4)

<p>
When finished, open ADUC and observe the accounts in the appropriate OU　(_EMPLOYEES)
</p>

![image](https://github.com/user-attachments/assets/bd982e45-5ede-4208-82ad-029238d4b615)

<p>
attempt to log into Client-1 with one of the accounts (take note of the password in the script)
</p>

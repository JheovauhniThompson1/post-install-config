<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Acknowledge the difference between the Agent Panel and the Admin Panel
- Create and Configure: Roles, Departments, and Teams
- Allow anyone(employyes+ and customers) to create tickets
- Configure Agents and Customers
- Configure SLA and Help Topics

<h2>Configuration Steps</h2>


<p>
<img src="https://github.com/user-attachments/assets/23a345d2-4c0b-4c91-a10a-29923b271278"/>
<img src="https://github.com/user-attachments/assets/04a34807-47eb-4163-a993-0e4416547e41"/>
</p>
<p>
After loging into Remote Desktop, I accessed osTicket using Internet Information Services (IIS) Manager and logged in as an administrator. I noticed a major difference between the admin panel and the Agent panel: the admin panel contained far more back end information, whilst the Agent panel contained more front end information.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/56e0cb58-bf3c-4885-9011-f8c7a6ea9213"/>
<img src="https://github.com/user-attachments/assets/8ddbd5cb-0084-4779-b0a6-abdf360f065c"/>
<img src="https://github.com/user-attachments/assets/6c44bdb3-dcb5-45ad-a24c-82f1b5ef6cc3"/>
</p>
<p>
In this stage, I went to the Admin panel, clicked Agents, then Roles, and created a new role called "Supreme Admin" with all necessary permissions. After that, I went back to Agents, clicked Departments, and created a new department named "SysAdmins" with the parent "Top Level Department". Finally, I returned to Agents, clicked on Teams, and created a new team named "Online Banking".
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/079287c1-98ab-4f5c-b783-0c28251d0986"/>
</p>
<p>
The following stage is quite straightforward; all I did was ensure that anyone may create tickets without having to register with osTicket. To accomplish this, I returned to the Admin panel, navigated to Settings -> Users, and unchecked the box "Require registration and login to create tickets."
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/f486ec7b-448d-4240-8ed9-46e29dbe16bb"/>
<img src="https://github.com/user-attachments/assets/ec7d63b4-47fa-4669-8bcc-8052a5d8110f"/>
<img src="https://github.com/user-attachments/assets/9788b0bd-d44a-4ada-9c36-e7f353ec9fa6"/>
</p>
<p>
In this phase, I created two Agents: Murphy McAllen and Jessica Jones. Murphy was assigned to the Support Department with the Limited Access role and no team, whereas Jessica was assigned to the SysAdmin Department with the Supreme Admin Role and the Online Banking Team. In addition, I established two users: Ken Carlton and Barbra Carson. This time, I went to the Agent panel, clicked Users, and then pressed Add New.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/4b825ec8-892a-4e3a-8962-464a3a81d57f"/>
</p>
<p>
For this final step, I'll return to the admin panel, click on Manage -> SLA, and create three SLAs: Sev-A, which means the issue within the ticket must be resolved within an hour and worked on 24/7; Sev-B, which means the issue within the ticket must be resolved within a four-hour grace period and worked on 24/7; and Sev-C, which means the issue within the ticket must be resolved within an eight-hour grace period and can be worked on during business hours. Finally, I returned to Manage and selected Help Topics to add: Business Critical Outage, Personal Computer Issues, Equipment Request, Password Reset, and Other.
</p>
<br />

# Active-Directory-Setup
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed using Oracle VirtualBox</h1>
This tutorial outlines the implementation of on-premises Active Directory within Oracle VirtualBox virtual machines. We use two VMs to simulate an enterprise enviornment. One VM as a domain controller and the other as a client machine. We are using VirtualBox specifically because it allows us to place created VMs within the same virtual network.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: Active Directory Setup](https://youtu.be/znJBrEnuL20)

<h2>Environments and Technologies Used</h2>

- Oracle VirtualBox (Virtual Machines)
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2019
- Windows 10 (21H1)



<h2>Important  Configuration and Deployment Steps</h2>

- Configuration for Domain Controller machine

<p>
<img width="489" height="583" alt="image" src="https://github.com/user-attachments/assets/91c278cf-db6f-40db-82a3-037f229231de" />
>
</p>
<p>
The most important setting here is the network configuration. Make sure we have two network adapters enabled. One under NAT and one as internal network renamed as you would like. This will allow the DC machine to connect to the internet and communicate with the client machine. 
</p>
<br />

- Configuration for Client machine

<p>
<img width="487" height="535" alt="image" src="https://github.com/user-attachments/assets/b14fbe0f-6aa0-4064-8689-59d8cd632190" />
>
</p>
<p>
Similarly, make sure the network adapter here is under the same internal network as the DC machine. This allows communication between both machines.
</p>
<br />

- Adding admin account to Domain Admins

<p>
  
<img width="463" height="400" alt="image" src="https://github.com/user-attachments/assets/859d6895-089c-47bc-9529-9884a6019089" />

</p>
<p>
We have made our first admin account(in this case, the John Doe account). Now we have to add this account to the Domain Admins group. This will allow the account to make changes to the domain.
</p>
<br />

- Adding Client VM to Domain

<p>
<img width="336" height="378" alt="image" src="https://github.com/user-attachments/assets/3259ee04-3993-4165-84c2-853e1ee495ac" />

</p>
<p>
When renaming the client machine, we will choose the advanced option. Then make sure we have the domain option selected and the correct domain name entered.
</p>
<br />

- Confirming communication between both machines

<img width="463" height="355" alt="image" src="https://github.com/user-attachments/assets/b47a4a43-2788-4c11-89f1-80c43304a342" />

<img width="433" height="187" alt="image" src="https://github.com/user-attachments/assets/33519867-95b2-4917-a6bd-7e0d93a3eee5" />

<p>
We can use the command prompt to ping each machine from the other. And here we can see that both machines are able to send and receive packets. 
</p>

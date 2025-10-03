<h1>Active Directory: Domain Setup and User Administration</h1>
<h2>Description</h2>
Built and administered an Active Directory environment in Microsoft Azure by deploying a new domain, joining client machines, configuring Remote Desktop access for domain users, and applying user administration tasks such as account lockout policies, enabling/disabling accounts, and monitoring authentication logs. This project highlights experience with domain administration, user account management, and security policy enforcement.

<h2>Skills Used</h2>

- <b>Domain Administration</b>
- <b>User & Group Administration</b>

<h2>Languages Used</h2>

- <b>PowerShell</b>

<h2>Cloud Platform Used</h2>

- <b>Microsoft Azure</b>

<h2>Environments Used</h2>

- <b>Windows Server 2022</b> 
- <b>Windows 10 (22H2)</b>

<h2>Services Used</h2>

- <b>Virtual Machine (DC-1: Windows Server)</b> 
- <b>Virtual Machine (Client-1: Windows 10)</b>

<h2>Project walk-through:</h2>

<p align="center">
Open up Server Manager and select DC-1 as the designated server for this project:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 155531" src="https://github.com/user-attachments/assets/dc81e06a-e1b4-4ede-a9a1-a54294e1227b" />


<p align="center">
Install Active Directory Domain Services on DC-1 by using Server Manager:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 155531" src="https://github.com/user-attachments/assets/e8d109fd-cdfb-4d5f-8bcc-15157dcf7600" />

<p align="center">
Confirm adding the roles and features for Active Directory Domain Services:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 155714" src="https://github.com/user-attachments/assets/6310681a-0101-43cf-bb6a-b7c7c1d660e0" />

<p align="center">
Confirmation screen before installion:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 155826" src="https://github.com/user-attachments/assets/f4226a24-3c17-4427-aa67-a410975971c3" />

<p align="center">
Select the promote this server to a domain controller:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 160242" src="https://github.com/user-attachments/assets/0f1de596-2e4b-4317-bace-670af0cea2a9" />

<p align="center">
Create a new forest by specifying the domain name to mydomain.com
<img width="1919" height="1079" alt="Screenshot 2025-09-03 160328" src="https://github.com/user-attachments/assets/b8fe77ca-f8dd-4dad-8fc2-431d5f30ae72" />

<p align="center">
Select Domain Name System (DNS) server and Global Catalog (GC) to ensure the Domain Controller can provide name resolution, handle logon requests, and support directory searches across the forest, then create a DSRM password for recovery purposes.
<img width="1919" height="1079" alt="Screenshot 2025-09-03 160450" src="https://github.com/user-attachments/assets/f3e79f30-aea2-4fa2-8063-8e64aaa48769" />

<p align="center">
Verify the NetBIOS name is assgined to the correct name:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 160532" src="https://github.com/user-attachments/assets/b6d18a06-a321-4024-8ead-d33833d1d4fc" />

<p align="center">
Confirm DC-1 server passed all requirements to be promoted to a Domain Controller to begin installation:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 160759" src="https://github.com/user-attachments/assets/b136bf7f-45f3-497e-9a88-37e90b604a93" />

<h1>Active Directory: Domain Setup and User Administration</h1>
<h2>Description</h2>
Built and administered an Active Directory environment in Microsoft Azure by deploying a new domain, joining client machines, configuring Remote Desktop access for domain users, and applying user administration tasks such as account lockout policies, enabling/disabling accounts, and monitoring authentication logs. This project highlights experience with domain administration, user account management, and security policy enforcement.

<h2>Skills Used</h2>

- <b>Domain Administration</b>
- <b>User & Group Administration</b>
- <b>Security Log Monitoring</b>

<h2>Program Used</h2>

- <b>Command Prompt</b>

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
Create a new forest by specifying the domain name to mydomain.com:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 160328" src="https://github.com/user-attachments/assets/b8fe77ca-f8dd-4dad-8fc2-431d5f30ae72" />

<p align="center">
Select Domain Name System (DNS) server and Global Catalog (GC) to ensure the Domain Controller can provide name resolution, handle logon requests, and support directory searches across the forest, then create a DSRM password for recovery purposes:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 160450" src="https://github.com/user-attachments/assets/f3e79f30-aea2-4fa2-8063-8e64aaa48769" />

<p align="center">
Verify the NetBIOS name is assgined to the correct name:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 160532" src="https://github.com/user-attachments/assets/b6d18a06-a321-4024-8ead-d33833d1d4fc" />

<p align="center">
Confirm DC-1 server passed all requirements to be promoted to a Domain Controller to begin installation:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 160759" src="https://github.com/user-attachments/assets/b136bf7f-45f3-497e-9a88-37e90b604a93" />

<p align="center">
Remote login into DC-1 as mydomain.com\labuser:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 161641" src="https://github.com/user-attachments/assets/be5589e0-5bb9-4331-bcd0-97aea31ea342" />

<p align="center">
Open up Active Directory Users and Computers:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 162146" src="https://github.com/user-attachments/assets/727404a5-bc76-4b95-81a4-7f3dda210269" />

<p align="center">
Now select mydomain.com and create a new Organization Unit by using the drop down menu:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 162328" src="https://github.com/user-attachments/assets/6e9c4532-83df-44ca-9f14-615548ff81c1" />

<p align="center">
Create an Organization Unit called _EMPLOYEES:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 162452" src="https://github.com/user-attachments/assets/71c6bbc6-da9b-4572-a0a2-f31415935e13" />

<p align="center">
Create an Organization Unit called _ADMINS:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 162539" src="https://github.com/user-attachments/assets/bbe83a41-b8bf-45a8-9571-df4db84d2cfc" />

<p align="center">
Inside the _ADMINS folder create a user named Genesis Sierra with the user logon name genesis_admin:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 162813" src="https://github.com/user-attachments/assets/b402e87f-eaba-4d2a-b20d-8a23aeeb822b" />

<p align="center">
Open up the properties of the user Genesis Sierra:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 163034" src="https://github.com/user-attachments/assets/538fee7c-99e6-4dc8-8e00-8d0224cf534e" />

<p align="center">
Add Genesis Sierra to the Domain Admins Security Group:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 163651" src="https://github.com/user-attachments/assets/936a46cb-86aa-4ad4-b357-6d9bb22f1394" />

<p align="center">
Log into Client-1 using the domain account mydomain.com\genesis_admin to gain administrative privileges:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 164006" src="https://github.com/user-attachments/assets/5f46b073-a07c-4478-bf3f-8bed05e2d9a2" />

<p align="center">
Open up settings storage and go to system properties:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 164538" src="https://github.com/user-attachments/assets/da1c55a3-647b-4aa6-884d-aea44f540bf6" />

<p align="center">
Change the computers domain to mydomain.com:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 164648" src="https://github.com/user-attachments/assets/9bf5c274-b76e-4bd6-9928-dd450d7cf1d4" />

<p align="center">
Confirm the changes by inputting the administrative account mydomain.com\genesis_admin:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 164842" src="https://github.com/user-attachments/assets/57c55bd0-d39a-42c9-a1d3-e0ab39c22156" />

<p align="center">
Go back into DC-1 as mydomain.com\genesis_admin and open up Active Directory Users and Computers:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 170214" src="https://github.com/user-attachments/assets/6c23fa9f-690c-4b1e-b444-252bf1bb79e6" />

<p align="center">
Create one last Organization Unit and name it _CLIENTS:
<img width="1919" height="1079" alt="Screenshot 2025-09-03 170358" src="https://github.com/user-attachments/assets/f9540ec0-0089-4c3e-9b31-bf4b145d0a31" />

<p align="center">
After usign Powershell to create users go ahead and select a random user this one being moxa.pogo:
<img width="1919" height="1079" alt="Screenshot 2025-09-04 233336" src="https://github.com/user-attachments/assets/d4ac375a-197b-453c-84f4-707555167b58" />

<p align="center">
Log into DC-1 as the user mydomain.com\moxa.pogo:
<img width="1919" height="1079" alt="Screenshot 2025-09-04 233527" src="https://github.com/user-attachments/assets/95f7c733-cb04-443e-966a-c6ecf45b276d" />

<p align="center">
Open up gpmc.msc on the run command to launch Group Policy Management:
<img width="1919" height="1079" alt="Screenshot 2025-09-04 234106" src="https://github.com/user-attachments/assets/11aa9ede-7552-4868-90e0-80fae0e460d5" />

<p align="center">
Edit Default Domain Policy and it will open up the Group Policy Management Editor:
<img width="1919" height="1079" alt="Screenshot 2025-09-04 234505" src="https://github.com/user-attachments/assets/f724432c-1660-4b8c-bc6d-cbae47ee7b0f" />

<p align="center">
Scroll down to Account Lockout Policy:
<img width="1919" height="1079" alt="Screenshot 2025-09-04 234738" src="https://github.com/user-attachments/assets/4afd1a10-8955-4616-b58d-fcd8a7064aea" />

<p align="center">
Change the lockout duration to 30 minutes:
<img width="1919" height="1079" alt="Screenshot 2025-09-04 234826" src="https://github.com/user-attachments/assets/c1728726-a1a5-49ff-a4d5-15dd3cff2d80" />

<p align="center">
Accept the suggested values that Windows is suggesting to related policies:
<img width="1919" height="1079" alt="Screenshot 2025-09-04 234849" src="https://github.com/user-attachments/assets/39a1423f-674e-49b8-80cb-1118ca690a81" />

<p align="center">
Go into the settings of Default Domain Policy to verify the settings took into affect:
<img width="1919" height="1079" alt="Screenshot 2025-09-04 235148" src="https://github.com/user-attachments/assets/7c213cab-9ea3-4b04-a95a-46afec69825a" />

<p align="center">
Launch virtual machine Client-1 as the admin mydomain.com\genesis_admin:
<img width="1919" height="1079" alt="Screenshot 2025-09-04 235434" src="https://github.com/user-attachments/assets/cab12c9e-b690-44ca-838e-7314fa5157c2" />

<p align="center">
Once inside the virtual machine Client-1 open up the Command Prompt and input the command line gpupdate /force:
<img width="1919" height="1079" alt="Screenshot 2025-09-04 235634" src="https://github.com/user-attachments/assets/7eb4d62c-51e6-4128-985e-04ca5abb5430" />

<p align="center">
Screen will now show the computer policy update was successful:
<img width="1919" height="1079" alt="Screenshot 2025-09-04 235728" src="https://github.com/user-attachments/assets/8425e687-aff9-479a-ac99-3fed4e474551" />

<p align="center">
Launch the Command Prompt as Administrator and run the command gpresult /r:
<img width="1919" height="1079" alt="Screenshot 2025-09-04 235955" src="https://github.com/user-attachments/assets/57b5fd91-1e40-41f7-b8bb-33ca298f3c59" />

<p align="center">
Verify that the Default Domain Policy was actullay applied to the windows server machine (DC-1):
<img width="1919" height="1079" alt="Screenshot 2025-09-05 000109" src="https://github.com/user-attachments/assets/5422ffcd-a867-452f-b541-e1b47f85d9ed" />

<p align="center">
Attempt to connect to Client-1 as mydomain\moxa.pogo with an incorrect password repeatedly until the account lockout message appears:
<img width="1919" height="1079" alt="Screenshot 2025-09-05 000513" src="https://github.com/user-attachments/assets/7dcd70fd-fa12-49d1-b655-c223f27acf20" />

<p align="center">
Back in DC-1 as mydomain.com\genesis_admin locate the user moxa.pogo in Active Directory Users and Computers:
<img width="1919" height="1079" alt="Screenshot 2025-09-05 000641" src="https://github.com/user-attachments/assets/02273ba6-df49-47f8-a1c5-82e297cfcd93" />

<p align="center">
Go into account properties and click on Unlock account:
<img width="1919" height="1079" alt="Screenshot 2025-09-05 000820" src="https://github.com/user-attachments/assets/99442b90-c079-4a93-ab84-3ab36fbd630f" />

<p align="center">
Now you should be able to login to the user moxa.pogo normally with the correct password:
<img width="1919" height="1079" alt="Screenshot 2025-09-05 000908" src="https://github.com/user-attachments/assets/e1503458-cbdc-4752-9c64-e4a8ea9e7495" />

<p align="center">
Go back into the Active Directory Users and Computers as mydomain.com\genesis_admin and now disable the account moxa.pogo:
<img width="1919" height="1079" alt="Screenshot 2025-09-05 001224" src="https://github.com/user-attachments/assets/0ff7b322-f6ca-4f9e-988b-1c73f5abc2a4" />

<p align="center">
Try to launch Client-1 as mydomain\moxa.pogo again and witness the pop up error of the account being disabled:
<img width="1919" height="1079" alt="Screenshot 2025-09-05 001612" src="https://github.com/user-attachments/assets/69394c4f-cb8e-42fc-84e6-6ea95431a11c" />

<p align="center">
Now once again go back into DC-1 as mydomain.com\genesis_admin and re enable the account:
<img width="1919" height="1079" alt="Screenshot 2025-09-05 001710" src="https://github.com/user-attachments/assets/95674ac2-c705-4ad7-b608-8808766d18fb" />

<p align="center">
Open up Event Viewer in DC-1 with mydomain.com\genesis_admin to observe logs:
<img width="1919" height="1079" alt="Screenshot 2025-09-05 002104" src="https://github.com/user-attachments/assets/3ed6a338-015b-404c-ab9f-e1ffa2985c3e" />

<p align="center">
Now scoll down to windows logs security and locate moxa.pogo you should now see all logs assocated for this account with Event ID 4776 being selected as an audit Failure which indicates an invalid login attempt:
<img width="1919" height="1079" alt="Screenshot 2025-09-05 002328" src="https://github.com/user-attachments/assets/cdb934c9-1957-484a-8762-4ded19634315" />

<p align="center">
Click Find Next to view another log entry this one being Event ID 4634 which is an Audit Success indicating a successful logout of the account moxa.pogo:
<img width="1919" height="1079" alt="Screenshot 2025-09-05 002408" src="https://github.com/user-attachments/assets/4eedb412-a69b-4081-b53b-50efb5111062" />

<p align="center">
Now go back into Client-1 as mydomain\moxa.pogo and open up eventvwr.msc on the windows search bar:
<img width="1919" height="1079" alt="Screenshot 2025-09-05 002547" src="https://github.com/user-attachments/assets/5aca2414-3d6c-4488-9788-eb3d8c6098ab" />

<p align="center">
Run the windows program Event Viewer as an the adminstrater mydomain.com\genesis_admin:
<img width="1919" height="1079" alt="Screenshot 2025-09-05 003238" src="https://github.com/user-attachments/assets/ba28c9ee-e00b-4590-bb54-7afe0761c9c8" />

<p align="center">
Now you should be able to see the rest of the logs generated by Client-1 with this entry being Event ID 4625 which is a recorded failed logon attempt coming from the source network address 115.92.155.19:
<img width="1919" height="1079" alt="Screenshot 2025-09-05 003714" src="https://github.com/user-attachments/assets/d90e7be4-30f6-4a0c-9471-6e30c35d5055" />

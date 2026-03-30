 This project documents the step-by-step setup of a Windows Server 2019 virtual machine in VMware Workstation, configured as a Domain Controller. The walkthrough covers VM creation, OS installation, VMware Tools setup, network verification, and concludes with successfully joining a Windows 10 client to the domain.




<img width="1365" height="699" alt="Picture1" src="https://github.com/user-attachments/assets/c8b8025c-d4a1-4fb8-9c3b-607331b8558b" />


 We start by opening VMware Workstation and launching the wizard to create a new virtual machine.

<img width="1365" height="699" alt="image" src="https://github.com/user-attachments/assets/b2ae8402-e381-4909-965c-40b150de96d8" />
<img width="452" height="238" alt="image" src="https://github.com/user-attachments/assets/d13327de-c7b1-466b-957e-861703604b35" />
<img width="452" height="238" alt="image" src="https://github.com/user-attachments/assets/85a72230-3195-4015-9896-e13e84bcea06" />
<img width="452" height="238" alt="image" src="https://github.com/user-attachments/assets/94eb3959-c347-49f3-b941-ac1538267ab7" />
<img width="452" height="240" alt="image" src="https://github.com/user-attachments/assets/78d83a41-ea75-4a41-9220-02b9143d4c9d" />

 The wizard asks how we want to install Windows. We point it to the Windows Server 2019 ISO file we have downloaded, so it can use that to install the operating system.
<img width="452" height="231" alt="image" src="https://github.com/user-attachments/assets/6419abcb-841d-46b2-b7b1-5f67a199110e" />


Next, we give the virtual machine a name. We call it "Server 2019" and choose where on our computer we want to save it.

<img width="452" height="238" alt="image" src="https://github.com/user-attachments/assets/c81200de-e816-46cc-9d0d-78f21b3414db" />

Now we decide how much storage space to give it. The recommended amount is 60 GB, so we go with that. We also choose to split the storage into multiple files, which makes it easier to move the VM to another computer if needed.

<img width="452" height="239" alt="image" src="https://github.com/user-attachments/assets/d999d7e9-1eaf-4882-966a-65bae7f3a79d" />

The wizard shows us a summary of everything we've set up so far. We double-check the name, storage size, memory (2 GB), processors (2), and network settings (NAT), then click Finish to create the VM.




<img width="452" height="239" alt="image" src="https://github.com/user-attachments/assets/423a6c54-ceab-4709-a096-51bbe0423a47" />
<img width="452" height="239" alt="image" src="https://github.com/user-attachments/assets/b4340327-7ed2-4e18-9ef8-5ff318dad140" />
<img width="452" height="238" alt="image" src="https://github.com/user-attachments/assets/e02387af-1698-492e-94c5-c73d77ad4151" />
<img width="452" height="239" alt="image" src="https://github.com/user-attachments/assets/aa9bccfb-927c-4e90-bd25-94c7424be2ff" />
<img width="452" height="239" alt="image" src="https://github.com/user-attachments/assets/3aefad4e-9d85-4f1e-b96f-3f6f59dda2ba" />
Once created, we see the new Server 2019 VM sitting in VMware Workstation. It's powered off and ready for the next step. We open the settings for the VM and go to the CD/DVD section. Here, we attach the Windows Server 2019 ISO file so the VM can boot from it. We make sure the ISO is connected and set it to automatically connect whenever the VM powers on. This way, when we start the VM, it will immediately begin installing Windows Server.

<img width="452" height="233" alt="image" src="https://github.com/user-attachments/assets/0b906663-a0c8-4434-9aec-98ccd64e329c" />


Once we power on the virtual machine, the Windows Setup screen appears. We start by choosing our language, time format, and keyboard layout. Everything is set to English (United States), so we click Next to continue.

<img width="452" height="232" alt="image" src="https://github.com/user-attachments/assets/e4475aaf-81f8-403c-b003-7b106cc4a569" />

The next screen gives us a simple button that says "Install now." We click it to begin the installation process. There's also an option to repair the computer if needed, but we're doing a fresh install.

<img width="452" height="239" alt="image" src="https://github.com/user-attachments/assets/2804e731-28da-4432-825d-405061a6b7ba" />

Now we choose which version of Windows Server to install. We select "Windows Server 2019 Standard Evaluation (Desktop Experience)" because this gives us the full graphical interface, making it easier to work with. We click Next.
<img width="452" height="214" alt="image" src="https://github.com/user-attachments/assets/10714248-7cd2-4db9-a65f-266f519c3ae6" />

Microsoft shows us the license terms. We read through them, then check the box that says "I accept the license terms" and click Next.
<img width="452" height="213" alt="image" src="https://github.com/user-attachments/assets/90520778-fcd4-42cd-9f2d-31a5a60fe94e" />

We're asked what type of installation we want. Since we're setting up a new virtual machine with nothing on it yet, we choose "Custom: Install Windows only (advanced)." This lets us do a clean installation.
<img width="452" height="232" alt="image" src="https://github.com/user-attachments/assets/ae389b82-839e-4c08-b704-86060025c1a1" />

Now we see the hard drive we created earlier. It shows 60 GB of unallocated space. We select it and click Next. Windows will handle the rest.

<img width="452" height="238" alt="image" src="https://github.com/user-attachments/assets/e19a30fc-3153-41d9-8d1c-6cb3c22b5a54" />

Installation begins! Windows starts copying files and getting everything ready. We see the progress bar moving as it goes through the steps. All we have to do is wait.

<img width="452" height="254" alt="image" src="https://github.com/user-attachments/assets/22592cfd-a460-42c9-a615-e75c1b81fb51" />

After a few minutes, Windows finishes the initial setup and needs to restart. A countdown appears, and we can click "Restart now" to speed things up. The virtual machine will reboot and continue the installation process.

<img width="452" height="238" alt="image" src="https://github.com/user-attachments/assets/506367f0-725e-48a7-981d-0ee4fb8ed6db" />

After the installation completes and the server restarts, we're asked to set a password for the built-in Administrator account. We type in a strong password and then type it again to confirm. This will be used to log into the server.

<img width="452" height="240" alt="image" src="https://github.com/user-attachments/assets/60f678f2-1ea4-4db4-91a5-e14a3a21a26d" />
<img width="452" height="232" alt="image" src="https://github.com/user-attachments/assets/58d34fe7-95f9-4b66-b54b-6929bd891465" />
<img width="452" height="240" alt="image" src="https://github.com/user-attachments/assets/293807ae-ce7a-4691-b19d-2b5619b2b273" />
<img width="452" height="232" alt="image" src="https://github.com/user-attachments/assets/ea3ba349-4bc9-4c2e-a34f-fd0a2ef19849" />


After unlocking, we're prompted to enter the Administrator password we just created. We type it in and press Enter to log in.

<img width="452" height="239" alt="image" src="https://github.com/user-attachments/assets/c493bc3c-a013-48c5-8fe0-b37d07252095" />

<img width="452" height="254" alt="image" src="https://github.com/user-attachments/assets/95dfe299-16e1-4054-88dd-de81b62228d8" />










Windows Server loads up and greets us with Server Manager, which opens automatically. This is the main dashboard where we can manage the server, add roles and features, and configure settings. It shows that we have one server set up.
<img width="452" height="236" alt="image" src="https://github.com/user-attachments/assets/b7e22ec1-0f63-42a9-9a51-b89ddc1ce29d" />

Looking at Server Manager, we see the local server listed along with its manageability status. We also notice a message at the bottom reminding us that VMware Tools isn't installed yet, which will help improve performance and functionality.To install VMware Tools, we open File Explorer by clicking the folder icon on the taskbar. We see the DVD drive labeled "VMware Tools." This virtual disc contains the tools we need to install.

<img width="452" height="232" alt="image" src="https://github.com/user-attachments/assets/77738510-537d-403d-8735-30151b90e1e2" />

To install VMware Tools, we open File Explorer by clicking the folder icon on the taskbar. We see the DVD drive labeled "VMware Tools." This virtual disc contains the tools we need to install.
<img width="452" height="214" alt="image" src="https://github.com/user-attachments/assets/6c3e3e31-01e8-4166-8954-08fca8668aa7" />

Inside the DVD drive, we find the VMware Tools setup files. We double-click the setup executable to begin the installation.
<img width="452" height="232" alt="image" src="https://github.com/user-attachments/assets/119d5662-cab5-43c8-aeb2-98e7ae75d429" />
<img width="452" height="230" alt="image" src="https://github.com/user-attachments/assets/6f1197dd-5598-4ee4-b78b-8cf24fcf305c" />


The VMware Tools installation wizard opens. We click Next to get started.
<img width="452" height="231" alt="image" src="https://github.com/user-attachments/assets/7894f2c1-ec2b-43ed-9f84-3e859e55af81" />

The wizard asks what type of installation we want. We choose "Typical," which installs everything we need for running this virtual machine with VMware Workstation. We click Next.
<img width="452" height="232" alt="image" src="https://github.com/user-attachments/assets/723a64f6-2b90-41c4-aef3-975b97181ea4" />

 We're now ready to install. We click Install to begin the process.
<img width="452" height="240" alt="image" src="https://github.com/user-attachments/assets/f1dafb37-4514-4629-b07c-7a033d5a4452" />

The installation runs. We see the status messages as it copies files and starts services. This only takes a minute or two.
<img width="452" height="231" alt="image" src="https://github.com/user-attachments/assets/d2f05fa8-f367-4e6a-9eee-52e651b272dc" />

Once the installation finishes, we click Finish to complete the wizard.

<img width="452" height="231" alt="image" src="https://github.com/user-attachments/assets/74ef58a1-c6c4-49cb-a4d6-bd10f4d98a17" />

A message appears asking us to restart the computer for the changes to take effect. We click Yes to restart now.
After the restart, VMware Tools is fully installed, and the server is ready to use. The display will be smoother, the mouse will move seamlessly between the host and guest, and overall performance will be improved. 








Phase 1: Install Active Directory (Server Side)


<img width="452" height="236" alt="image" src="https://github.com/user-attachments/assets/c5c41e80-753e-4676-9c1c-19e6242ad60d" />

<img width="452" height="247" alt="image" src="https://github.com/user-attachments/assets/21af5c7f-e965-4d4a-a8ae-b2ff05418d33" />

<img width="452" height="235" alt="image" src="https://github.com/user-attachments/assets/fd5bc4b3-45ce-41b0-8c04-db40edb1e204" />
















Active Directory Setup
1.Set a Static IP:
On Server 2019: Right-click the network icon > Open Network & Internet settings > Change adapter options.
<img width="452" height="248" alt="image" src="https://github.com/user-attachments/assets/e4dbf1fc-daff-454e-8769-d91716c7444b" />
<img width="452" height="248" alt="image" src="https://github.com/user-attachments/assets/e6ae27e4-0edd-4cba-abbf-7f669e729ec4" />








Right-click your Ethernet adapter > Properties > IPv4 > Properties.

<img width="452" height="251" alt="image" src="https://github.com/user-attachments/assets/e61aff71-ebd0-4830-b75c-435c8d491561" />
<img width="452" height="250" alt="image" src="https://github.com/user-attachments/assets/b5a5dd0f-d101-41df-8176-760be89933cc" />








Set a static IP 

<img width="452" height="236" alt="image" src="https://github.com/user-attachments/assets/2092ab7e-6ce2-4e04-bede-c61d5ad1717c" />
<img width="452" height="236" alt="image" src="https://github.com/user-attachments/assets/a435f8c3-1fc1-4dcc-8d69-cd70a426e976" />








Set the Preferred DNS server to 127.0.0.1 (the server itself).

<img width="452" height="236" alt="image" src="https://github.com/user-attachments/assets/c9e03ee6-a614-4709-a268-989791a3c9b0" />
<img width="452" height="220" alt="image" src="https://github.com/user-attachments/assets/1ab740c2-cd96-473d-8636-bb12a2f2b270" />











1.Add the Role:
Open Server Manager > Manage > Add Roles and Features.
<img width="452" height="221" alt="image" src="https://github.com/user-attachments/assets/bdcf4d8b-3616-4a66-b4df-bc86a3b0023a" />
<img width="452" height="236" alt="image" src="https://github.com/user-attachments/assets/246202fb-f626-4691-9862-5c1a6843488e" />
<img width="452" height="237" alt="image" src="https://github.com/user-attachments/assets/c5c29ca8-c645-443f-8164-ab02209ca619" />




Click Next until you reach Server Roles. Check Active Directory Domain Services.

<img width="452" height="236" alt="image" src="https://github.com/user-attachments/assets/9573846c-8b89-4389-bd88-97acd1a852a0" />







Click Add Features when prompted, then Next until Install.

<img width="452" height="220" alt="image" src="https://github.com/user-attachments/assets/cac0d947-a5cb-4229-82ea-f9ae9d92757e" />
<img width="452" height="236" alt="image" src="https://github.com/user-attachments/assets/95d74c22-2297-465d-819e-44a4677f2684" />
<img width="452" height="236" alt="image" src="https://github.com/user-attachments/assets/49c312f8-4842-4782-b68e-0f0edd910edb" />
<img width="452" height="237" alt="image" src="https://github.com/user-attachments/assets/963e0e63-bf83-4a07-8919-0a592856f5d0" />
<img width="452" height="232" alt="image" src="https://github.com/user-attachments/assets/e65b0e56-f5a8-44cb-a8ce-e69af3b0bc86" />
<img width="452" height="234" alt="image" src="https://github.com/user-attachments/assets/231ddffb-02f7-46e8-8ae0-db578cc06047" />
<img width="452" height="237" alt="image" src="https://github.com/user-attachments/assets/5a683324-0185-4603-8bdd-7841aa3fcd11" />






1.Promote to Domain Controller:
Once installed, click the Flag icon (Notifications) in Server Manager and select Promote this server to a domain controller.

<img width="452" height="237" alt="image" src="https://github.com/user-attachments/assets/f5ede339-c66e-4f75-9fe6-e40950595086" />
<img width="452" height="227" alt="image" src="https://github.com/user-attachments/assets/8656b2c5-bcae-463b-9d2d-a9ee77bc8eb0" />
<img width="452" height="227" alt="image" src="https://github.com/user-attachments/assets/f38cd76c-2156-4889-a148-3b89d5146dd6" />













Select Add a new forest. Root domain name: dumebi.local.

<img width="452" height="212" alt="image" src="https://github.com/user-attachments/assets/c16ca24c-a555-4025-a7b3-4d503daa8fd5" />
<img width="452" height="237" alt="image" src="https://github.com/user-attachments/assets/3d462e85-fc96-4e19-bd5e-cfdd604d4b63" />









Set a DSRM Password (keep this safe) and click Next through the defaults.
<img width="452" height="237" alt="image" src="https://github.com/user-attachments/assets/4858dbe5-cf8b-4167-a55e-81a7e7ac4a87" />
<img width="452" height="249" alt="image" src="https://github.com/user-attachments/assets/e824910f-5548-40df-bd1a-7500b4ac2e93" />
<img width="452" height="236" alt="image" src="https://github.com/user-attachments/assets/a18343a3-b757-4f19-b228-0f77d81743c0" />
<img width="452" height="220" alt="image" src="https://github.com/user-attachments/assets/271479c3-c7f8-4523-8752-f050aa825950" />
<img width="452" height="237" alt="image" src="https://github.com/user-attachments/assets/fa7bdb75-5797-4844-9251-e120b038261d" />
<img width="452" height="224" alt="image" src="https://github.com/user-attachments/assets/2b8c95d9-463a-4734-a904-9937b56685c0" />

















Click Install. The server will reboot. Log back in as DUMEBI\Administrator.
<img width="452" height="235" alt="image" src="https://github.com/user-attachments/assets/ece93748-9a88-44f6-8542-2f4205d96bcf" />
<img width="452" height="220" alt="image" src="https://github.com/user-attachments/assets/a3b46ffe-56fa-41c8-ab65-b263d1db19b0" />

<img width="452" height="249" alt="image" src="https://github.com/user-attachments/assets/8d1bf838-0225-4798-acbc-04fd618dbd57" />

<img width="452" height="240" alt="image" src="https://github.com/user-attachments/assets/2586e4b9-9e3b-455d-88e7-56ef72ba8874" />

<img width="452" height="240" alt="image" src="https://github.com/user-attachments/assets/73070492-fcb8-466b-8ca0-ff0f7a04d0f2" />
<img width="452" height="240" alt="image" src="https://github.com/user-attachments/assets/bdb80023-d70f-42fd-9582-50bae6f29fce" />



Phase 2: Create the "Sales" Environment
1.Create the OU (Organizational Unit):
In Server Manager, go to Tools > Active Directory Users and Computers.


<img width="452" height="235" alt="image" src="https://github.com/user-attachments/assets/2f4170cd-578c-400e-88a0-aabde1ab14b7" />
<img width="452" height="238" alt="image" src="https://github.com/user-attachments/assets/66c4f53a-5d27-483c-91c5-dbf5919c12c5" />


Right-click dumebi.local > New > Organizational Unit. Name it Sales.
<img width="452" height="235" alt="image" src="https://github.com/user-attachments/assets/d21516bd-dca6-47f9-9551-2a825e361fde" />
<img width="452" height="221" alt="image" src="https://github.com/user-attachments/assets/4307600e-6252-41bd-b32e-f9e3b325e528" />
<img width="452" height="240" alt="image" src="https://github.com/user-attachments/assets/02d4ad50-fbe0-4e28-8cb3-5ae9e25ef54a" />
<img width="452" height="222" alt="image" src="https://github.com/user-attachments/assets/50b65c65-8a9e-4ece-b8c6-1bae5976d0b8" />




1.Create the User:
Right-click your new Sales OU > New > User.
<img width="452" height="237" alt="image" src="https://github.com/user-attachments/assets/f6531e50-bdf8-4291-8069-62f437aac1db" />
<img width="452" height="237" alt="image" src="https://github.com/user-attachments/assets/b70e5f87-e272-4fae-aa60-354cd18ee384" />


First Name: dumebi, Login Name: chukwuma. Click Next.

<img width="452" height="228" alt="image" src="https://github.com/user-attachments/assets/9ccc6ec5-1b3a-4020-b8f6-2edab3e60e8a" />








Set a password (e.g., P@ssword123) and uncheck "User must change password at next logon" for this lab.

<img width="452" height="237" alt="image" src="https://github.com/user-attachments/assets/adba1c7c-0b45-46c7-be3b-6264876a7a80" />
<img width="452" height="228" alt="image" src="https://github.com/user-attachments/assets/68cc9cd5-3780-4723-91ab-9e9232e9ebd9" />
<img width="452" height="212" alt="image" src="https://github.com/user-attachments/assets/c112ba8b-df4a-4ec4-960b-433c68baf6a2" />
<img width="452" height="212" alt="image" src="https://github.com/user-attachments/assets/a0edf498-650e-4639-b1ec-5ace34c00340" />
<img width="452" height="235" alt="image" src="https://github.com/user-attachments/assets/a3effbf2-e17c-4e60-b394-36756dec2c63" />





Phase 3: Connect the Windows 10 VM
1.Set Client DNS:
On your Windows 10 VM, go to Network Properties (IPv4).

<img width="452" height="237" alt="image" src="https://github.com/user-attachments/assets/d9854f2c-68eb-4931-a2db-389cf702f1a4" />
<img width="452" height="237" alt="image" src="https://github.com/user-attachments/assets/3dd4390c-c736-4924-a2ad-3bcf2bce1e2b" />
<img width="452" height="237" alt="image" src="https://github.com/user-attachments/assets/fd95df54-2c8b-4a48-8345-10b3d1b7b0df" />
<img width="452" height="236" alt="image" src="https://github.com/user-attachments/assets/aceafcd7-1469-4cd1-869e-5624dcf46ba4" />
<img width="452" height="235" alt="image" src="https://github.com/user-attachments/assets/1af4ed00-3467-4c84-892e-71f7bc4cea15" />






Set the Preferred DNS server to the IP of your Server .Leave the IP settings as DHCP or set a static one in the same range ( 

<img width="452" height="222" alt="image" src="https://github.com/user-attachments/assets/c23fdba3-abb4-48d4-a8ce-a4a40edc4913" />


1.Join the Domain:
Click Start, type sysdm.cpl, and press Enter.

Click Change... > Select Domain > Type dumebi.local.











oEnter the Server's Admin credentials (DUMEBI\Administrator and your password).



oRestart the VM.


Login as Dumebi:
oOn the login screen, select Other User.







oLog in as dumebi\dumebi.chukwuma.







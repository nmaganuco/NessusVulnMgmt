<h1>Nessus Vulnerability Management Lab</h1>

<h2>Description</h2>
Project consists of 
<br />


<h2>Utilities Used</h2>

- <b>Nessus Essentials</b> 
- <b>Command Prompt</b> 


<h2>Environments Used </h2>

- <b>Windows 10</b>
- <b>VMWare</b>

<h2>Links</h2>

- <b>VMWare Workstation:</b>https://www.vmware.com/products/workstation-player/workstation-player-evaluation.html
- <b>Windows 10 ISO:</b> https://www.microsoft.com/en-us/evalcenter/evaluate-windows-10-enterprise
- <b>Nessus Essentials:</b> https://www.tenable.com/products/nessus/nessus-essentials




<h2>Lab walk-through:</h2>

<p align="center">
<h2> Downloading and Installing VMWare Workstation </h2> 
  <b> Head to the VMWare Workstation website and select "Try Workstation 17 Player For Windows." Install VMWare with the defualt configurations. </b>
<br />
<br />
<img src="https://i.imgur.com/OOC4jKg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<p align="center">
<h2> Downloading Nessus Essentials </h2> 
  <b> Go to the Nessus Essentials website and fill out your name and email address. You will be sent an activation code to use Nessus. </b>
<br />
<br />
<img src="https://i.imgur.com/uuEp8WA.png"/>
<br />

<b> Once you recieve the email, press the link to download Nessus. </b>


<b> Select the first option, which should be "Nessus", and it should automatically select the correct version and platform. Download Nessus and complete the installation wizard. </b>
<br />
<br />
<img src="https://i.imgur.com/eF1Nimx.png"/>
<br />
<br />


<b> Once the installation is completed, a page will be appear. I recommend saving the URL for future references.</b>
<br />
<br />
<img src="https://i.imgur.com/6ij6ORx.png"/>
<br />
<br />

<b> Select Connect via SSL > Advanced > Accept the risk and continue/Proceed. </b>

<b> Select Continue > Register for Nessus Essentials > Skip. Refer back to the email you recieved from Nessus and paste the Activation Code. </b>

<b> Create a Username and Password for Nessus. Make sure to write this down or properly save this information.</b>
<br />
<br />
<img src="https://i.imgur.com/et8aCtw.png"/>
<br />
<br />

<b> Nessus will then begin installing. This installation will take a while.</b>
<br />
<br />
<img src="https://i.imgur.com/Qqq0Z9l.png"/>
<br />
<br />

<b> Once the installation is complete, the Nessus Essentials web application will appear. Check the top right of your page and make sure that all plugins are done compliling to ensure that Nessus functionality is not limited.</b>
<br />
<br />
<img src="https://i.imgur.com/NDDgi9f.png"/>
<br />
<br />

<p align="center">
<h2> Downloading Windows 10 </h2> 
  <b> Click on the Windows 10 link and select "Download the ISO - Enterprise." Fill out the form and select the 64-bit edition. </b>
<br />
<br />
<img src="https://i.imgur.com/uzOKTdo.png"/>
<br />
<br />

<b> On VMWare, select "Create a new virtual machine." </b>

<b> Browse and select the recently downloaded Windows 10 Iso file. </b>

<b> Do not worry about the product key, just press Next. </b>

<b> You can leave the default disk capacity. </b>

<b> Select "Customize Hardware." Change the NAT to "Bridged." This will put the Windows 10 virtual machine on the same network as your physical computer. </b>
<br />
<br />
<img src="https://i.imgur.com/MMBkmGl.png"/>
<br />
<br />

<b> Make sure to uncheck "Power on this virtual machine after creation." </b>

<b> Select Close and then Finish.</b>

<b> Click "Edit virtual machine settings" and remove the Floppy drive. </b>

<b> You can now start the Windows 10 virtual machine. Make sure to press a key when it launches to boot into the ISO. </b>

<b> You will be presented with the Windows Setup. </b>
<br />
<br />
<img src="https://i.imgur.com/sHJ01jQ.png"/>
<br />
<br />

<b> Select Next > Install Now > Agree to the license terms > Next > Custom > Next.</b>

<b> Windows will now begin installing and will restart when completed.</b>

<b> Select your Region and Keyboard layout.</b>

<b> Press "Domain join instead" and add a name for the user, as well as a password. </b>
<br />
<br />
<img src="https://i.imgur.com/dZFOXKB.png"/>
<br />
<br />

<b> Fill out the security questions. </b> 

<b> Choose your preferred privacy settings. (preferably no) </b> 

<b> Select Accept. </b>

<b> Select Not Now for Cortana. </b>

<p align="center">
<h2> Ensuring Connectivity With The Virtual Windows 10 </h2> 
<b> Open the Command prompt by searching "CMD."  </b>
<br />
<br />
<img src="https://i.imgur.com/wRZU7Fc.png"/>
<br />
<br />

<b> Type "ipconfig" to get the IPv4 address of your virtual Windows 10. </b>

<b> Open the command prompt on your physical pc and type "ping <IPv4 Address>." Make sure to put the IPv4 address of your virtual machine. </b>
  
<b> As we can see, your physical pc can't establish a connection with your virtual machine. We can tell because the pings are timing out. This is due to the Windows Firewall blocking network connections. </b>
<br />
<br />
![Failed Ping](https://github.com/nmaganuco/NessusVulnMgmt/assets/136499884/e73b179e-88a3-450e-b164-97e5241b635b)
<br />
<br />

<b> For the purposes of this lab, we are going to disable Windows Firewall. Do not do this with your physical pc as it could be dangerous. </b>
  
<b> Search "wf.msc" and it will bring you to the Windows Defender Firewall. </b>
  
<b> Click on "Windows Defender Firewall Properties" and select "Off" for all three profiles. </b>
<br />
<br />
![Firewall Off](https://github.com/nmaganuco/NessusVulnMgmt/assets/136499884/b0e57c0a-43df-430c-8468-a68e664a8ef6)
<br />
<br />
  
<b> Go back to the command prompt on your physical pc and ping the virtual machine again. This time, we should see a reply from our Windows 10. </b>
<br />
<br />
![Good Pings](https://github.com/nmaganuco/NessusVulnMgmt/assets/136499884/42366dec-9ac2-4d23-a9a3-a7189639745d)
<br />
<br />
  
<p align="center">
<h2> Creating A New Scan On Nessus </h2> 
<b> Return to your Nessus web app and select "New Scan" > "Basic Network Scan." </b>
<br />
<br />
<img src="https://i.imgur.com/MIUf199.png"/>
<br />
<br />
  
<b> Type a name for the scan and the targeted IP Address (VM IP Address). Then press "Save." </b>
<br />
<br />
![Animation1](https://github.com/nmaganuco/NessusVulnMgmt/assets/136499884/97e7bf21-5548-4870-adf7-804a1f99fba6)
<br />
<br />
  
<b> Select the launch button (play symbol) on the right of your scan to begin scanning the targeted machine. Wait for Nessus to finish scanning. </b>
<br />
<br />
![Progress](https://github.com/nmaganuco/NessusVulnMgmt/assets/136499884/ead12fb1-1450-47b9-a5d9-b480572e9467)
<br />
<br />  
  
<b> Once the scan is complete, click on it and go to "Vulnerabilities." From here, we can see vulnerabilities that Nessus discovered. It discovered 34 vulnerabilities, in which 1 is classified as "Medium" and 33 as "Info." Info means that it isn't necessarily a vulnerability, but it should be something that you are made aware of.  </b>
<br />
<br />
![Info](https://github.com/nmaganuco/NessusVulnMgmt/assets/136499884/9fc8a21c-82ec-46b0-abd0-0633100add94)
<br />
<br />  
  
<b> Looking at the medium vulnerability, we can see that Nessus discovered SMB Signing is not required. Nessus will offer a description of the vulnerability, as well as a solutuion to remediate the vulnerability and other resources for further information.  </b>
<br />
<br />
![Animation12](https://github.com/nmaganuco/NessusVulnMgmt/assets/136499884/f98fcc05-ae67-4d3b-9ad8-8860132a9bb3)
<br />
<br />  
  
<p align="center">
<h2> Configuring The Virtual Machine For Credentialed Scans</h2> 
<b> We are now going to configure the virtual machine to accept authenticated scans and provide credentials to Nessus. Begin by returning to the virtual machine and search for "services.msc." </b>
<br />
<br />
<img src="https://i.imgur.com/xlQEmEU.png"/>
<br />
<br />  

<b> Find the "Remote Registry" service, change the Startup Type to Automatic. Press Apply > Start > OK.  </b>
<br />
<br />
![Animation122](https://github.com/nmaganuco/NessusVulnMgmt/assets/136499884/f62ac8ca-42bc-4e2d-80ac-7dad3f9880a1)
<br />
<br /> 
  
<b> Enabling Remote Registry allows Nessus to look through the Registry and look for vulnerabilities such as deprecated cipher suites or insecure configurations. </b>

<b> Exit out of the Services page and search for "User Account Control Settings." Set the setting to "Never Notify."  </b>
<br />
<br />
![Notication settings](https://github.com/nmaganuco/NessusVulnMgmt/assets/136499884/14d15165-f59c-4750-b888-e5325a80b7c4)
<br />
<br />   

<b> Search for "Registry Editor." We will be adding a key that will allow Nessus to connect by futher disabling user account controls. </b>
  
<b> Browse to Local Machine > Software > Microsoft > Windows > Current Version > Policies > System. </b>
<br />
<br />
![Registry](https://github.com/nmaganuco/NessusVulnMgmt/assets/136499884/0c47d4e3-20a1-42bd-8219-dd4ed6758dec)
<br />
<br />   

<b> Right-click on an empty white space and select New > DWORD (32-bit) value. Name it "LocalAccountTokenFilterPolicy." Double click it and set the value to 1.  </b>
<br />
<br />
![Editor](https://github.com/nmaganuco/NessusVulnMgmt/assets/136499884/e6faa61f-628f-46bc-bf95-a5bfcd6fd601)
<br />
<br />     

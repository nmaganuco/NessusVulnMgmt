<h1>Nessus Vulnerability Management Lab</h1>

<h2>Description</h2>
Project consists of 
<br />


<h2>Utilities Used</h2>

- <b>Nessus Essentials</b> 


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

<b> Fill out the security questions </b> 

<b> Choose your preferred privacy settings (preferably no) </b> 

<b> Select Accept </b>

<b> Select Not Now for Cortana </b>

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable Internet Information Services (IIS)
- Install Web Platform Installer 
- Install MYSQL 
- Install Microsoft Visual C++ 2008 Redistributable Package and PHP Manager 1.5.0 
- Set Permissions and Install osTicket 

<h2>Installation Steps</h2>

<p>
To install osTicket on a virtual machine, enable Internet Information Services (IIS) in the Windows features. Start by pressing the Windows button on your keyboard and typing "Windows features." Then select Turn Windows features on or off from the menu.
</p>
<br />
<p>
<img src="https://i.imgur.com/tJcRxeS.png" height="70%" width="70%" alt="Windows Features Search"/>
</p>
<br />

<p>
Find and select Internet Information Services from the Turn Windows Features on or off menu, then click the OK button.
</p>
<br />
<p>
<img src="https://i.imgur.com/Sv2WgiI.png" height="70%" width="70%" alt="Windows Features Menu"/>
</p>
<br />

<p>
Allow for the installation of Internet Information Services. 
<br />
<p>
<img src="https://i.imgur.com/R4ge2PR.png" height="70%" width="70%" alt="Applying Changes"/>
</p>
<br />

<p>
Once installed, go to Windows Administrative Tools to find the Internet Information Services (IIS) Manager.
</p>
<br />
<p>
<img src="https://i.imgur.com/LrNUJp9.png" height="70%" width="70%" alt="Windows Administrative Tools"/>
</p>
<br />

<p>
Now you can work on adding the prerequisites (PHP Version: 7.3 and MySQL Database: 5.0+). To do this, you will need to download and install the Web Platform Installer Extension. You can find the download for the Web Platform Installer on Microsoft.com.
</p>
<br />
<p>
<img src="https://i.imgur.com/dfgaKNT.png" height="90%" width="90%" alt="Download Page"/>
</p>
<br />

<p>
Install Web Platform Installer.
</p>
<br />
<p>
<img src="https://i.imgur.com/yxtOLfG.png" height="70%" width="70%" alt="Install Page Web Platfrom Installer"/>
</p>
<br />

<p>
After the installation, open the Web Platform Installer and search for MySQL and add version 5.5.
</p>
<br />
<p>
<img src="https://i.imgur.com/7bXxHJw.png" height="70%" width="70%" alt="MySQL Search"/>
</p>
<br />

<p>
Next, search for PHP and add each version of PHP leading up to 7.3. Once you have selected all the necessary prerequisites, press install.
</p>
<br />
<p>
<img src="https://i.imgur.com/rtMV3PE.png" height="70%" width="70%" alt="PHP Search"/>
</p>
<br />

<p>
The installer will prompt you to create a password for the database admin account "root." Make sure to write down the password.
</p>
<br />
<p>
<img src="https://i.imgur.com/Gtb66Ge.png" height="70%" width="70%" alt="Installer Prompt"/>
</p>
<br />

<p>
After completing the prompts, wait for the installation to complete.
</p>
<br />
<p>
<img src="https://i.imgur.com/wbTajNN.png" height="70%" width="70%" alt="Install Page"/>
</p>
<br />

<p>
Once completed, you may find that a few of the selected products did not install successfully. You will need to download the products that were unable to be installed manually. For example, even though the Microsoft Visual C++ 2008 Redistributable Package and PHP Manager 1.5.0 are available to be downloaded through the Web Platform Installer, they may not be able to be successfully installed. You can find the download for the Microsoft Visual C++ 2008 Redistributable Package and PHP Manager 1.5.0 by searching on Google.
</p>
<br />
<p>
<img src="https://i.imgur.com/JigNgq2.png" height="70%" width="70%" alt="Unsuccessfully Install List"/>
</p>
<br />

<p>
After you have installed all the prerequisites, you can begin downloading and installing osTicket. The open-source download for osTicket can be found at the osTicket website.
</p>
<br />
<p>
<img src="https://i.imgur.com/WHtClsV.png" height="70%" width="70%" alt="osTicket Download Website"/>
</p>
<br />

<p>
Once you have the osTicket files downloaded, you will need to extract them by going to your downloads folder, selecting the osTicket download folder, and right clicking to select extract all.
</p>
<br />
<p>
<img src="https://i.imgur.com/625rHib.png" height="70%" width="70%" alt="Extract osTicket Files"/>
</p>
<br />

<p>
When this is complete, go back to the downloads folder and open the osTicket folder. Then extract and copy the "upload" folder into c:\inetpub\wwwroot and rename the "upload" folder to "osTicket".
</p>
<br />
<p>
<img src="https://i.imgur.com/5hhQznj.png" height="70%" width="70%" alt="Rename Upload Folder"/>
</p>
<br />

<p>
Run Internet Information Services (IIS) as an administrator and refresh the page. After, go to the "Sites" folder, followed by "Default Web Site," and select osTicket. Once osTicket is selected on the right, click "Browse *:80."
</p>
<br />
<p>
<img src="https://i.imgur.com/9CT1bZS.png" height="70%" width="70%" alt="Browse 80"/>
</p>
<br />

<p>
You will be taken to the osTicket installer page, where you will find that a few of the recommended extensions are not enabled. These extensions will need to be enabled by using the PHP Manager in IIS.
</p>
<br />
<p>
<img src="https://i.imgur.com/SNqrHnD.png" height="70%" width="70%" alt="osTicket Insaller Page"/>
</p>
<br />

<p>
Go back to IIS and double-click on PHP Manager and select "Enable or disable an extension," then enable php_imap.dll, php_intl.dll, and php_opcache.dll.
</p>
<br />
<p>
<img src="https://i.imgur.com/1eb7rvN.png" height="70%" width="70%" alt="PHP Manager"/>
</p>
<br />

<p>
Refresh the osTicket site in your browser and observe the changes.
</p>
<br />
<p>
<img src="https://i.imgur.com/ZBiWPLj.png" height="70%" width="70%" alt="Refresh osTicket"/>
</p>
<br />

<p>
Rename the sample file from C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to C:\inetpub\wwwroot\osTicket\include\ost-config.php.
</p>
<br />
<p>
<img src="https://i.imgur.com/nzoNXHD.png" height="70%" width="70%" alt="Rename Sample File"/>
</p>
<br />

<p>
You will need to assign permissions to ost-config.php by right-clicking the file and selecting Properties, then going to Security and selecting Advanced. Once in the advanced settings, click on Disable inheritance and select Remove All from the prompt.
</p>
<br />
<p>
<img src="https://i.imgur.com/P3m1lPn.png" height="70%" width="70%" alt="Assign Permissions"/>
</p>
<br />

<p>
Then you will need to add your own permissions by clicking on "Add," followed by "selecting a principal," and entering a group name for users in the box. You will now be able to click on "full control," which will give the group access to osTicket.
</p>
<br />
<p>
<img src="https://i.imgur.com/HjWSLyb.png" height="70%" width="70%" alt="Adding Group"/>
</p>
<br />

<p>
Now you can continue setting up osTicket in the browser and start filling out the form. 
</p>
<br />
<p>
<img src="https://i.imgur.com/2L4gogG.png" height="70%" width="70%" alt="osTicket Install Form"/>
</p>
<br />

<p>
Once you have entered a name for the help desk and a default email address and filled out the admin user information, you can download and install HeidiSQL. This is required to set up a database.
</p>
<br />
<p>
<img src="https://i.imgur.com/nMD6dlC.png" height="70%" width="70%" alt="HeidiSQL Install"/>
</p>
<br />

<p>
After HeidiSQL is installed, create a new session (please note you will need the password you set up for root earlier), then connect to the new session, and create a new database called "osTicket."
</p>
<br />
<p>
<img src="https://i.imgur.com/sJFBDU2.png" height="70%" width="70%" alt="New Database"/>
</p>
<br />

<p>
You can now continue setting up osTicket in the browser, and once the form is filled out, you can click "Install Now!" If installation was successful, you will be taken to a page where you will find links to your help desk and staff control panel.
</p>
<br />
<p>
<img src="https://i.imgur.com/peNtlHo.png" height="70%" width="70%" alt="osTicket Install Complete"/>
</p>
<br />

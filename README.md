
<h1>Active Directory and Access Control Administration Lab</h1>

<h2>Description</h2>
This project demonstrates hands-on experience administering Active Directory with a focus on user lifecycle management, role-based access control (RBAC), and access troubleshooting in a service desk environment.

<h2>Languages and Utilities Used</h2>
- <b>Active Directory Users and Computers (ADUC), Group Policy Management (GPMC), Windows Server, Windows 10/11</b> 
  

<h2>Environments Used </h2>

- <b> Windows Server (Domain Controller) </b>
- <b> Windows 10/11 Client </b>
- <b> Active Directory Users and Computers (ADUC) </b>
- <b> Group Policy Management (GPMC) </b>

<h2>Create Organizational Unit(OUs)<h2>
Phase 1:I am going to create Dffrent OUs so we could use later in this lab which are IT_Users,Finance_users,HR_Users,Disabled_Users,Service_Accounts.
We first enter in Active Directory<br/>
<img src="https://i.imgur.com/PqvBUKN.png" height="80%" width="80%" alt="VM launch"/>
<br />
<br />
Phase 2:Now we click on new object organizational unit and i will start with IT_users and we will do the same process as we did to create the first OUs to the rest of the OUs we have to make,and aslo we make the any OUs we make is under mydomain.com: <br/>
<img src="https://i.imgur.com/Ema29Go.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Phase 3:Now we have made all the OUs reguired for the next step of the lab: <br/>
<img src="https://i.imgur.com/w3PDfYx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Phase 4: we are creating our users so we are going to click on users then at the top we are going to click on create a new user in the current container and it will show this page where we are going to fill in the user information which we are going to make all our users :  <br/>
<img src="https://i.imgur.com/4wrZWBZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br /> 
<br />
Now we are going to get to this screeen after we are done with his basic information it will ask us to set up a password for the user which are going to set up a tempory password and clikc on user must change password at next logon then we are done for that part but we did that so when we go to login in the client VM we should be prompted to change the password because us knowing the user password is not good security practice so in real life we are also going to ask the user to set his own password. :  <br/>
<img src="https://i.imgur.com/TjGdwt4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Here we are going to take each user and put them thier respective OUs,so we are going to go in users and on the top and click on find object in Active directory service to find any of the user we created to add them in thier respective OUs,so we search for laura and click on find now then we go to property and click move to move her to IT_users and press ok and laura is move in the IT_user OUs, and now we are going to do the same the the rest of the users we made we will make to users per OUs:  <br/>
<img src="https://i.imgur.com/3aL0g4U.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Next here are the users in thier respective OUs 2 users per OUs,next we are goign to create security group for the 3 OUs we made earlier IT_SG,Finance_SG,HR_SG then add users to thier correct groups.:  <br/>
<img src="https://i.imgur.com/R2sZN7k.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Here we are going to create security groups of  IT_SG,Finance_SG,HR_SG,first we are going to click on groups which we want to be under then next we will click on create a new group in the current container above in Active Directory,then we are going to give the first name of the group which will be IT_SG then after that we leave the rest as it is and press ok then we have made our group now we are just going to the same for the rest of the groups we had.  :  <br/>
<img src="https://i.imgur.com/gCHxzFP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Next now we are going to add each user under thier respective groups,first we click the IT_SG then press property then we go to memnber and we add Laura mile and Luka zila to be members but we are going to search for them then add them ass showm then click apply and ok thast all then we are going to do the same for the rest of the users :  <br/>
<img src="https://i.imgur.com/WCTdgf9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/hFgOZOI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
We are going to Simulate and account lock and reset the password.
First we are going to login to laura mile account and change her password first then with the group policy i have set  when we will try many time entrying the wrong password we are going to lock from the account and reset it after :  <br/>
<img src="https://i.imgur.com/0zLCSES.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/hhZHZf4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/sJi0vDi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Next we are going to lock the account and  try to unlock it,so here the account is lock and then we are going to unlock it and change its password :  <br/>
<img src="https://i.imgur.com/lTf3946.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Now we are going to unlock the account so first we are going to find the user in the IT_users OUs then right click and go to properties then accounts then find unlock account and also change the password of the accountand also when changing the password we need to make suer we check user must change password when login in very important for best practice :  <br/>
<img src="https://i.imgur.com/945vyQY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/d3KEYo9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/vcmDzYB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/moNMgLX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/knq2mL7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
We are going to try now to login and see if everyhting works fine now and also we are going to be prompted to change the password again then after all that we will change the password and then be able to log back into laura account as she was suppose to.    :  <br/>
<img src="https://i.imgur.com/gCHxzFP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/DXxuCLd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/FWCKzR0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/aNzOaX4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/qPUT2xf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
We are going to disable an account and put him in the disable user OUs for security awareness and for offboarding, we are going to go into any OUs we made then click on the user and find disable account then an Arrow pointing down will appear then we will just move the user into the disable OUs :  <br/>
<img src="https://i.imgur.com/EprBmR5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/Le5Q6jO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/MHvn3es.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/5UBiXvP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

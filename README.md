# mudbins  
.Zips needed to make a mud server  
  
Azure - assuming you already have an account  
From the Dashboard  
- +Add, Compute, Virtual Machine  
- Windows Server 2012 R2 DataCenter  
- Standard B1ms  
- Networking - allow RDP  
- Management - disable auto shutdown  
Remote to the machine, should be a connect button that will d/l an .rdp file  
You need to get the bins... how you do this is up to you, I have everything in a git repo  
Install git and notepad++  
- Open IE. Accept the settings pop-up  
- search for 'git' in the url bar  
- click add on every pop-up, keep trying until this stops and the search works  
- enable download - IE > gear > inet options > security > internet > custom level - find file download and enable  
- download git and install  
- install notepad++, same process, click add a lot  
open cmd window  
cd \  
git clone https://github.com/jabber422/mudbins.git  
cd mudbins  
- install 7z - 7znnnnn.exe  
- extract all the .zip and .rar files  
  
Install WorldGroup c:\mudbins\worldgroup-3.30\setup.exe  
Run through the install, click next to everything, except for the sysop name/password  
  
open galgsbl.DLL in a hex editor  
search for 'reg#'  
change the registration number to something other than 39574913  
  
run keygen.exe with the new reg #, get the new activation code  
  
  
Run wg > utils > security - oprn core security > ACTCOD - enter the new activation code  
  
Now do everything here - http://www.mudinfo.net/viewtopic.php?f=44&t=2070  


Other stuff I did that wasn't covered and didn't work from the above link

Install MMUD.  The setup.exe in c:\mudbins\MajorMUD v1.11p does not work, do this instead  
open cmd window, cd to c:\mudbins\MajorMUD v1.11p\WCCNT8PJ  
run:  
- icomp WCCMMUD.Z c:\wgserv\*.* -d -o i  
This will extract the wcc files to the wgserv folder  
Then rename *.vir to *.dat  
Copy c:\mudbins\wccmmud.ini to c:\wgserv\  

uncompress both MajorMUD_HSE_FILES_ODSBBS.zip and galtntd-mp.zip into c:\wgserv\*  
HSE are the gang house descriptions - not confirmed this is working yet  
galtntd will add a telnet port option in the general config  

Get the MMUD activation keys  
You will need the reg# from above  
Run the keygen, used the reg#, get all of the activation codes.  option 1,2,4.  
  
Configure the server  
Security and Accounting  
Enter the mud activations keys, from option 1 and 2 above  
To give everyone sys go and sys map - under WCCMUD  
- set GAMOPKEY, SYSOPKEY, PLAYKEY, SAVEKEY to normal  

If you want to allow connections from the internet  
open windows firewall  
click inbound rules -> new rules  
select port, next, select tcp, set the specific local port to the port mud is using (23 by default), next, allow  
name the new rule and apply it  

Azure configure port forwarding  
From Dashboard  
- click on the vm, should open the overview page  
- click networking link  
- click add inbound port rule  
- Change destination port range to the port configured in the firewall  
- Protocol is TCP, everything else should be default  
- name it an save it  
  
Bring up the server and you should be able to connect from any computer using the vm NIC Public IP  
  
Setting up DNS - Azure has this, I haven't played with it yet.  I've used dyndns years ago, it seems to work fine.  






  
  

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
Run through the install, click next except for the sysop name/password  
  
open galgsbl.DLL in a hex editor  
search for 'reg#'  
change the registration number to something other than 39574913  
  
run keygen.exe with the new reh #, get the new activation code  
  
  
Run wg > utils > security - enter the new activation code  
  
Now do everything here - http://www.mudinfo.net/viewtopic.php?f=44&t=2070  
  
If mud won't install go to where it's extracted  
icomp WCCMMUD.Z c:\wgserv\*.* -d -o i  

uncompress both MajorMUD_HSE_FILES_ODSBBS.zip and galtntd-mp.zip into c:\wgserv\*
HSE are the gang house descriptions - not confirmed this is working yet
galtntd will add a telnet port option in the general config

  
  

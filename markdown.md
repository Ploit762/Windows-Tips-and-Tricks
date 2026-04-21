# Windows "sfc scannow" Command for Boot Load Errors

- Many times files can be corrupted on a device that has a Windows OS. Experiencing this on my own with my Windows desktops and lap top devices, I found these commands to be helpful when needing to trouble shoot the issue of an OS not booting like it should.

This can be caused by a combination of things like...
  - hardware failures
  - software corruption
  - incorrect system configurations

The most common causes of these bootloader errors come from Corrupt bootloader files and software corruption. Either way these two commands can help out a lot when troubleshooting the device.

## Steps and Commands
*<p align="left"> To run these commands, you will need... </p>*

- A Drive enclosure.
- A fully functioning Windows device with admin privileges.
- Powershell or Command Line Prompt (CMD)

#
- When repairing a drive that was in a device, usally it is encrypted if the security steps of the device was taken appropriately. Microsoft does have a built in encryption called "Bitlocker". Make sure to grab the encryption key (Bitlocker key) or back it up somewhere that you can easly get to it.

- Make sure to remove the drive "SSD" or "HDD", and put it in a drive enclosure. This will then allow to then connect the drive via USB to another device so that you can run your commands and have admin rights. It is important that the account on your device does have full admin privileges. 
    
*<p align="center"> I will cover "encryption keys" later in this repository </p>*

#
- This command is a simple file checker utiltiy. It checks the integrity of the Windows system files to see if there is any corruption to those files like ".NET". This also repairs the required system files if they were to come up corrupted. Usally after running this command, it would prompt you to choose "Yes" to repair files, or "no" to not repair files. After selectign yes, files will then be in the process of being repaired.

  *<p align="center">"sfc /scannow /offbootdir=`((name of traget drive))`: /offwindir=`((name of traget drive))`:\Windows"</p>*

- After the top command has ran and completed. You can then run this command to repair Windows image located on the drive itself. It uses the default Windows source to fix corrupted files. It will scan for the Windows installation, and fixes the corrupted components of it.

*<p align="center">"DISM /Image:`((name of target drive))`:\ /Cleanup-Image /RestoreHealth"</p>*

#
From here, after everything has completed and the drive came back fully restord and completed both of the commands process, you can then put the drive back into the device that you took it out of and boot to the OS. From there you should be on the "Hello Windows" profile screen.


  

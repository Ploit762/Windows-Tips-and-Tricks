# Utilman.exe Hack/Trick

The Utilman.exe (Utility Manager) is a executable that holds and handles the accessibility options on the login screen of a Windows operating system. The exe file is located in the `C:\Windows\System32\` and can also be accessed from the lock screen by clicking on the Ease of Access icon or the little person in the bottom right corner of the screen. 
#
The utilman.exe hack is used to mostly reset local Windows accounts passwords that are located on the device through CMD. This hack mostly works with local accounts that are on the device, other accounts like domain or cloud accounts vary due to the security that is implemented.

Key thing to remember and make sure that you have is the bitlocker key for what ever drive that the Windows OS is on. Usually the bitlocker key backs itself up to areas like your email or a ".txt" file automatically. If you know the email account associated with the local account, try to log into that account at this link, https://aka.ms/aadrecoverykey</a>. Once you log into the account you can locate the bitlocker key under that device that the email account is connected to. You can save a bitlocker key as a ".txt" file under Bit Locker Management if you have access to that device and logged in with a local account, but this will only work if you are logged in. 
#
* Here are the steps to take to execute this hack, you would first want to work on getting CMD (Command Prompt) to show up at the login screen...

  * Access the WindowsRE by holding `[Shift]` and clicking the restart button on the screen, hold the `[Shift]` button for a while after clicking restart on the screen. Access the Command Prompt in the "Troubleshoot>Advance Option" section.
  * Bitlocker may be enforced, take note of where the bitlocker key is stored. You can find this usually in a Microsoft account if it is backed up.
  * Once you are in CMD (Command Prompt), you would first want to see what drive your Windows Directory is on. To list out disk drives that your computer has, use this command..
      *   `diskpart`
      *   `list disk (Display list a list of disks)`
      *   `list volume (Display a list of volumes)`
   
  *   Once you found the drive that you think has the Windows driectory in it, look to see what files are in there, type any drive letter followed by a colon sign ( : ).
      * `Ex: "C:", "X:"`
  * You would want to look for "Windows" and to the left of it says "DIR" for directory.
      * `Ex: <DIR>  Windows`
  *  Once you found the the "DIR" Windows, you then wnat to execute these commands..
      * `cd windows`
      * `cd system32`
      * `ren utilman.exe utilman1.exe` The command is just renaming the file, feel free to rename this how you please. Just make sure you remember what you renamed it to.
      * `ren cmd.exe utilman.exe`
  * After this is done type "exit" and continue to Windows 11, once you are back at the Hello Windows screen, click on the accessibility icon (Ease of Access icon or the little person icon) at the bottom right corner of the screen.
  * This will now open up the Command prompt (CMD), from here you have the options to reset a local account password or create a local account. Here are the commands to use if wanting to do so..
      * `control userspasswords2` This command gives you a easy to use interface to reset a local accounts password, set up a local account with a password, or delete a local account.
      * `net user` A command that list out local user accounts within CMD, you can find the local user that you are wanting to target this way.
      * `net user <username> \[new password]` once you have the user name, you can then create a new password for the account.
        
      *<p align="center">If the username has a space in it, enclose the username in quotation marks (")</p>*
  * To create a local account within CMD, use these commands..
      * `net user <name> * /add` replace "name" with a name that you are wanting to create.
  * After this type in a password of your choice
  * Once the account is created, add to local admin group.
      * `net localgroup administrators <name of account> /add`
  * After you have successfully got into a local account, you will then want to change everything back to the way it was. repeat the steps from above, Access the WindowsRE by holding `[Shift]` and clicking the restart button on the screen. Access the Command Prompt in the "Troubleshoot>Advance Option" section.
  * Once you access CMD reverse the process that we just did by doing these commands..
      * `"C:", "X:", "D:"` remembering the drive you found the "DIR" Windows on, locate that exact drive. If you forgot, repeat the "diskpart" command above.
      * `cd Windowss`
      * `cd system32`
      * `ren utilman.exe cmd.exe`
      * `ren utilman1.exe utilman.exe`
  * All what is being done here is you renaming the file back to what it was before you started the hack. This is a great way to clean up your tracks that you left behind.
  * type "exit" and continue to Windows 11, check to see if the CMD shows once you click on the accessibility icon. If it does not show and gives you the normal Windows accessibility options, this means you have successfully changed everything back to the way it was.
  * If you are still getting the CMD when clicking the accessibility icon, redo some of the steps and see where you may have missed something. 




      
    


  






This is a guide on how to install the Vox Populi Mod for Civilization V on Linux easily

Contrary to other guides, this guide doesn't require Lutris, Bottles or any other such program. Only Steam and a program called ProtonTricks is required.  
I was inspired by Baaards guide and the information on the civfanatics forum:  
https://gitlab.com/baaard/vox-populi-on-linux/-/blob/main/README.md  
https://forums.civfanatics.com/threads/vox-populi-on-linux.673879/page-2

If you have any problems, please make an issue and I will try to help

# Step 1: Installation of the Windows version of Civ 5
- Open Steam (on your Linux desktop, no Lutris). 
- Right click on Civilization V, right-click on Compatibility and check the "force compatibility" box. In the dropdown, select either the newest version of Proton or Proton experimental. Either will work.
![Selection screen compatibility Steam](https://github.com/TeaDrinkingProgrammer/Civilization-V-Vox-Populi-on-Linux/blob/main/force%20proton.png)
- Now, it will start installing or updating to the windows version.
  -  (Note: reports suggest that the proton version works better than the native version, so this is useful even without VP).


# Step 2: Installing Vox populi
- Install [Protontricks](https://github.com/Matoking/protontricks). Follow their installation instructions as you may need to install Winetricks or do some other things to get it working.
- Download the [Vox Populi Automatic Installer](https://forums.civfanatics.com/threads/community-patch-how-to-install.528034/).
- Once downloaded, right click on the executable and select Open with -> Protontricks Launcher. 
![Select open with, then proton tricks](https://github.com/TeaDrinkingProgrammer/Civilization-V-Vox-Populi-on-Linux/blob/main/select%20protontricks.png)
- (Note: the image is from KDE but this should work in other Desktop interfaces as well).
- Select Civilization V, click OK and wait for a bit. After a few seconds the install window should pop up.
- The default install location is still valid since the .exe file is loaded within the environment (wine prefix) of Civ 5.
- Click next and close the window when it is done installing.

# Step 3: A small hack
You would think VP is installed but there is a small problem. VP installs the mods in the mod directory (the one that was selected) but it also installs some textures in the default steam install location. The problem is that Civ5 is not there. We thus have to move the files from the directory VP thinks is the steam install location to the actual one.

## 3a
  - Try navigating to the following path: "~/.local/share/Steam/steamapps/compatdata/8930/pfx/drive_c/Program Files (x86)/Steam/steamapps/common/Sid Meier's Civilization".Does it contain an "Asset" folder? If there is, skip to step 4. Is the folder empty? Go to 3b and then step 4.
## 3b
  - Open Protontricks and select Civ 5. You can safely ignore the warning about 64-bit prefixes.
  - Select "Select the default prefix" and click on OK.
![Selection screen prefix protontricks](https://github.com/TeaDrinkingProgrammer/Civilization-V-Vox-Populi-on-Linux/blob/main/default%20wineprefix.png)
  - In the next window, select "browse files" and hit OK. A new window or tab should open in your file manager (check because with Wayland the app is not     brought to the foreground). 
  - You can close the Protontricks window(s).
  - navigate to "some_directory/pfx/drive_c/Program Files (x86)/Steam/steamapps/common/Sid Meier's Civilization V/" where "some_directory" is the path where Protontricks sent you.

# Step 4:

  -  Copy the "Asset" folder.
  -  Paste the folder in the installation location of Civ 5 of Steam and confirm the merges. The default location is: "~/.local/share/Steam/steamapps/common/Sid Meier's Civilization V/". If it is not there, check your download locations in Steam (Settings -> Downloads -> Steam Library Folders) to see where Civ 5 is installed.


# Step 5: Enjoy the game!

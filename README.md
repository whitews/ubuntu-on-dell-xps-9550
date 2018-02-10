# ubuntu-on-dell-xps-9550
Setup instructions for installing Ubuntu on a Dell XPS 9550

## For a PCIe m2 drive

Add the following kernel argument at boot time:
nvme_load=YES

1. Press 12 when you see the keyboard prompt
1. Press Enter to select Language
1. Press F6
1. Press Esc
1. Modify the boot option to add "nvme_load=YES" and remove "quiet splash ---"

## UEFI vs Legacy Boot

First you just need to ensure the BIOS is set to UEFI, disable "Legacy option ROMS" and enable secure boot (Secure boot is optional)

Download and create a bootable Ubuntu Linux External Link USB key. (You may want to use a 3rd party application like Rufus External Link to create the bootable USB key.)

NOTE: Dell does not recommend or support applications like Rufus. Third party applications are use at your own risk.
Once the UBUNTU install from the USB key is finished and you reboot the system, Press F2 when you see the Dell logo to enter the BIOS. Once in the BIOS choose Boot Sequence.

In the boot sequence screen that pops up click on the Add Boot Option button. The Add Boot Option window will pop up. Type a name in the Boot Option Name text area (Ubuntu for example). Click the button to the left of the File Name text area. The EFI Boot Selection window will pop up. 

In the File System drop down menu choose "FS0:". Then using the Directories section, navigate until you can choose SHIMx64.EFI file in the Files section. (See figures 5, 6 & 7)

Type a name in the Boot Option Name text area (Ubuntu for example). Click OK. Click Apply. (See Figure 8.)

Exit the BIOS and you should now be able to boot to UBUNTU normally from the boot drive.

##  Setup the Ubuntu Install

Insert the Ubuntu disk into your DVD drive or connect your Bootable USB into a port on the system.

Tap rapidly on the F12 key when you see the Dell logo appear during start up. This will take you to the Boot Once menu.

You can use the Cursor/Arrow keys to navigate the menu and highlight your selection. It will be either boot from USB or Boot from CD/DVD Drive. Once your Choice is highlighted hit the ENTER key.

When the setup boots, choose the Try Ubuntu option. this option will check that your hardware is seen okay by Ubuntu.

When you're ready to proceed, click the Install Ubuntu button. The install wizard will appear to prompt you through some choices.

Select your install language and click Continue.

The Preparing to install Ubuntu window appears. Choose the applicable options and click Continue.


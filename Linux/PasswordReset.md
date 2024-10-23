#### Steps to Reset the Password via GRUB (Recovery Mode):
##### Restart Your System:

##### If your Linux system is already running, reboot it.
* Access GRUB Menu:

##### As the system starts to boot, press the Esc key (or Shift key in some distributions like Ubuntu) to enter the GRUB menu.
* Select the Recovery Mode:

* In the GRUB menu, select the option that says "Advanced options for" followed by your distribution name.
* Then, select the Recovery Mode option, which typically has something like (recovery mode) next to the kernel version.
* Enter Root Shell:

* Once in recovery mode, you'll see a list of recovery options. Choose the option to "Drop to root shell prompt" (or something similar).
* Remount File System as Read/Write:

* Once you are at the root shell (which looks like a terminal), by default, the root filesystem is mounted as read-only. To make changes, you need to remount it as read/write.
Run the following command:

* bash : mount -o remount,rw /

* Reset the Password:

* To change the password for a user (e.g., username), type:
* bash : passwd username
Replace username with your actual username (for the root user, just type passwd without specifying a username).

* Enter the New Password:

* You will be prompted to enter a new password and then confirm it.
Reboot the System:

* Once the password is changed, type the following to reboot the system:
* bash : reboot
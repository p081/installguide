<img width="256" alt="Project081-MainLogo" src="https://user-images.githubusercontent.com/71722170/143572664-dd5c2017-4ed7-4612-880d-783ab828aa28.png">

# Project 081

**You've reached the Install Guide. By following this guide you'll find out how to install Project 081 on your Late 2007 or Early 2008 Macs.**
**You can also download this guide for yourself by clicking "Save As" or by using the following wget command:**

```wget https://raw.githubusercontent.com/p081/installguide/main/README.md```

# Guide starts here.

### **Making sure you have everything**

In order to follow the guide you must have:
- A Late 2007 or Early 2008 Apple Mac. *
- A USB drive or a DVD (2GB or larger, only tested with a 16GB USB drive) *
- An internet connection (Dial-up not recommended) *
- Time and patience (You know, just in case) *
- Second machine running Windows/Mac OS X/Linux (Highly recommended)
- Modern web browser (For downloading images) (Highly recommended)

### **Risks**

- Data loss can happen if you format the wrong partition. 
- Tiger doesn't really like Windows EFI partitions and will sometimes break them so we highly recommend that you install Windows on a separate drive. If you must run Windows on the same drive make sure to back up your data, and be ready to reinstall Windows or at least rebuild your bootloaders. 
- Same can likely happen with Grub, rEFInd, OpenCore, Clover and other bootloaders so back them up before even booting.
- General security things, Mac OS X Tiger has not been updated and supported since 2009 so there are some risks
- Bad luck causing your machine to "reject" the install
- Project 081 is not an official product by Apple and "can" therefore be filled with malicious software (Although you can check for yourself)
- The people behind Project 081 will not take any responsibility for any data loss, dead machines or any reason not listed here. This software is simply provided to you for free and it's your responsibility to use it responsibly.

### **Getting Started**

Make sure you know what Mac you have. Do this by running systemctl hw.model. Results should be one of the following:
- iMac8,1
- Xserve2,1
- MacPro3,1
- MacBook3,1
- MacBook4,1
- MacBookPro4,1
- MacBookAir1,1

If the number value is lower than these then your machine can OFFICIALLY run Mac OS X Tiger and therefore doesn't need this (See download section for Mac OS X images)
If the number value is higher than these then your machine CANNOT run Mac OS X Tiger because the hardware is fully incompatible. Sorry, Apple made it that way. (Although feel free to try)
If you get nothing back, something is wrong with your OS or machine.

If you have a MacBookAir1,1: You will not have ANY graphics acceleration which means your OS might run slow. It should still run well because Tiger is lightweight but keep this in mind.
If you have a MacPro3,1: Your hardware may be unsupported if it was upgraded with components that Tiger doesn't natively support. Make sure to check what hardware you have before installing.
If you have a Hackintosh: Stop, this is the wrong place for that.

On a computer with a working internet connection and a modern enough web browser, check the /Downloads section and download the image your model needs. Make sure you get this right as failing to do so will leave you with a broken OS that may not install. You can download the image with any of the mirrors or with the wget command listed for your download. Do not interrupt or cancel the download.

If you're downloading the image on a Mac running Mac OS X, you may wanna try mounting it before writing the image. If it doesn't mount then it's corrupted and you should definitely redownload the image to prevent wasting your time and potentially breaking your Mac/USB drive.

**Now insert your USB drive into the machine you downloaded the image on.**

### If you wish to burn a DVD instead, you can do so as well but it's unsupported.

SD card booting is not supported (Why would you wanna do that anyway)
Other methods are unsupported, try at your own risk.

### **Writing the image**

To write the image, you will have many options available to you.
In this guide, we're showing you how to use two of them.

**Easy method (using balenaEtcher)**
Download balenaEtcher and install it on the machine you downloaded the image to.
Here are some links you can use to download Etcher

*For Windows users:*
### (Recommended) Visit the official balenaEtcher website (https://www.balena.io/etcher) and download it.

You can also download the portable version quickly using this link although it may be outdated:
https://github.com/balena-io/etcher/releases/download/v1.5.115/balenaEtcher-Portable-1.5.115.exe?d_id=addce433-fbb8-48c9-a92d-3ab640a0a0ebR
```wget https://github.com/balena-io/etcher/releases/download/v1.5.115/balenaEtcher-Portable-1.5.115.exe?d_id=addce433-fbb8-48c9-a92d-3ab640a0a0ebR```

*For Mac OS X/OS X/macOS users:*
(Recommended) Visit the official balenaEtcher website (https://www.balena.io/etcher) and download it.

You can also download the portable version quickly using this link although it may be outdated:
https://github.com/balena-io/etcher/releases/download/v1.5.115/balenaEtcher-1.5.115.dmg?d_id=addce433-fbb8-48c9-a92d-3ab640a0a0ebR
```wget https://github.com/balena-io/etcher/releases/download/v1.5.115/balenaEtcher-1.5.115.dmg?d_id=addce433-fbb8-48c9-a92d-3ab640a0a0ebR```

*For Linux users:*
(Recommended) Visit the official balenaEtcher website (https://www.balena.io/etcher) and download it.

.AppImage AMD64 download:
https://github.com/balena-io/etcher/releases/download/v1.5.115/balena-etcher-electron-1.5.115-linux-x64.zip?d_id=addce433-fbb8-48c9-a92d-3ab640a0a0ebR

.AppImage IA32 download:
https://github.com/balena-io/etcher/releases/download/v1.5.115/balena-etcher-electron-1.5.115-linux-ia32.zip?d_id=addce433-fbb8-48c9-a92d-3ab640a0a0ebR

.deb AMD64 download (Because .AppImage sucks):
https://github.com/balena-io/etcher/releases/download/v1.7.0/balena-etcher-electron_1.7.0_amd64.deb

.deb IA32 download (Because .AppImage sucks):
https://github.com/balena-io/etcher/releases/download/v1.7.0/balena-etcher-electron-1.7.0.x86_64.deb

.rpm download
https://github.com/balena-io/etcher/releases/download/v1.7.0/balena-etcher-electron-1.7.0.x86_64.rpm

```wget https://github.com/balena-io/etcher/releases/download/v1.5.115/balena-etcher-electron-1.5.115-linux-x64.zip?d_id=addce433-fbb8-48c9-a92d-3ab640a0a0ebR```

```wget https://github.com/balena-io/etcher/releases/download/v1.5.115/balena-etcher-electron-1.5.115-linux-ia32.zip?d_id=addce433-fbb8-48c9-a92d-3ab640a0a0ebR```

```wget https://github.com/balena-io/etcher/releases/download/v1.7.0/balena-etcher-electron_1.7.0_amd64.deb```

```wget https://github.com/balena-io/etcher/releases/download/v1.7.0/balena-etcher-electron-1.7.0.x86_64.deb```

```wget https://github.com/balena-io/etcher/releases/download/v1.7.0/balena-etcher-electron-1.7.0.x86_64.rpm```

Once you have balenaEtcher installed and working, launch it using your preferred method.
**NOTE: You may need to format your drive in some cases although Etcher should detect it automatically anyway**

Click "Select Image" and select the Project 081 image you downloaded earlier. Then select your drive (Be careful, you could potentially erase your entire boot drive). Then click "Flash" and wait while it writes the image to your USB drive and verifies it.

**(!!ADVANCED USERS ONLY, DANGEROUS!!) Method 2: Using the Mac OS X Terminal**

If you're running Mac OS X and you wish to use the Terminal to write your image, here's a small and less detailed guide on how you can do it.
This method uses the "dd" command present in Mac OS X. Make sure your version has this.

**NOTE: This method is very dangerous. Erasing the wrong drive WILL cause data loss.
Only use this method if the balenaEtcher method doesn't work or if you're feeling dangerous.**

Run the "diskutil list" command to find the drive identifier for your drive.
Your drive identifier will be /dev/diskX where X is the specific disk.

Make sure you get the right one as otherwise you may lose data
Write the full identifier down somewhere somehow.

Now run "sudo umount /dev/diskX" where X is the disk to unmount the disk. You'll probably need to enter your password.

Once the disk is no longer mounted, run "sudo dd if=/location/p081.dmg of=/dev/diskX" to format and write the image to the disk.
Again, make sure you get the right identifier as otherwise you'll likely erase the wrong drive. Be VERY careful.

Make sure you wait for the process to finish. Do not eject the drive until the image is fully written to the drive. Doing so may cause damage to the drive and will cause corruption.

### **Installation**

If you reached this point and didn't fail, you should have a USB drive (Or DVD) containing Project 081
The hard part is now done, the rest is pretty easy as long as you won't have more issues.

Make sure your Mac is plugged in, and then insert the USB drive into one of its USB ports.
NOTE that the official Apple iMac keyboards are known to cause issues when booting from USB devices so plug it into one of the ports on your machine.

Power on your machine and hold the Option key when powering your machine up. If you don't have an official Apple branded keyboard, it should be the Windows flag key. If you fail this way, try holding Left ALT instead. If you still cannot reach the menu, your keyboard may have a weird configuration. In this case try another keyboard.

Once in the boot menu, you'll want to pick the USB drive. This option may have the Project 081 logo with a Project 081 label but it may also be named "EFI Boot" and have a regular hard drive icon.
If you are not sure which option is correct, unplug any other bootable devices or try booting until you get the right one.

After pressing enter, you should either see an Apple logo with a spinning wheel or a bunch of text. Both of these are normal. Please be patient and wait while it tries to boot to the Project 081 installer.

If all went fine, you should see either a window that looks like an installer with a nice message or a blue screen. If you see a blue screen, please wait a moment while it loads the Installer.app

If you're stuck at a blue screen for a long time (10 or more minutes), the installer probably froze, in this case please contact me or add an issue on GitHub.

At the top of your screen, you should see either a "Util", "Utilities" or "Tools" option. Click this option and then Disk Utility.

Select your internal or external drive (Install destination) and format it as Mac OS Extended (Journaled)
Make sure you don't format the wrong drive. The drive should NOT be MBR but GPT.

Once you're sure you selected the correct drive (You may need to format the entire drive, not just a partition) click the "Erase" button and then "Erase" to confirm it. Wait while it erases your drive and perhaps your memories. It shouldn't take too long. If the process fails, try again. Otherwise the drive may be failing.

Finally, exit out of the Disk Utility, select your drive and click Install. No need to customize as all the extra features have been taken out. Patches will be automatically installed if needed. Now all you have to do is wait for the installation process to finish. It should automatically reboot so you can go grab a snack or something while it installs. After the install, you may eject your USB drive or DVD from your Mac as it shouldn't be needed anymore.

It should automatically boot into your Mac OS X installation but if it doesn't, hold the Option key on boot and select the Mac OS X partition. If it's not available, the installer may have failed to bless the volume. In this case, you may try to bless it yourself but it shouldn't be necessary.

If you boot and it gives you a nice prohibition sign, consider yourself screwed. You may try to reinstall but the issue is likely related to your hardware. You might wanna try booting in Verbose mode to check where it fails. If you're booting through a third-party bootloader then it could likely be the issue. You should boot using completely vanilla methods like Apple intended.
If you kernel panic, your model is likely unsupported and this was a complete waste of time. If your machine IS supported, create an issue on GitHub or contact me.

If it keeps spinning forever, this could be because of the above issues or something completely different. Create an issue on GitHub or contact me.
If you reach the intro video, you'll find out which features work and don't work. If you do not have any audio, you downloaded the wrong image. You should download the (ALT) image instead of the regular one. If you downloaded the ALT image and your machine needs the regular image, reinstall using the regular image.

Set up your Mac as usual, and enjoy your Project 081 install. Any features designed for officially supported Intel Macs should be working, even on your Late 2007/Early 2008 Macs. If some features are broken, create an issue on GitHub please so that I can fix it.

#### You just finished the Project 081 install guide. Thank you for reading!

##### Have a good day! 


### [Return to p081.github.io](https://p081.github.io "Return")



##### Project 081 made using official Apple Mac OS X 10.4.10 Tiger images and unofficial tools. Website and images made by speedie, see Credits section for more information. Images are hosted by my accounts on GitHub and Archive.org.

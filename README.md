# Instructions for installation.
Go and follow this instructions carefully otherwise it won't work. Open your terminal.
## Step 1:
First update your system 'apt update' and upgrade it 'apt upgrade' and to satisfy the dependencies run:

```
sudo apt install plymouth
```
```
sudo apt install plymouth-themes
```
## Step 2:
Upgrade yourself to root if you are an expert outherwise use sudo before every command! we are assuming you are upgrading yourself to root.
Now change the current directory
```
# cd /usr/share/plymouth/themes/
```
Now make a directory named GLUG
```
# mkdir ./GLUG
```
Enter into this directory
```
# cd GLUG
```
Now you gotta clone this repo in there. 
```
# git clone https://github.com/EdiTechStudio/Plymouth-Theme-v2.0 .
```
Don't assume the dot was added by mistake after the .git option. Now move the the content of output directory to the current directory:
```
# mv ./output/* ../
```
## Step 3:
Now let's complete the installation.
Use the command:
```
# update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/GLUG/glug.plymouth 10
 ```
 Select the default theme. 
 ```\
# update-alternatives --config default.plymouth
 ```
 And select the number for your theme e.g glug.plymouth
 
 ## Step 4:
 Now you gotta update your initramfs.
 ```
 # update-initramfs -u
 ```
 So are ready to rock! But hold on, there are things that you might want to recheck!
 If your transition of Plymouth theme isn't smooth, you might want to add this line in your /etc/initramfs-tools/confd folder
 ```
 # echo "FRAMEBUFFER=y" > /etc/initramfs-tools/conf.d/splash
 ```
 Now update your initramfs again.
 ```
 # update-initramfs -u
 ```
 And you are done!

 ## May the source be with you! 🐧❤️

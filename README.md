# Instructions for installation.
Go and follow this instructions carefully otherwise it won't work. Open your terminal.
⚠️⚠️: Make sure you do it from command line because this package requires you to select theme priority.

## Step 1:
First update your system 'apt update' and upgrade it 'apt upgrade' and to satisfy the dependencies run:
```
sudo apt install plymouth
```
## Step 2:
Upgrade yourself to root if you are an expert outherwise use sudo before every command! we are assuming you are upgrading yourself to root.
Now install `wget` in case you don't have it.
```
# apt install wget
```
Now let's download our theme package.
```
wget -P ~/Downloads https://github.com/EdiTechStudio/Plymouth-Theme-v2.0/raw/main/glug-splash-screen-plymouth_2.0_all.deb
```
Now run the command
```
dpkg -i ~/Downloads/glug-splash-screen-plymouth_2.0_all.deb
```
 And you are done!

 ## May the source be with you! 🐧❤️

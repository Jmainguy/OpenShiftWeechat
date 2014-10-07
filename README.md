OpenShiftWeechat
================

Pre-Compiled Weechat, works well inside Openshift cartridges

Create a free openshift account at https://www.openshift.com/
Once signed in. Go to the Applications tab https://openshift.redhat.com/app/console/applications
Select Add application. Choose Do-It-Your-Self at the very bottom of the page
Change the public url to anything you want, I chose to name it weechat
Click Create application
Click Continue to applications overlay
Click Want to log in to your application?
This opens a box with your ssh info, mine looked like ssh 52c593e9e0b8cdd91a000229@weechat2-jmainguy.rhcloud.com
52c593e9e0b8cdd91a000229 is my username, weechat2-jmainguy.rhcloud.com is the hostname, and there is no password, you must use key-authentication.

Setup your ssh key in Openshift.
Click the Settings tab
click add a new key
name it anything you want
place the contents of your public key in box
click create.
 
Now that the app has been created, and you have added your key. Go ahead and ssh into the box.
 
Once logged into the box via ssh. run the following commands to install weechat

cd /sandbox
git clone https://github.com/Jmainguy/OpenShiftWeechat
#Then to run weechat, just run ./weechat.sh from inside the sandbox
#Next time you wish to connect, cd to /sandbox and run ./weechat.sh

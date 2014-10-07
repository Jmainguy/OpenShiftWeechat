OpenShiftWeechat
================

Pre-Compiled Weechat, works well inside Openshift cartridges

**Creating your Cartridge**
- Create a free openshift account at https://www.openshift.com/
- Once signed in. Go to the Applications tab https://openshift.redhat.com/app/console/applications
- Select Add application. Choose Do-It-Your-Self at the very bottom of the page
- Change the public url to anything you want, I chose to name it weechat
- Click Create application
- Click Continue to applications overlay
- Click Want to log in to your application?
- This opens a box with your ssh info, mine looked like ssh 52c593e9e0b8cdd91a000229@weechat2-jmainguy.rhcloud.com
- 52c593e9e0b8cdd91a000229 is my username, weechat2-jmainguy.rhcloud.com is the hostname, and there is no password, you must use key-authentication.

**Setup your ssh key in Openshift.**
- Click the Settings tab
- Click add a new key
- Name it anything you want
- Place the contents of your public key in box
- Click create.
 
**Now that the app has been created, and you have added your key. Go ahead and ssh into the box.**
**Once logged into the box via ssh. run the following commands to install weechat**

```
ssh into your cartridge
cd /sandbox
git clone https://github.com/Jmainguy/OpenShiftWeechat
```
**Now that you have weechat installed, you can keep it running inside of tmux**
```
tmux
cd /sandbox/OpenShiftWeechat
./weechat.sh
```
**Next time you want to connect, just run tmux a to resume your session**
```
ssh into your server
tmux a
```
**To configure your weechat sessions, edit /sandbox/OpenShiftWeechat/.weechat/irc.conf**

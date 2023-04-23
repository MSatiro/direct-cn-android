# direct-connection-android (OUT OF DATE, WILL UPDATE SOON)

### The advantage of a Direct Connection server is the possibility for players on Android and PC play together without using VPN services, quickly and easily.

# **How to create a Direct Connection Server for sm64ex-coop on ANDROID**

## ⚠️ Prerequisites: Termux and Ubuntu in Termux.**

You can get the Termux app in F-Droid Store, using the app or website: <https://f-droid.org/packages/com.termux/>

And for Ubuntu in Termux, follow this very intuitive guide on GitHub: <https://github.com/MFDGaming/ubuntu-in-termux>

With everything installed and ready, let's get down to business. ⚠️

1° **Create a account** on <https://playit.gg> (It is the program that we will use to create our server). You won't have any problems, just create the account and check the email for authentication.

2° In your account page, press `+Add Tunnel` and do these steps:

 • `Tunnel Type:` TCP+UHP

 • `Port Count:` 1

 • `Local Port:` 7777

 • Check the `Enable Tunnel` box, then press **Add Tunnel**.

3° You'll be redirected to your Tunnel page, scroll down until you find the **Update Local Adress** window,

4° Now you can name the Tunnel whatever you want. You will see a window with some information about your tunnel, like the IP, Adress, Port, etc. You will need to **save some information**: `Adress (ex: somethin-your.at.ply.gg)  |  IP (ex: 211.ply.gg)  |  IPV4 (ex: 136.361.221.211)  |  Port (ex: 43578)` Soon we will use it to assemble the connection addresses.

5° On Termux, **check your device architecture** using `uname -m`, will probably be “aarch64”. Go to <https://playit.gg/download/> and donwload the **Linux** version corresponding to your device architecture, so in this case,  get the aarch64

6° Use some file explorer app to move the archive we donwloaded to “ubuntu-in-termux/ubuntu-fs/home”. I recommend using the app **Material Files** (you can find it on Google Play Store or F-Droid), because we will need to enter the Termux folder, which is located externally and not just any file manager will be able to access it. Using the Material Files app: 

(top right corner)

↳ Add Storage 

↳ External Storage

↳ (probay the google integrated files manager will show up, then click top right corner)

↳ Termux

↳ ubuntu-in-termux/ubuntu-fs/home, give the access permission and then move the archive you downloaded to that folder 

7° On Termux, write these commands:

`cd ubuntu-in-termux` 

`./startubuntu.sh`

`cd /home`

`ls | grep playit`  (it will show the playit version, I'll use as **example** “playit-0.9.3-aarch64”) 

`chmod +x playit-0.9.3-aarch64` (again, write the version that appeared when you used the command above)

`./playit-0.9.3-aarch64`

After you write the last command, playit will start and a link will show, **click on the link**. (similar to this playitgg/claim/a1b2c3d3)

8° After the page opens, click on “Add Agent”, and everything will be done, now you just need the addresses for the game. **To find out if the server is active, enter Termux and see if there is informations about your playit server, if everything is “true”, then it's working**

9° Assemble the addresses for your games, remember the information I told you to keep in step 4? So we'll use it now. You have three address options available:

Adress:Port `(ex: somethin-your.at.ply.gg:43578)`

IP:Port `(ex: 211.ply.gg:43578)`

Ipv4:Port `(ex: 136.361.221.211:43578)`

Every time you start an online game, people will have these three addresses choices to use. 

# **Tips:**

• Save the complete command and the adress in the clipboard of your virtual keyboard. This will help you to start the server in Termux (after the 1st time you launch the server) and to share the addresses. Btw you can put all the commands at once when starting, example:

`cd ubuntu-in-termux`

`./startubuntu.sh`

`cd /home`

`./playit-0.9.3-aarch64`

Just make sure you put the command in the Termux text box, **not directly at the prompt, otherwise it won't work**


# **Information about some know problems:**

• Some people **may not be able to enter your server**, I don't know why this happens, but in one of my tests a user could not enter

• Maybe **no one can get into your server**, a friend of mine took the test and I couldn't get in and not even a second friend could either, none of the three addresses worked

• Some of the three addresses may not work when you connect/when they connect to you, but the others may work


**That's all, I hope this guide can be useful for someone :D**

# **Credits:**

I'M NOT a programmer or even the user who created these guides, I just gathered the available information and brought it to you, to make the work slightly easier. **ALL CREDIT GOES TO THESE PEOPLE:**

**MateusL13 for the playit on Termux Guide on Playit Forum; (https://discuss.playit.gg/t/how-to-run-playit-on-android/133)**

**MFDGaming for Ubuntu in Termux on GitHub; (https://github.com/MFDGaming/ubuntu-in-termux)**

And a **special thanks to Sunk for the Playit Setup Guide in Discord** 

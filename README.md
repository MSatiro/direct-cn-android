# direct-connection-sm64excoop-android 

## Prerequisites: [Termux](https://f-droid.org/packages/com.termux/) and [Ubuntu in Termux](https://github.com/MFDGaming/ubuntu-in-termux)
(note: don't download the Termux from Google Play Store, it's outdated and won't properly work)

1° **Create a account** on <https://playit.gg> (It is the program that we will use to create our server). You won't have any problems, just create the account and check the email for authentication.

2° In your account page, press `+Add Tunnel` and do these steps:

 • `Tunnel Type:` TCP+UHP

 • `Port Count:` 1

 • `Local Port:` 7777

 • Check the `Enable Tunnel` box, then press **Add Tunnel**.

3° You'll be redirected to your Tunnel page, scroll down until you find the **Update Local Adress** window, you'll need to put your router IP in the Local Adress, to see your IP on Android: **Go into Wi-fi Settings > Select Your Wi-fi > Details > Scroll Down until you will see the the IP Address**, now copy it and paste in the 'Local Adress`, then click in Update



4° On Termux, **check your device architecture** using `uname -m`, I'll be considering that is “aarch64”. Then go to <https://playit.gg/download/> and donwload the **Linux** version corresponding to your device architecture, so in this example,  get the aarch64 (if isn't aarch64, then grab the corresponding one).

5° Use some file explorer app to **move the archive we donwloaded to “ubuntu-in-termux/ubuntu-fs/home”**. I recommend using the app **Material Files** (you can find it on Google Play Store or F-Droid), because we will need to enter the Termux folder, which is located externally and not just any file manager will be able to access it. Using the Material Files app: 

`(top right corner)`

↳ `Add Storage`

↳ `External Storage`

↳ `(probay the google integrated files manager will show up, then click top right corner)`

↳ `Termux`

↳ `ubuntu-in-termux/ubuntu-fs/home` give the access permission and then move the archive you downloaded to that folder 

6° On Termux, write these commands:

`cd ubuntu-in-termux` 

`./startubuntu.sh`

`cd /home`

`ls | grep playit`  (it will show the playit version, I'll use as **example** “playit-0.9.3-aarch64”) 

`chmod +x playit-0.9.3-aarch64` (again, if your device architecture isn't aarch64 or even the playit version isn't 0.9.3, then write the version that appeared when you used the command above)

`./playit-0.9.3-aarch64`

7° After you write the last command, playit will start and a **token will show, save it somewhere** then go in <https://playit.gg/setup/agent>. That page it's a one-time step, if the webpage doesn't detect your token automatically (what I'm not sure if it's working 100% on mobile), then click on the hyperlink "...[here](https://playit.gg/claim?setup_start=0)" and put the token. The app will validate the token, and you're all set. 
**PRO-GAMER-TIP:** To see if the server is active, go in Termux and see if "Authenticated, Connection Alive and Tunnels Setup" are `true`, if everything is then you're online!

8° In your [tunnel overview](https://playit.gg/account/tunnels) select the tunnel you've created, and you'll find your `Domain`, 'Allocation` and `Port` infos.

Combine then in this way:
`Domain`:`Port` (ex: as-lexington.at.ply.gg:76532)
`Allocation`:`Port` (ex: 229.ip.ply.gg:76532)

**Then you'll have yours addresses to share with your friends!**
Every time you start an online game, people will have these two addresses choices to use. THAT'S ALL! SO SIMPLE AND EASY, RIGHT? 😊

# **Tips:**

• Save the complete command and the adress in the clipboard of your virtual keyboard. This will help you to start the server in Termux (after the 1st time you launch the server) and to share the addresses. Btw you can put all the commands at once when starting, example:

`cd ubuntu-in-termux
./startubuntu.sh
cd /home
./playit-0.9.3-aarch64`

☝️ **That's how you start the server.**
Just make sure you put the command in the Termux text box, **not directly at the prompt, otherwise it won't work**


# **Information about some know problems:**

• Some people **may not be able to enter your server**, I don't know why this happens, but in one of my tests a user could not enter

• Maybe **no one can get into your server**, a friend made the server but in the test and I couldn't get in and not even a second friend could either, none of the addresses worked

• Some of the addresses may not work when you connect/when they connect to you, but the other may work.

• If you're trying to join but the progress bar isn't loading, wait just a little bit more, sometimes it don't load but that doesn't mean you aren't connecting.


**We're done! I hope this guide can be useful for someone :D**

# **Credits:**

I'M NOT a programmer or even the user who created these guides, I just gathered the available information and brought it to you, to make the work slightly easier. **ALL CREDIT GOES TO THESE PEOPLE:**

[MateusL13 for the playit on Termux Guide on Playit Forum] (https://discuss.playit.gg/t/how-to-run-playit-on-android/133)

[MFDGaming for Ubuntu in Termux on GitHub] (https://github.com/MFDGaming/ubuntu-in-termux)

And a **special thanks to Sunk for the Playit Setup Guide in Discord** 
![RaspiBlitz](pictures/raspilogo_400px.png)

*Build your own Lightning Node on a RaspberryPi with a nice Display.*

`Version 1.5.1 with lnd 0.9.2-beta (0.10.0-beta optional) and bitcoin 0.19.1 (or litecoin 0.17.1)`

![RaspiBlitz](pictures/raspiblitz.jpg)

**The RaspiBlitz is a do-it-yourself Lightning Node based on LND running together with a Bitcoin-Fullnode on a RaspberryPi 3/4 - with a HDD/SSD and an nice display for easy setup & monitoring.**

RaspiBlitz is mainly targeted for learning how to run your own node decentralized from home - because: Not your Node, Not your Rules. Discover & develop the growing ecosystem of the Lightning Network by becoming a full part of it. Build it as part of a [workshop](WORKSHOP.md) or as a weekend project yourself.

## Feature Overview

This is a quick look at the SSH main menu (once RaspiBlitz is SetUp):

![MainMenu-A](pictures/mainmenu.png)

As an alternative to the SSH menu the "Ride the Lightning" (RTL) WebUI is available:

![RTL-preview](pictures/RTL-dashboard.png)

There are further Services that can be switched on:

* **TOR** (Run as Hidden Service) [details](https://en.wikipedia.org/wiki/Tor_(anonymity_network)#Onion_services)
* **ElectRS** (Electrum Server in Rust) [details](https://github.com/romanz/electrs)
* **BTCPayServer** (Cryptocurrency Payment Processor) [details](https://btcpayserver.org)
* **BTC-RPC-Explorer** (Bitcoin Blockchain Explorer) [details](https://github.com/janoside/btc-rpc-explorer)
* **LNbits** (Lightning wallet/accounts System) [details](https://twitter.com/lnbits/status/1253700293440741377?s=20)
* **SpecterDesktop** (Multisig Trezor, Ledger, COLDCARDwallet & Specter-DIY) [details](https://twitter.com/CryptoAdvance/status/1233833767283941376?s=20)
* **LNDmanage** (Advanced Channel Management CLI) [details](https://github.com/bitromortac/lndmanage)
* **Loop** (Submarine Swaps Service) [details](https://github.com/lightninglabs/loop)
* **JoinMarket** (CoinJoin Service) [details](https://github.com/JoinMarket-Org/joinmarket-clientserver)

You can connect the following Wallet-Apps to your RaspiBlitz:

* **Zap** (Android, iOS & Desktop) [details](https://zap.jackmallers.com/)
* **Zeus** (Android & iOS-TestFlight) [details](https://zeusln.app)
* **Shango** (Android & iOS-TestFlight) [details](https://github.com/neogeno/shango-lightning-wallet)
* **Fully Noded** (iOS) [details](https://apps.apple.com/us/app/fully-noded/id1436425586)
* **SendMany** (Android) [details](https://github.com/fusion44/sendmany/blob/master/README.md)

Also much more features like Touchscreen, Autopilot, DynDNS, SSH-Tunneling, UPS Support, ...

## Time Estimate to Setup a RaspiBlitz

The RaspiBlitz is optimized for being setup during a workshop at a hackday or conference (see [detailed workshop tutorial](WORKSHOP.md)). When it comes ready assembled together with a up-to-date synced blockchain it's possible to have it ready in about 2 to 3 hours - most is waiting time.

If you start at home ordering the parts from Amazon (see shopping list below) then it's a weekend project with a lot of download and syncing time where you can do other stuff while checking on the progress from time to time.

## Hardware Needed

All parts together are at around 150-250 USD - based on shops and location.

### Buy a ready-2-go RaspiBlitz (Germany, EU and International)

If you like to support the RaspiBlitz project you can order a ready-2-go RaspiBlitz or a all-you-need-hardware set for yourself or for your RaspiBlitz workshop from [raspiblitz.com](https://raspiblitz.com)

### Amazon Shopping List (buy parts & build it yourself)

The cheapest way is to buy and assemble the single parts yourself. There are two packages.

*Please try to use the exact hardware models that are recommended in the shopping lists, because we have multiple reports were for example other SSD or SSD cases/controllers lead to problems. The idea of the shopping lists is to provide you the best tested hardware components that work together - improvement recommendations are always welcome.*

#### Package: Standard (around 250 USD)

*The "Standard Package" is most tested and recommended if you can effort it. It aims to give you the best economic value to run all the RaspiBlitz features at a good performance and even allows you to self-validate your blockchain in under 3 days.* 

* RaspBerry Pi 4 2GB (or 4GB) [amazon](https://geni.us/raspiblitz-4-2gb)
* RaspBerry Power Supply [amazon](https://geni.us/raspiblitz-ps)
* 1TB SSD: [amazon](https://geni.us/raspiblitz-1000gb-san)
* SSD-Case: [amazon](https://geni.us/raspiblitz-ssd-case) 
* Micro SD-Card 32GB: [amazon](https://geni.us/raspiblitz-sc-card)
* LCD-Display: [amazon](https://geni.us/raspiblitz-touchscreen) 
* RaspberryPi Heatsink Case: [amazon](https://geni.us/heatsink-raspi4) 

*You can even pay your RaspiBlitz Amazon Shopping with Bitcoin & Lightning through [Bitrefill](https://blog.bitrefill.com/its-here-buy-amazon-vouchers-with-bitcoin-on-bitrefill-bb2a4449724a).*

#### Package: Minimal (around 180 USD)

*The minimal package aims for the cheapest price and allows you to use old hardware. It will always be possible to run all the basic features of a Bitcoin- & Lightning-Fullnode, but the system might be too slow to validate the blockchain history by itself and run some resource intensive extended services.*

Basic Parts:
* 1TB Hard Drive: [amazon](https://geni.us/raspiblitz-hdd)
* Micro SD-Card 16GB: [amazon](https://geni.us/raspiblitz-sd-card16gb)
* LCD-Display: [amazon](https://geni.us/raspiblitz-touchscreen) 

When RaspberryPi 3 --> add following parts:
* RaspBerry Pi 3: [amazon](https://geni.us/raspiblitz-rpi3)
* Heatsink-Case RP3: [amazon](https://geni.us/raspiblitz-heatsink)
* Powersupply >=3A: [amazon](https://geni.us/raspiblitz-3A-power)

When RaspberryPi 4 2GB --> add following parts:
* RaspBerry Pi 4 2GB [amazon](https://geni.us/raspiblitz-4-2gb)
* RaspBerry Power Supply [amazon](https://geni.us/raspiblitz-ps)
* RaspberryPi Heatsink Case: [amazon](https://geni.us/heatsink-raspi4)

[What other case options do I have?](FAQ.md#what-other-case-options-do-i-have)

## Assemble your RaspiBlitz

When you have all parts you need to:

- Assemble the Heatsink-Case on the RaspberryPi (follow the intructions in package).
- Put the SSD/Hdd into the Case and connect it per USB to the RaspberryPi
- Add the display on top with the pins like in picture below.
- PlugIn the network cable.

In the end your RaspiBlitz should look like this:

![HardwareSetup](pictures/hardwaresetup.jpg)

## Downloading the Software

Your SD-card needs to contain the RaspiBlitz software. You can take the long road by [building the SD-card image yourself](#build-the-sd-card-image) or use the already prepared SD-Card image:

**Download SD-Card image - Version 1.5.1:**

Browser: https://files.rotzoll.de/raspiblitz-v1.5.1-2020-05-30.img.gz

SHA-256: e896c7c1cc38622b02037569c2b76ad56b72dfb93c01024a0cb278d0d899d210 or [SIGNATURE](https://files.rotzoll.de/raspiblitz-v1.5.1-2020-05-30.img.gz.sig)

* [Whats new in Version 1.5 of RaspiBlitz?](FAQ.md#whats-new-in-version-15-of-raspiblitz)
* [How to update my RaspiBlitz?](README.md#updating-raspiblitz-to-new-version)
* [How to verify the sd card image after download?](FAQ.md#how-to-verify-the-sd-card-image-after-download)

## Write the SD-Card image to your SD Card

You need to write the downloaded sd card image (the img.gz-file) to your sd card (16GB minimum) - you can use the very easy tool Balena Etcher for this:
https://www.balena.io/etcher/ .. it's available for Win, Mac & Linux.


## Boot your RaspiBlitz

Insert the SD card and connect the power plug.

* Make sure to connect the raspberry with a LAN cable to the internet at this point.
* Make sure that your laptop and the raspberry are on the same local network.

**Troubleshoot:**

* [I don't have a LAN port on my Laptop - how to connect to my RaspiBlitz?](FAQ.md#i-dont-have-a-lan-port-on-my-laptop---how-to-connect-to-my-raspiblitz)
* [Is it possible to connect the Blitz over Wifi instead of using a LAN cable?](FAQ.md#is-it-possible-to-connect-the-blitz-over-wifi-instead-of-using-a-lan-cable)
* [Can I directly connect the RaspiBlitz with my laptop?](FAQ.md#can-i-directly-connect-the-raspiblitz-with-my-laptop)
* [I connected my HDD but it still says 'Connect HDD' on the display?](FAQ.md#i-connected-my-hdd-but-it-still-says-connect-hdd-on-the-display)

When everything boots up correctly, you should see the local IP address of your RaspiBlitz on the LCD panel.

![LCD0](pictures/lcd0-welcome.png)

Now open up a terminal ([OSX](https://www.youtube.com/watch?v=5XgBd6rjuDQ)/[Win10](https://www.howtogeek.com/336775/how-to-enable-and-use-windows-10s-built-in-ssh-commands/)) and connect through SSH with the command displayed by the RaspiBlitz:

`ssh admin@[YOURIP]` → use password: `raspiblitz`

**Now follow the dialogue in your terminal. This can take some time (prepare some coffee) - but in the end you should have a running Lightning node on your RaspberryPi that you can start to learn and hack on.**

* [I cannot connect per SSH to my RaspiBlitz. What to do?](FAQ.md#i-cannot-connect-per-ssh-to-my-raspiblitz-what-to-do)

## Support

If you run into a problem or you have still a question, follow the steps below to get support. Also check the [setup documentation](#setup-process-detailed-documentation) for details.

1. Lookup the [FAQ](FAQ.md) if you can find an answer to this question/problem.

2. If you have a hardware problem, please check that your hardware parts are exactly the parts recommended in the shopping list above. Different screens or even SSD-casings can cause problems.

3. There is a Telegram Group of RaspiBlitz users helping each other: https://t.me/raspiblitz

4. Please determine if your problem/question is about RaspiBlitz or for example with LND. For example if you cant route a payment or get an error when opening a channel that is an LND question/problem an is best answered by the LND dev community: https://dev.lightning.community

5. Go to the GitHub issues of the RaspiBlitz: https://github.com/rootzoll/raspiblitz/issues Do a search there. Also check closed issues by removing 'is:open' from the filter/search-box.

6. If you haven't found an answer yet, open a new issue on the RaspiBlitz GitHub. You may have to register an account with GitHub for this. If it's a bug with the RaspiBlitz, please add (copy+paste) a Debug Report to your issue (see [FAQ](FAQ.md) how to generate) and/or add some screenshots/photos so the community gets more insight into your problem.

## Setup Process (Detailed Documentation)

*The goal is, that all information needed during setup is provided from the interaction with the RaspiBlitz itself during the setup. Documentation in this chapter is for background, comments for educators and to mention edge cases.*

If you are looking for a tutorial on how to organize a workshop to build the RaspiBlitz, [see here](WORKSHOP.md).

### Init

Automatically after login per SSH as admin to the RaspiBlitz, it will run a hardware test.

![HardwareTest](pictures/hardwaretest.png)

If you see a warning there, please read carefully, because a lot of things that go wrong later (errors and even loss of funds) relate of problems with the hardware. If you get an OK here ... you are good to go :)

In the beginning you can choose how to setup your RaspiBlitz, by running on Bitcoin or Litecoin with Lightning. This is also the point where you can import a Migration file from an older RaspiBlitz - read about Migration [further down](README.md#import-a-migration-file). The default is here to choose Bitcoin.

![SSH0](pictures/ssh0-welcome2.png)

First thing to setup is giving your RaspiBlitz a name:

![SSH1](pictures/ssh1-name.png)

This name is given to the RaspiBlitz as an public alias of the lightning node for everybody to see.

Then the user gets requested to think of and write down 4 passwords:

![SSH2](pictures/ssh2-passwords.png)

You can use this [RaspiBlitz Password Sheet (PDF)](https://github.com/rootzoll/raspiblitz/raw/v1.4/home.admin/assets/RaspiBlitzRecoverySheet.pdf) to write those passwords down for save storage. And also use it later on for your Seed Words.

*The password A,B,C & D idea is directly based in the [RaspiBolt Guide Preperations](https://stadicus.github.io/RaspiBolt/raspibolt_10_preparations.html#write-down-your-passwords) - check out for more background.*

Then the user is asked to enter the Password A:

![SSH3a](pictures/ssh3a-password.png)

This is the new password has to be used for every SSH login after this screen with the user admin. It's also set for the other user existing user: root, bitcoin & pi.

*The bitcoin and lightning services will later run in the background (as daemon) and use the separate user “bitcoin” for security reasons. This user does not have admin rights and cannot change the system configuration.*

Then the user is asked to enter the Password B - this is internally used for the bitcoin RPC interface. But also as login for additional Apps like the RTL-WebGUI or the Blockexplorer:

![SSH3b](pictures/ssh3b-password.png)

*The other passwords C & D will be needed later on. They will be used during the lightning wallet setup.*

### Running behind TOR

On setup you can now decide if you want to run your RaspiBlitz behind TOR or make your IP public to the lightning network.

![TOR](pictures/chooseTOR.png)

Your IP can reveal your location (at least to a certain radius) to everyone and your internet provider has a record of your personal identity tied to your IP. When you choose to run behind the TOR network this personal data is much better protected. But running behind TOR reduces speed and might makes it more difficult to connect to you for other nodes or pairing other devices and apps to it.

You can switch TOR off later on. Also you can switch TOR on also after the setup, but keep in mind that once running your node with your public IP leaves records on the internet connecting your lightning node id to your public IP.

After this the setup process will need some time and the user will see a lot of console outputs - just wait until its finished:

![SSH4](pictures/ssh4-scripts.png)

### Getting the Blockchain

*If you have a HDD/SSD with a prepared blockchain (e.g. a ready2go-set or you are at a workshop) you have the option to trust that data and skip to the [next chapter](#setup-lightning). If you started with an empty HDD - you will see the following screens:*

If you connected a fresh Hard Drive or SSD to the RaspiBlitz it might now ask you if it's OK to format it.

<img src="pictures/ssh4-formatHDD.png" alt="format-HDD" width="366">

*Your HDD/SSD will get formatted with the linux standard file system EXT4. If you want to try out the experimental new [BTRFS](FAQ.md#why-use-btrfs-on-raspiblitz) that RaspiBlitz supports since v1.4 - you need to start the setup with an additional 32GB USB thumb drive connected to the second USB3 port of the RaspberryPi. Then you will unlock this new secret feature.*

After formatting you need to get a copy of the blockchain, the RaspiBlitz offers the following options:

<img src="pictures/ssh5-blockchain2.png" alt="blockchain-options" width="551">

The options - and when to choose which - will be explained here shortly:

#### 1. SYNC - Selfvalidate all Blocks

With the new RaspberryPi 4 (with SSD & min 2GB RAM) this is the best way to go. It will take around 2-3 days to sync & validate directly with the bitcoin network and then you have done it completely the original `don't trust, verify` way.

*For the old RaspberryPi 3 this is not recommended. A RaspberryPi 3 has a very low power CPU and syncing+validating the blockchain directly with the peer2peer network can take multiple weeks - that's why the other options above where invented.*


#### 2. COPY - Copy from Laptop or another RaspiBlitz over Local Network

If you have another computer available (laptop, desktop or another RaspiBlitz) that already runs a working blockchain you can use this option to copy it over to the RaspiBlitz. This will be done over the local network by SCP (SSH file transfer). Choose this option and follow the given instructions.

This is also the best option if you don't like to run your RaspberryPi 3 with a prepared blockchain by a third party. Then install bitcoin-core (0.18.1 or higher) on a more powerful computer, sync+validate the blockchain there by yourself and copy it over after that through the local network.

More details: [I have the full blockchain on another computer. How do I copy it to the RaspiBlitz?](FAQ.md#i-have-the-full-blockchain-on-another-computer-how-do-i-copy-it-to-the-raspiblitz)

#### 3. Torrent Fallback

*This is recommended for old RaspberryPi 3s - for the newer RaspberryPi 4 you might consider the `SYNC` option.*

If you choose `TORRENT` it will show you the following screen:

![DOWNLOAD1](pictures/download-torrent.png)

*This can take a while - normally it should be done if you keep it running over night, but some users reported that it took up to 3 days. If it takes longer than that or you cannot see any progress (downloading starting) for over an hour after you started this option consider to cancel the download and go with the COPY option or retry fresh.*

It is safe to close the terminal window (and shutting down your laptop) while the RaspiBlitz is doing the torrent download. To check on progress and to continue the setup you need to ssh back in again.

You can cancel the torrent download by keeping the key `x` pressed. Then the download will stop and you will be asked if you want to keep the progress so far. This makes sense if you need to shutdown the RaspiBlitz and you want to continue later or when you want to try another download option but want to keep the option to continue on torrent if the other option is slower or not working.

* [I don't trust a torrent blockchain, how can I validate myself?](FAQ.md#how-can-i-avoid-using-a-prepared-blockchain-and-validate-myself)
* [Why is taking my torrent download of the blockchain so long?](FAQ.md#why-is-taking-my-torrent-download-of-the-blockchain-so-long)

### Setup Lightning

Lightning is installed and waiting for your setup if you see this screen.

![SSH7](pictures/ssh7-lndinit.png)

You now decide if you want to setup a fresh new wallet or if you want to recover an old wallet from a RaspiBlitz you had before.

#### Setup a NEW Wallet

This is the default if you setup a RaspiBlitz the first time.

![SSH8](pictures/ssh8-wallet.png)

RaspiBlitz will ask you to set your wallet unlock password - use your chosen PASSWORD C here and confirm it by inputting it a second time.

LND will now generate a fresh cipher seed (word list) for you.

![SSH8](pictures/ssh8-walletb.png)

WRITE YOUR PERSONAL WORDS DOWN before you continue - without it you limit your chances to recover funds in case of failing hardware etc. If you just want to try/experiment with the RaspiBlitz at least take a photo with your smartphone just in case. If you might plan to keep your RaspiBlitz running store this word list offline or in a password safe. You can use the [RaspiBlitz Password Sheet (PDF)](https://github.com/rootzoll/raspiblitz/raw/v1.4/home.admin/assets/RaspiBlitzRecoverySheet.pdf) for this.

#### Recover a OLD Wallet

Choose this option if you had an old RaspiBlitz you want to recover. You have three options to do that:

![SSH7](pictures/ssh7-lndrecover.png)

The RaspiBlitz calling the LND wallet creation command for you:

##### LNDRESCUE LND tar.gz-Backupfile (BEST)

Choose this option if you have made a complete backup of the LND data and have a tar.gz file starting withthe word 'lnd-rescue' available. It will recover all your on-chain funds and open channels you had. But you have to be sure, that the LND backup you have is really the latest version - otherwise you might loose channel funds.

*If you have tar.gz file that starts with 'raspiblitz' than thats a migration file. That also includes your old LND wallet, but you import it earlier in the setup process .. see further below for details.*

##### SEED+SCB Words Seed & channel.backup file (OK)

Next best option is, if you have the channel.backup file and the word seed. This is the best chance to recover your on-chain funds and funds you had in open channels. But all channels you had open before will be closed in this procedure.

##### ONLY SEED Only Seed Word List (Fallback)

If you just have the word list (RaspiBlitz 1.1 and older) you can at least try to recover your on-chain funds. Recover of channel funds is not very likely in this scenario.

### Final LND Setup

It will now make sure your wallet is initialized correctly and may ask you to unlock it with your just set PASSWORD C.

![SSH9c](pictures/ssh9c-unlock.png)

*The LND wallet needs to get unlocked on every new start/reboot of the RaspiBlitz.*

The RaspiBlitz will now do final setup configuration like installing tools, moving the SWAP file to the HDD or activating the firewall. You will see some text moving across the screen until this screen:

![SSH9b](pictures/ssh9b-reboot.png)

The basic setup is done - hooray ... but it can now take still some time before everything is ready and you can play around with your new RaspiBlitz. Press OK to make a reboot. Your terminal session will get disconnected and the raspberry pi restarts.

### First Start: Syncing & Scanning

After the reboot is done it takes a while for all services to start up - wait until you see on the LCD/display that LND wallet needs to get unlocked. Then SSH in again with the same command like in the beginning (check LCD/display) but this time (and every following login) use your PASSWORD A.

After terminal login LND will ask you (like on every start/reboot) to unlock the wallet again - use PASSWORD C:

![SSH9c](pictures/ssh9c-unlock.png)

Now on first start you will have a longer waiting time (between 10 minutes and 2-3 days, depending on your initial setup) ... but that's OK, just leave the RaspiBlitz running until it's done.

![SSH9d1](pictures/ssh9d-sync.png)

*You can even close your terminal now and shutdown your laptop and ssh back in later on. You will see on the Blitz LCD/display that it is ready, when the blue background screen is gone and you see a status screen.*

To understand what is taking so long .. it's two things:

1. Blockchain Sync

The blockchain on your HDD is not absolutely up-to-date. Depending how you got it transferred to your RaspiBlitz it will be some hours, days or even weeks behind. Now the RaspiBlitz needs to catch-up the rest by directly syncing with the peer-2-peer network until it reaches almost 100%. But even if you see in the beginning a 99.8% this can take time - gaining 1% can be up to 4 hours (depending on network speed). So be patient here.

2. Lightning Scanning

Automatically if the Blockchain Sync is progressing LND will start to scan the blockchain and collect information. The Lightning scanning alone normally just take around 1 hour until the waiting time is over. Can take much longer if you recover on old wallet from seed.

* [Why is my "final sync" taking so long?](FAQ.md#why-is-my-final-sync-taking-so-long)

Once all is done you should see this status screen on the RaspiBlitz LCD/display like this:

![SSH9dz](pictures/ssh9z-ready.png)

### Main Menu

If you now login by SSH in your RaspiBlitz (or you are still logged in) you will the the Main Menu:

![SSH9e1](pictures/mainmenu.png)

And if you scroll down .. you see even more options. All options of the main menu will be explained below in the feature documentation.

*OK .. so from here on your RaspiBlitz is ready to play with.*

If you need an idea what the most basic next steps to experience Lightning would be:

* Fund on-chain Wallet
* Open a channel
* Make a payment

If you like to do this all from a web browser with a dashboard UI instead from an SSH terminal, go to `SERVICES`, activate the `RTL Webinterface` and after the reboot open in your web browser: http://[LOCAL-IP-OF-YOU-NODE]:3000 (PASSWORD B is your RPC password).

Have fun riding the lightning :D

*BTW always love seeing photos of new RaspBlitzes added to the network on twitter @rootzoll - also there is a [RaspiBlitz Donation Page](https://tallyco.in/s/r5lx23/), why not try to send some satoshis there with your new RaspiBlitz :D *

* [How can I get further help/support?](#support)

### Feature Documentation

These are the features available through the RaspiBlitz SSH menus. They have the goal to offer some basic/fallback functionality & configurations. More complex or user-friendly tasks are best to be done with wallets, apps and scripts you connect to your Lightning Node via [APIs](#interface--apis) - because you have a full Bitcoin- and Lightning-Node on the RaspiBlitz.

So lets take a look at the SSH main in detail:

#### INFO: Raspiblitz Status Screen

This is the screen that gets displayed on the LCD/display. It's useful to call in a remote situation from SSH if you don't have your RaspiBlitz next to you. But also if you want to copy+paste your nodeID or make a screenshot.

![SSH9dz](pictures/ssh9z-ready.png)

*It's not automatically updating. It's just for one-time info.*

* [Why is my bitcoin IP on the display red?](FAQ.md#why-is-my-bitcoin-ip-on-the-display-red)
* [Why is my node address on the display red?](FAQ.md#why-is-my-node-address-on-the-display-red)
* [Why is my node address on the display yellow (not green)?](FAQ.md#why-is-my-node-address-on-the-display-yellow-not-green)

#### FUNDING: Fund your on-chain Wallet

Before you can open channels with other nodes you need to put some coins onto your LND on-chain wallet. Use this option to generate an address to send funds to.

*Reminder: RaspiBlitz & LND is still experimental software. With funding your LND node you accept the risk of losing funds. So just play with small amounts - something in then area of 20 EUR/USD should be enough to make your first experiences. Also, it's a good privacy practice to [coinjoin your coins](https://bitcoin-only.com/#privacy) before sending them to any Lightning Network wallet.*

You can make multiple fundings - so you can start with small amounts first to test. LND will generate always a different address, but all funds you send will get into the same LND on-chain wallet.

#### CONNECT: Connect to a Peer

Before you can open a channel with another node on the network you need to connect this node as a peer to your node.

Opening a channel with a peer is just optional. Having another node a peer helps your node to receive information about the network through the gossip protocol. It will help your node to find better routes through the network.

#### CHANNEL: Open a Channel with Peer

To open a payment channel with another node you can use this option.

Find interesting nodes to open channels with on online directories like [1ML.com](https://1ml.com/) or join the RaspiBlitz NodeManager telegram group to meet people to open channels with: https://t.me/raspiblitz

Bear in mind that this option will open a public channel that can be seen by everyone in the network. This is good if you want to route payments. If your intention is to use it privately only, you will need to go to the command line and open the channel with the -private option.

*This is just a very basic shell script. For more usability try the RTL Webinterface (under Services) or connect a (mobile) wallet with your RaspiBlitz.*

#### SEND: Pay an Invoice/PaymentRequest

Pay an invoice through lightning.

*This is just a very basic shell script. For more usability try the RTL Webinterface (under Services) or connect a (mobile) wallet with your RaspiBlitz.*

If you are looking for something to test pay with Lightning ... why not [donate some satoshis to the RaspiBlitz development[(https://tallyco.in/s/r5lx23/)? Thanks :) 

#### RECEIVE: Create Invoice/PaymentRequest

Create an invoice to send to someone or a service to be payed through lightnig.

*This is just a very basic shell script. For more usability try the RTL Webinterface (under Services) or connect a (mobile) wallet with your RaspiBlitz.*

#### CLOSE ALL: Closing all open Channels

*This option is just available if you have channels open.*

With this feature you can close down all open channels and get funds locked up in those channels back to your on-chain wallet.

It might even offer you to force close some channels where the channel-partner is no longer reachable. Keep in mind that those force closings can take a much longer time until your funds are available again on your on-chain wallet.

#### CHASHOUT: Remove Funds fro, on-chain Wallet

Use if the want to remove all funds from the RaspiBlitz.

#### lnbalance: Detailed Wallet Balances

<img src="pictures/bonus-lnbalance.png" alt="bonus-lnbalance" width="600">

#### lnchannels: Lightning Channel List

<img src="pictures/bonus-lnchannels.png" alt="bonus-lnchannels" width="600">


#### lnfwdreport: Report on your earned fees for Forwarding Payments 

If you connected your node well within the Lightning Network you can become a "Routing Node" other users select your Node as part of a Lightnig Payment and will pay you the fee you set on those channels. This menu point gives you a detailed report over the amount of days you set.

Beware - earning fees as a routing node does not come automatic. Its a bit of hard work of building the right channels to be attractive for other people to route thru. Check the interet for tutorials or use tools like "lndmanage" (see under RaspiBlitz SERVICES) to help you analyse and optimize your channel management.
  
#### SERVICES: Activate/Deactivate Services

The RaspiBlitz offers further Services, Apps and configuration (scroll down in the to see all in the RaspiBlitz):

![MainMenu-Services](pictures/mainmenu-services.png)

Activate/Deactivate service selection with the space bar and then select OK to trigger Install/Uninstall. Here you find more details about those options (top to down):

##### Channel Autopilot

The autopilot is a feature of LND that you can switch on. It automatically uses around half of your your on-chain funds (if available) to open channels with other lightning nodes the autopilot thinks can be useful to improve your payment routes.

##### Accept Keysend

Keysend is a feature of LND that allows your node to accept payments without creating an invoice first. This is needs to be activated for example if you want to use your nodes for experimental messaging over the Lightning Network (see RaspiBlitz MOBILE apps like SendMany).  

##### Loop

A Submarine Swaps Service by lighting labs. You call it from the RaspiBlitz terminal with the command 'loop' - if you have the RTL service installed (see below), then loop will also be available as part of the RTL web interface. You can use Loop for example to send satoshies from one of your channel to a on-chain bitcoin address without closing the channel for a fee. This can be use full to send earned satoshies to your hardware wallet while freeing up your inbound liquidity on your channels again. 

[Details on Service](https://github.com/lightninglabs/loop)

##### Testnet

You can switch from mainnet to testnet of your blockchain if you want to try things out and play with free test coins.

Please beware that to might take some time to sync the test blockchain and you need to setup a new lnd testnet wallet during the process.

##### DynamicDNS

This is a way to make your RaspiBlitz publicly reachable from the internet so that other nodes can open channels with you and you can connect with your mobile wallet from outside your local network.

To do so you can register at an DynamicDomain service like freedns.afraid.org and forward the TCP ports ...

* 8333 (Bitcoin/mainnet)
* 9735 (LND Node)
* 10009 (LND RPC)
* 8080 (LND REST API)

... from your internet router to the local IP of your RaspiBlitz and then activate under "Services" the "DynamicDNS" option.

You will be asked for your dynamic domain name such like "mynode.crabdance.org" and you can also optionally set an URL that will be called regularly to update your routers IP with the dynamic domain service. At freedns.afraid.org this URL is called "Direct URL" under the menu "Dynamic DNS" once you added one.

*NOTE: DynamicDNS just works if you can forward ports on your router and you have a temporary public IP address (your ISP is not running you behind a NAT - like on most mobile connections). Another solution to make your ports reachable from the public internet is to use reverse ssh tunneling - see FAQ on ['How to setup port-forwarding with a SSH tunnel?'](FAQ.md#how-to-setup-port-forwarding-with-a-ssh-tunnel)*

##### Run behind TOR

You can run your Bitcoin- & Lightning-Node and also additional Apps as a TOR hidden service - replacing your IP with an .onion-address

![tor1](pictures/tor1.png)

This has some benefits:

* You don't publish your IP running a node so it's much harder to resolve your real name and location.
* You tunnel through the NAT of your router and make Bitcoin and Lightning reachable to all other TOR nodes.
* By using a TOR address it's possible to move the node to a different IPv4 address and keep the existing (=preciously open and funded) channels functional.

But this also comes with the following side effects:

* Some Mobile wallets don't support connecting to RaspiBlitz over TOR yet
* Lightning nodes that don't run TOR cannot reach you (like behind NAT)

To try it out just switch on the service - you can deactivate later on if it's not working for you.

##### RTL Webinterface

The RTL Webinterface is a LND Control Dashboard you can run in your browser with a nice GUI - it offers much more control over your Lightning node than the RaspiBlitz SSH menus. It's recommended to give it a try.

![RTL](pictures/RTL-dashboard.png)

Read an Intro-Tutorial to RTL: https://medium.com/@suheb.khan/how-to-ride-the-lightning-447af999dcd2

Feedback is welcome by the RTL programmer: https://github.com/ShahanaFarooqui/RTL

##### BTC-RPC-Explorer

BTC-RPC-Explorer is a blockchain explorer webseite you can run on your own RaspiBlitz. See an example running on: https://btc-explorer.com 

![EXPLORER](pictures/blockexplorer.png)

[Details on Service](https://github.com/janoside/btc-rpc-explorer)

##### Cryptoadvance Specter

Bitcoin Core that you have running on the RaspiBlitz has a very powerful command line interface and a wonderful daemon. Using PSBT and HWI it can also work with hardware wallets, but at the moment it is too linux-way. The same applies to multisignature setups.

The goal of SpecterDesktop is to make a convenient and user-friendly GUI around Bitcoin Core with a focus on multisignature setup with airgapped hardware wallets like Trezor, Ledger, COLDCARD or the Specter-DIY.

![SPECTER](pictures/specter.jpg)

##### LND Auto-Unlock

The RaspiBlitz will automatically unlock the LND wallet on every start.

This feature is based on https://github.com/Stadicus/guides/blob/master/raspibolt/raspibolt_6A_auto-unlock.md

It can be activated under "Services" -> "Auto-unlock LND". It's recommended to be turned on, when DynamicDNS is used. Because on a public IP change of your router, LND gets restarted automatically and without Auto-Unlock it will stay inactive/unreachable until you manually unlock it.

* [When using Auto-Unlock, how much security do I lose?](FAQ.md#when-using-auto-unlock-how-much-security-do-i-lose)

##### Touchscreen (experimental)

Your RaspiBlitz has an LCD that is touchscreen capable. You can switch on this new feature that is still in development.

![RTL](pictures/touchscreen.png)

It will give you 4 buttons on the right side. 

- Info - to defined later
- Node - shows the nodeid/uri as QR code (use to open channels from mobile wallets)
- Invoice - creates an Invoice-QRcode that can be used for donations
- Off - Shutdown or Restart the RaspiBlitz 

##### LCD Rotate

If you switch this on you can rotate the LCD of your RaspiBlitz 180 degrees. This can make sense if you want to use it in a special case or wall mount.

##### Electrum Rust Server

Enable a user to run his own Electrum server on the RaspiBlitz. The server indexes the entire Bitcoin blockchain, and the resulting index enables fast queries for any given user wallet, allowing the user to keep real-time track of his balances and his transaction history using the [Electrum wallet](https://electrum.org).

Since Electrum Rust Server runs on the user's own machine, there is no need for the wallet to communicate with external Electrum servers, thus preserving the privacy of the user's addresses and balances.

For example if you use your Trezor Hardware Wallet with the trezor.io wallet it will tell a third party your public keys - connecting it with your IP. Now you can use your Trezor with the Electrum Wallet just talking to your own Electrum Server preserving your privacy.

[Details on Service](https://github.com/romanz/electrs)

##### BTCPayServer

BTCPay Server is a self-hosted, open-source cryptocurrency payment processor. It's secure, private, censorship-resistant and free. 

![BTCPAY](pictures/btcpay.png)

*At the moment the RaspiBlitz can just make the BTCPayServer publicly available to the outside over the TOR network (Hidden Service).*

[Details on Service](https://btcpayserver.org/)

##### LNDmanage

lndmanage is a command line tool for advanced channel management of an node.

*You need at least one open channel to use this tool.*

To run it change to the RaspiBlitz terminal and type 'manage'. This starts the LNDManage interactive mode and you can use the following commands:

* __Activity reports ```report```__
* __Display the node summary ```status```__
* __Advanced channel listings ```listchannels```__
  * ```listchannels rebalance```: list channels for rebalancing
  * ```listchannels forwardings```: list forwarding statistics for each channel 
  * ```listchannels hygiene```: information for closing of active channels
  * ```listchannels inactive```: information on inactive channels
* __Rebalancing command ```rebalance```__
  * different rebalancing strategies can be chosen
  * a target 'balancedness' can be specified (e.g. to empty the channel)
* __Circular self-payments ```circle```__
* __Recommendation of good nodes ```recommend-nodes```__

[Details on Service](https://github.com/bitromortac/lndmanage/blob/master/README.md)

##### LNbits

LNbits is a very simple server that sits on top of your Lightning Wallet

![LNBITS](pictures/lnbits.png)

It can be used as:
- Accounts system to mitigate the risk of exposing applications to your full balance, via unique API keys for each wallet
- Fallback wallet for the LNURL scheme
- Instant wallet for LN demonstrations

You can also develop extensions on it.

[Details on Service](https://github.com/arcbtc/lnbits/blob/master/README.md)

##### StaticChannelBackup on DropBox

The [below on this README](README.md#backup-for-on-chain---channel-funds) for your Backup options to secure your funds against loss. Storing the encrypted Static Channel Backup file to your Dropbox account is an easy and secure way todo this.

##### JoinMarket

JoinMarket is software to create a special kind of bitcoin transaction called a CoinJoin transaction. It's aim is to improve the confidentiality and privacy of bitcoin transactions.

A CoinJoin transaction requires other people to take part. The right resources (coins) have to be in the right place, at the right time, in the right quantity. This isn't a software or tech problem, its an economic problem. JoinMarket works by creating a new kind of market that would allocate these resources in the best way.

Fore more details see [here](https://github.com/JoinMarket-Org/joinmarket-clientserver).

#### MOBILE: Connect Mobile Wallet

This feature should support you in connecting your RaspiBlitz to a mobile wallet on your smartphone.

<img src="pictures/mobile.png" alt="mobile-wallets">

At the moment the following mobile wallets are supported:

* [ZAP (iOS/Android)](https://github.com/LN-Zap/zap-iOS)
* [Shango (iOS/Android)](https://github.com/neogeno/shango-lightning-wallet)
* [Zeus (iOS/Android)](https://github.com/ZeusLN/zeus)
* [Fully Noded (iOS over TOR)](https://apps.apple.com/us/app/fully-noded/id1436425586)
* [SendMany (Android)](https://github.com/fusion44/sendmany/blob/master/README.md)

Please keep in mind that if you also want to connect to your smartphone also from the outside (when you are outside of your local network) with your RaspiBlitz you might need to open/forward ports on your router and should look into the DynamicDNS features to handle changing IP of our Home-DSL.

This youtube video explains the "port forwarding" on your router in more detail: https://www.youtube.com/watch?v=KESo7hHXQtg

When you have TOR activated you can also try to connect mobile wallets that support this. The Fully Noded Wallet can only connect over TOR. 

If you run your node behind TOR the SendMany App will just offer to connect when your in the same local network ... for connection over TOR there is no support yet. 

Basically those mobile wallets work as a remote control app for your RaspiBlitz. First you need to install the apps on your phone - a QR code with the links to the app stores are displayed. And then you need to `pair` them with your RaspiBlitz - also with a QR code displayed on the LCD. If you run your RaspiBlitz without a LCD there is the fallback option to display that QR code on the terminal as ASCII code (might involve lowering your terminal font size).

#### LNDCREDS: Macaroons and TLS.cert

If you want to access your LND APIs (to connect apps and additional services) you need credential files that grant to access (Macaroons & the TLS cert).

*Macaroons: Access Tokens that allow certain command executions on the LND node.*

*TLS: Certificate to secure/encrypt the communication with the LND node.*

In this menu you can reset and re-sync those or export them as a file or string so that you can import them to the apps and additional services. The following export options are available:

Offers the following options to get the Macaroon and TLS files to be used in other apps and wallets.

##### Hex-String

The Macaroons and TLS.cert files can be copy+pasted as Hex-Strings from RaspiBlitz to any other app that supports that. If you choose this option RaspiBlitz will all files print for you as Hex-String to do so.

This method is recommended to export to:
* [Joule Browser Wallet](https://lightningjoule.com)

##### SSH Download

SCP is a SSH like command to transfer files. If were able to SSH into the RaspiBlitz also the SCP to transfer the files should work. If you choose these option, RaspiBlitz will print prepared SCP commands you can copy+paste to run in a second terminal.

This method is recommended to export to:
* [Zap Desktop Wallet](https://github.com/LN-Zap/zap-desktop)

##### Browser download

Opens an ad-hoc webserver so that you can download the files in your local network through the browser.

*This is a least secure way to transfer those file - everybody in your local network has access to those file during download. Remember with the Admin-Macaroon somebody could takeover your node and spend all your funds. Just use as last fallback.*

##### Renew Macaroons & TLS

Use if you want to invalidate earlier exported Macaroons & TLS files - e.g. lost mobile wallet.

#### NAME: Change Name/Alias of Node

Change the name of your node.

#### PASSWORD: Change Passwords

Change you passwords for security.

#### REPAIR: Options to test, repair and reset your RaspiBlitz

The `REPAIR` menu gives you options to check and reset your RaspiBlitz

![RepairMenu](pictures/repairmenu.png)

The options are explained in detail:

##### HARDWARE: Run Hardware Test

This will start the hardware test and identify if your RaspiBlitz is in good shape and can provide a stable service.

Use this option is you see under-voltage reports on your LCD display or you think your RaspiBlitz gets very hot.

##### SOFTWARE: Run Software Tests (DebugReport)

This will print out a lot of information that can be used to find software problems.

Use this if you want to report a software problem with your RaspiBlitz so that others can have a look at the details and help you better.

##### BACKUP-LND: Backup your LND data (Rescue-File)

This stops your RaspiBlitz and creates a LND-Rescue ZIP file you can download per SCP to your laptop. This can be used to move your LND id, wallet & channels to another RaspiBlitz. 

*NOTICE: If you start your RaspiBlitz after this backup again the backup is outdated and using it can risk loosing your channel funds.*

##### MIGRATION: Migrate Bitz Date to new Hardware

This stops your RaspiBlitz and creates a Migration ZIP file you can download/export per SCP to your laptop. This contains all important data of your RaspiBlitz including LND, your Blitz configuration and also data from your installed apps. Can be used to migrate your RaspiBlitz to a new hardware - for example if your want to replace the HDD with a SSD. How to import a Migration File [see here](README.md#import-a-migration-file).

*NOTICE: If you start your RaspiBlitz after exporting the migration file again it is outdated and using it can risk loosing your channel funds.*

##### RESET-CHAIN: Delete Blockchain and Re-Download

Use this if your blockchain data got corrupted. It will keep your LND data. You can even keep your channels open. Just keep in mind that your node will be offline to the network until you re-downloaded the blockchain.

##### RESET-LND: Delete LND data & start new node/wallet

*THIS WILL DELETE ALL YOUR LND DATA WITH FUND AND CHANNELS.
Use this if you have closed all channels and removed all funds.*

Use this if you want to start with a fresh LND nodeid & wallet.

##### RESET-HDD: Delete HDD data but keep blockchain

*THIS WILL DELETE ALL YOUR LND DATA WITH FUND AND CHANNELS.
Use this if you have closed all channels and removed all funds.*

Use this if you want to setup a fresh RaspiBlitz but don't want to re-download the blockchain on setup.

##### RESET-ALL: Delete HDD completely & start fresh

*THIS WILL DELETE ALL YOUR LND DATA WITH FUND AND CHANNELS.
Use this if you have closed all channels and removed all funds.*

Use this if you want to setup a fresh RaspiBlitz with an empty HDD.

##### DELETE-ELEC: Delete Electrum Index

If you had Electrum installed you can use this option to make sure also the space consuming electrum index gets deleted to free up space.

##### DELETE-INDEX: Delete Bitcoin TX-Index

If you had the Bitcoin Transaction Index activated you can use this option to make sure also tthis extra space consuming index gets deleted to free up space.

#### UPDATE: Check/Prepare RaspiBlitz Update

The `UPDATE` menu gives you options to upadte your RaspiBlitz

![UpdateMenu](pictures/updatemenu.png)

The options are explained in detail:

*Please note that the RaspiBlitz does not support an Auto-Update to ensure that there is no remote control of your node possible from a central server.*

#### RELEASE: Update RaspiBlitz to a new Version

This is common way to update your RaspiBlitz. Choose this option to prepeare your raspiBlitz for a new sd card image containing the new version release.

#### LND: Interim LND Update

Sometimes there is a new LND release that has some breaking changes that once you updated the LND databse that cannot be reversed (like the update from 0.9.2 to 0.10.0). Then RaspiBlitz offers you an optional update ... this is where you then can update LND. 

If oyu choose this you get the option to do this `VERIFIED` that means it offers you the optional LND update we tested the raspiBlitz with or `RECKLESS` which will just grab the latest LND release from the GitHub releases page (also Release Candidates) and install it with no further garantees and verification checks - this is for people that run nodes to test new releases and how they work with existing RaspiBlitz apps. 

#### PATCH: Patch RaspiBlitz code

With Patching you have now an easy way to sync your RaspiBlitz code/scripts with the official RaspiBlitz GitHub Repo or even your own forked GitHUb Repo. This is an option for people that report bugs and we like to offer them a quick script update (patch) between RaspiBlitz releases or for people that wnat to develolp on the RaspiBlitz and sync code between their IDE, forked GitHub and their RaspiBlitz.   

#### REBOOT: Reboot RaspiBlitz

A safe way to restart the RaspiBlitz ... have you tried to turn it off and on again?

#### OFF: PowerOff RaspiBlitz

A safe way to shutdown the RaspiBlitz.

#### X: Console Terminal

Closes the SSH main menu and exits to the terminal - where the user can make use of the CLI clients `bitcoin-cli` & `lncli` directly to make use of the Bitcoin - and Lightning node.

With the command `raspiblitz` it's possible to return to the main menu.

## Import a Migration File

As mentioned above you can export a Migration File from your Raspiblitz with MAINMENU > REPAIR > MIGRATION and store it on your laptop.

A Migration file contains all the important data of your RaspiBlitz like your LND data, Bitcoin Wallet, raspiblitz.config, TOR/SSH keys .. and also the data of installed apps. You can use this to migrate your RaspiBlitz to a new hardware. 

If you want to it to import it again to a new RaspiBlitz (for example with an updated HDD/SSD) you can choose the MIGRATION option on the first setup dialog after the Hardwaretest (where you normally choose between Bitcoin & Litecoin).

![SSH0](pictures/ssh0-welcome2.png)

If you start MIGRATION you will need in the next step to format your HDD/SSD.

![MIGRATION1](pictures/migration1.png)

Normally you choose here the EXT4 format. But you have also have the option to choose the BTRFS format which is an expiremental feature under RaspiBlitz - see [FAQ for details on BTRFS](FAQ.md#why-use-btrfs-on-raspiblitz).

Then you wil be asked to upload the Migration Zip file to the RaspiBlitz. Follow the instructions shown to you. 

Finally you need to decide how to get a copy of the blockchain data again for your RaspiBlitz.

![MIGRATION2](pictures/migration2.png)

Here you have the two options [SYNC](README.md#1-sync---selfvalidate-all-blocks) and [COPY](README.md#2-copy---copy-from-laptop-or-another-raspiblitz-over-local-network) as mentioned in the normal setup.

Then RaspiBlitz will reboot and start the normal recovery process to install all the services that are defined by the raspiblitz.config from your Migration File.

Then the blockhain needs to sync up and you should be back to normal.

## Interface / APIs

To develop your own scripts/apps and to connect other services/apps to your RaspiBlitz you have multiple interfaces/APIs available:

### Bitcoin

* `bitcoin-cli` command line interface on the terminal
* `bitcoind` running on port 8333 (public)
* `JSON-RPC` running on port 8332 (local) [DOC](https://en.bitcoin.it/wiki/API_reference_%28JSON-RPC%29)

### LND-Lightning

* `lncli` command line interface on the terminal [DOC](https://api.lightning.community/)
* `lnd` running on port 9735 (public)
* `gRPC` running on port 10009 (public) [DOC](https://api.lightning.community/)
* `REST` running on port 8080 (public) [DOC](https://api.lightning.community/rest/index.html)

If you activate TOR then your LND gRPC & REST APIs are also reachable publicly as a Hidden Service.

### Backup for On-Chain- & Channel-Funds

Since LND v0.6 (and RaspiBlitz v1.2) a feature called Static-Channel-Backups is available. Within RaspiBlitz this is used when a `channel.backup` file is mentioned.

It's the best backup to protect the funds you put on your RaspiBlitz and into channel available yet - so it's recommended to make use of it.

To recover your funds you need two things:
- the 24 words seed
- the latest `channel.backup` file

The word seed you got during wallet setup, to write it down and to keep it at a safe (offline) location. The `channel.backup` is stored on the HDD and updated by LND every time a new channel is opened or closed. The latest version of this file is needed to recover all your funds (if possible). In case your HDD gets damaged, RaspiBlitz always keeps a copy of the latest version of the `channel.backup` file on the SD card within the sub-directories of: `/home/admin/.lnd/data/chain/`.

If you want to get one step further in securing your funds against total fall-out of the RaspiBlitz (gets completely damaged, stolen or lost) then you can additional setup an off-location or cloud backup of the `channel.backup` file. The file itself is encrypted by your word seed - so it's OK to store the file to untrusted third parties for backup (if you want). The feature is still new ... here is how you can set it up -a t the moment the following two off-location options are available (and/or):

#### A) DropBox Backup Target

Acticate the StaticChannelBackup to DropBox in the `SERVICES` menu of your RaspiBlitz. It will ask you for the Dropbox-Authtoken - this is how you can get this token:

Go to your web browser, do the following:

1. Go to https://www.dropbox.com/developers/apps/create and sign in

1. Choose **Dropbox Api**

    ![Dropbox API 1](https://raw.githubusercontent.com/vindard/lnd-backup/master/images/dropbox-1.png)

1. Choose **App Folder**

    ![Dropbox API 2](https://raw.githubusercontent.com/vindard/lnd-backup/master/images/dropbox-2.png)

1. Name your app and click **Create App** to proceed

    ![Dropbox API 3](https://raw.githubusercontent.com/vindard/lnd-backup/master/images/dropbox-3.png)

1. On the settings page for your new app, scroll down to **OAuth 2** and click **Generate**

    ![Dropbox API 4](https://raw.githubusercontent.com/vindard/lnd-backup/master/images/dropbox-4.png)

1. You will now see a string of letters and numbers appear. This is your **Dropbox-Authtoken**.

To test it - open or close a channel and check if you find a copy of `channel.backup` in your dropbox. You can check the background-script logs to see details on errors: `sudo journalctl -f -u background`

#### B) SCP Backup Target

*You can also backup the SCB to your own server, but this needs manual setup:*

In the `/mnt/hdd/raspiblitz.conf` the parameter `scpBackupTarget='[USER]@[SERVER]:[DIRPATH-WITHOUT-ENDING-/]'` can be set to activate this feature. On that remote server the publickey of the RaspiBlitz root user needs to be part of the authorized keys - so that no password is needed for the background script to make the backup.

The script `/home/admin/config.scripts/internet.sshpubkey.sh` helps on init, show and transfer ssh-pubkey to a remote server.

To test it - open or close a channel and check if you find a copy of `channel.backup` on your remote server. You can check the background-script logs to see details on errors: `sudo journalctl -f -u background`

## Updating RaspiBlitz to new Version

If you have a RaspiBlitz v1.2 or higher - just follow the `UPDATE` option from the main menu (choose `RELEASE` if asked) and follow the instructions.

If you have a RaspiBlitz older then version v1.0 please [see here](FAQ.md).

If you have a RaspiBlitz v1.0 or v1.1 or newer do the following:

* Main menu > OFF
* Remove power
* Remove SD card

Now download the new RaspiBlitz SD card image and write it to your SD card .. yes you simply overwrite the old one, it's OK, the RaspiBlitz stores all your personal data on the HDD. See details about latest SD card image [here](#installing-the-software).

*If you have done manual changes to the system (installed packages, added scripts, etc) you might need to do some preparations before overwriting your sd card - see [FAQ](FAQ.md#why-do-i-need-to-re-burn-my-sd-card-for-an-update).*

If done successfully, simply put the SD card into the RaspiBlitz and power on again. Then follow the instructions on the display ... and don't worry, you don't need to re-download the blockchain again.

* [Why do I need to re-burn my SD card for an update?](FAQ.md#why-do-i-need-to-re-burn-my-sd-card-for-an-update)

## Build the SD Card Image

A ready to use SD card image of the RaspiBlitz for your RaspberryPi is provided as download by us to get everybody started quickly (see above). But if you want to build that image yourself - here is a quick guide:

* Get a fresh Rasbian RASPBIAN BUSTER WITH DESKTOP card image: [DOWNLOAD](https://www.raspberrypi.org/downloads/raspbian/)
* Write image to a SD card: [TUTORIAL](https://www.raspberrypi.org/documentation/installation/installing-images/README.md)
* Add a file called `ssh` to the root of the SD card when mounted to enable SSH login
* Start card in Raspi and login per SSH with `ssh pi@[IP-OF-YOUR-RASPI]` password is `raspberry`

Now you are ready to start the SD card build script (check the code if every installs and config is OK for you) - copy the following command into your terminal and execute:

`wget https://raw.githubusercontent.com/rootzoll/raspiblitz/master/build_sdcard.sh && sudo bash build_sdcard.sh`

As you can see from the URL you find the build script in this Git repo under `build_sdcard.sh` - there you can check what gets installed and configured in detail. Feel free to post improvements as pull requests.

The whole build process takes a while. At the end the LCD drivers get installed and a reboot is needed. A user `admin` is created during the process. Remember the default password is now `raspiblitz`. You can login per SSH again - this time use admin: `ssh admin@[IP-OF-YOUR-RASPI]`. An installer of the SD card image should automatically launch. If you do not want to continue with the installation at this moment and use this sd card as a template for setting up multiple RaspiBlitze, click `Cancel` and run `/home/admin/XXprepareRelease.sh`. Once you see the LCD going white and the activity LED of the pi starts going dark, you can unplug power and remove the SD card. You have now built your own RaspiBlitz SD card image.

*Note: If you plan to use your self build sd card as a MASTER copy to backup image and distribute it. Use a smaller 8GB card for that. This way it's ensured that it will fit on every 16 GB card recommended for RaspiBlitz later on.*

* [Can I run RaspiBlitz on other computers than RaspberryPi?](FAQ.md#can-i-run-raspiblitz-on-other-computers-than-raspberrypi)
* [How can I build an SD card other then the master branch?](FAQ.md#how-can-i-build-an-sd-card-other-then-the-master-branch)
* [How can I build an SD card from my forked GitHub Repo?](FAQ.md#how-can-i-build-an-sd-card-from-my-forked-github-repo)

## FAQ

Here is a just a short selection of the very frequently asked questions:

* [How to backup my Lightning Node?](FAQ.md#how-to-backup-my-lightning-node)
* [How can I recover my coins from a failing RaspiBlitz?](FAQ.md#how-can-i-recover-my-coins-from-a-failing-raspiblitz)
* [Are those "Under-Voltage detected" warnings a problem?](FAQ.md#are-those-under-voltage-detected-warnings-a-problem)
* [Can I run RaspiBlitz on other computer boards than RaspberryPi?](FAQ.md#can-i-run-raspiblitz-on-other-computers-than-raspberrypi)

You have still more questions? Check the [RaspiBlitz-FAQ-Archive](FAQ.md).

## Community Development

Everybody is welcome to join, improve and extend the RaspiBlitz - it's a work in progress. [Check the issues](https://github.com/rootzoll/raspiblitz/issues) if you wanna help out or add new ideas. You find the scripts used for RaspiBlitz interactions on the device at `/home/admin` or in this git repo in the subfolder `home.admin`.

To start your Deep Dive into the RaspiBlitz project, the following YouTube video from the London Bitcoin Dev Meetup (July 2019) is recommended: [https://youtu.be/R_ggGj7Hk1w](https://youtu.be/R_ggGj7Hk1w)

[![Watch the RaspiBlitz DeepDive](pictures/raspiblitz-deepdive.png)](https://youtu.be/R_ggGj7Hk1w)

Also get inspired for a deep-dive with the original "[RaspiBolt](https://stadicus.github.io/RaspiBolt/)" tutorial on how to build a lightning node on the RaspberryPi which was the base work the RaspiBlitz was developed on - so much thx to Stadicus :)

Join me on twitter [@rootzoll](https://twitter.com/rootzoll), visit us at a upcoming [#lightninghackday](https://twitter.com/hashtag/LightningHackday?src=hash) or check by on of our bitcoin meetups in Berlin ... every 1st Thursday evening a month at the room77 bar - feel free to buy me a beer with lightning there :)

* [How can I get further help/support?](#support)

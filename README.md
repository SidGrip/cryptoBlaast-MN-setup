# cryptoBlast
Shell script to install a [Blast Masternode](https://bitcointalk.org/index.php?topic=2547036) on a Linux server running Ubuntu 16.04.
Use it at your own risk.
***

## VPS installation
<a href="https://www.vultr.com/?ref=7390666" rel="nofollow">Believe Me, I have Tried Everything. Click Here for Vultr</a>
<br>
<br>
Copy & paste into terminal window
```
wget -q https://github.com/SidGrip/cryptoBlast-MN-setup/raw/master/blast_install.sh
bash blast_install.sh
```
During the Masternode setup it will ask for your Private key, copy the output from step 5 below.
***

## Desktop wallet setup

As the Masternode is installing, you need to configure the desktop wallet accordingly. Here are the steps:
1. Open the Blast Desktop Wallet.
2. Go to RECEIVE and create a New Address: **MN1**
3. Send **6400** Blast to **MN1**. You need to send all 6400 coins in one single transaction.
4. Go to **Help -> "Debug Window - Console"**
5. Type the following command: masternode genkey
5. Type the following command: masternode outputs
6. Go to  **Tools -> "Open Masternode Configuration File"**
7. Add the following entry:
```
Alias Address Privkey TxHash TxIndex Identifier
```
* Alias: **MN1**
* Address: **VPS_IP:PORT**
* Privkey: **Masternode Genkey**
* TxHash: **First value from Step 5**
* TxIndex:  **Second value from Step 5**
* Identifier: **Payout address**
8. Save and close the file.
9. Go to **Masternode Tab**. If you tab is not shown, please enable it from: **Settings - Options - Wallet - Show Masternodes Tab**
10. Click **Update status** to see your node. If it is not shown, close the wallet and start it again. Make sure the wallet is unlocked.
11. Select your MN and click **Start Alias** to start it.
12. Alternatively, open **Debug Console** and type:
```
startmasternode alias MN1
```
14. Login to your VPS and check your masternode status by running the following command to confirm your MN is running:
```
blast-cli masternode status
```
***

## Usage:
```
blast-cli masternode status #To check your MN status
blast-cli getinfo #To get general info such as Blast version and current block numnber
blast-cli mnsync status #To check if your MN is synced.
```
Also, if you want to check/start/stop **Blast**, run one of the following commands as **root**:

```
systemctl status Blast #To check if Blast service is running
systemctl start Blast #To start Blast service
systemctl stop Blast #To stop Blast service
systemctl is-enabled Blast #To check if Blast service is enabled on boot
```
***

## Donations
Any donation is highly appreciated

**--- sidgrip ---**
<br>
**Blast**: BG3ejZ1bJaxh3UMeqND7Sn8xtT5M1RBT6o


**---- zoldur ----**
<br>
**BTC**: 3MQLEcHXVvxpmwbB811qiC1c6g21ZKa7Jh
<br>
**ETH**: 0x26B9dDa0616FE0759273D651e77Fe7dd7751E01E
<br>
**LTC**: LNZpK4rCd1JVSB3rGKTAnTkudV9So9zexB

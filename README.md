# Relarium
Shell script to install a [Relarium Masternode](https://relarium.com/) on a Linux server running Ubuntu 16.04. Use it on your own risk.

***
## Installation:
```
wget -q https://raw.githubusercontent.com/Driekant/Relarium/master/Relarium_install.sh
bash Relarium_install.sh
```
***

## Desktop wallet setup

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps for Windows Wallet
1. Open **Relarium Core Wallet**.
2. Go to RECEIVE and create a New Address: **MN1**
3. Send **1000** **Relarium** to **MN1**.
4. Wait for 15 confirmations.
5. Go to **Tools -> "Debug console - Console"**
6. Type the following command: **masternode outputs**
7. Go to  **Tools -> "Open Masternode Configuration File"**
8. Add the following entry:
```
Alias Address Privkey TxHash Output_index
```
* Alias: **MN1**
* Address: **VPS_IP:PORT**
* Privkey: **Masternode Private Key**
* TxHash: **First value from Step 6**
* Output index:  **Second value from Step 6**
9. Save and close the file.
10. Go to **Masternode Tab**. If you tab is not shown, please enable it from: **Settings - Options - Wallet - Show Masternodes Tab**
11. Click **Update status** to see your node. If it is not shown, close the wallet and start it again. Make sure the wallet is un
12. Select your MN and click **Start Alias** to start it.
***

## Usage:
```
Relarium-cli mnsync status
Relarium-cli getinfo
Relarium-cli masternode status #This command will show your masternode status
```

Also, if you want to check/start/stop **Relarium** , run one of the following commands as **root**:

```
systemctl status Relarium #To check the service is running.
systemctl start Relarium #To start Relarium service.
systemctl stop Relarium #To stop Relarium service.
systemctl is-enabled Relarium #To check whetether Relarium service is enabled on boot or not.
```
***

## Issues:
If your Relarium Core Wallet doesn't sync, go to **Tools -> Open Wallet Configuration File** and add the following entries:

```
```

## Donations:  


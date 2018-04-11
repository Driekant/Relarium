Shell script to install a Tec-AX Masternode on a Linux server running Ubuntu 16.04. Use it on your own risk.
Installation:

wget -q https://raw.githubusercontent.com/zoldur/Tecax/master/tecax_install.sh
bash tecax_install.sh

Desktop wallet setup

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps for Windows Wallet

    Open Tecax Core Wallet.
    Go to RECEIVE and create a New Address: MN1
    Send 1000 TECAX to MN1.
    Wait for 15 confirmations.
    Go to Tools -> "Debug console - Console"
    Type the following command: masternode outputs
    Go to Tools -> "Open Masternode Configuration File"
    Add the following entry:

Alias Address Privkey TxHash Output_index

    Alias: MN1
    Address: VPS_IP:PORT
    Privkey: Masternode Private Key
    TxHash: First value from Step 6
    Output index: Second value from Step 6

    Save and close the file.
    Go to Masternode Tab. If you tab is not shown, please enable it from: Settings - Options - Wallet - Show Masternodes Tab
    Click Update status to see your node. If it is not shown, close the wallet and start it again. Make sure the wallet is un
    Select your MN and click Start Alias to start it.

Usage:

tecax-cli mnsync status
tecax-cli getinfo
tecax-cli masternode status #This command will show your masternode status

Also, if you want to check/start/stop tecax , run one of the following commands as root:

systemctl status Tecax #To check the service is running.
systemctl start Tecax #To start Tecax service.
systemctl stop Tecax #To stop Tecax service.
systemctl is-enabled tecax #To check whetether Tecax service is enabled on boot or not.

Issues:

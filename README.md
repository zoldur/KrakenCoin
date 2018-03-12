# Kraken
Shell script to install n [Kraken Masternode](http://krakencoin.eu/) on a Linux server running Ubuntu 16.04. Use it on your own risk.
***

## Installation
```
wget -q https://raw.githubusercontent.com/zoldur/KrakeCoin/master/kraken_install.sh  
bash kraken_install.sh
```
***

## Desktop wallet setup  

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:  
1. Open the Kraken Desktop Wallet.  
2. Go to RECEIVE and create a New Address: **MN1**  
3. Send **2500** KC to **MN1**.  
4. Wait for 15 confirmations.  
5. Go to **Help -> "Debug Window - Console"**  
6. Type the following command: **masternode outputs**  
7. Go to **Masternodes** tab  
8. Click **Create** and fill the details:  
* Alias: **MN1**  
* Address: **VPS_IP:PORT**  
* Privkey: **Masternode Private Key**  
* TxHash: **First value from Step 6**  
* Output index:  **Second value from Step 6**  
* Reward address: leave blank  
* Reward %: leave blank  
9. Click **OK** to add the masternode  
10. Click **Start All**  
***

## Usage:
```
Krakend masternode status  
Krakend getinfo
```
Also, if you want to check/start/stop **Kraken**, run one of the following commands as **root**:

```
systemctl status Kraken #To check if Kraken service is running  
systemctl start Kraken #To start Kraken service  
systemctl stop Kraken #To stop Kraken service  
systemctl is-enabled Kraken #To check if Kraken service is enabled on boot  
```  
***

## Donations

Any donation is highly appreciated  

  
**BTC**: 3MQLEcHXVvxpmwbB811qiC1c6g21ZKa7Jh  
**ETH**: 0x26B9dDa0616FE0759273D651e77Fe7dd7751E01E  
**LTC**: LNZpK4rCd1JVSB3rGKTAnTkudV9So9zexB  

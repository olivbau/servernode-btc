```bash
apt update
apt upgrade
apt install snapd git
snap install bitcoin-core
ufw allow ssh
ufw enable
bitcoin-core.daemon -daemon -conf=./bitcoin.conf
git clone https://github.com/olivbau/servernode-btc.git
cd servernode-btc
```
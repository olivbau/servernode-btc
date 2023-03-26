```bash
git clone https://github.com/olivbau/servernode-btc.git
cd servernode-btc
apt update
apt upgrade
apt install -y snapd git clang cmake build-essential cargo

# Bitcoin core
snap install bitcoin-core
ufw allow ssh
ufw enable
bitcoin-core.daemon -daemon -server -chain=main -prune=0 -txindex=0
bitcoin-core.cli  stop

# Electrs
git clone https://github.com/romanz/electrs
cd electrs
cargo build --locked --release
./target/release/electrs --version

~/snap/bitcoin-core/common/.bitcoin
```
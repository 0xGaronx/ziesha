**ℤ - The Groth Testnet**

**Install Bazuka**

 

 - Pertama Pastikan Kalian Memakai Ubuntu 22 juga menginstall `libssl-dev` dan `cmake` caranya :
 

> 
```
sudo apt-get update && sudo apt-get upgrade
sudo apt install -y build-essential libssl-dev cmake
```

 - Kemudian Install rustup
> 
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
 - Clone bazuka repo
> 
```
git clone https://github.com/ziesha-network/bazuka
```
 - Lalu Pastikan biner Rust ada di PATH Anda sebelum dikompilasi
> 
```
source "$HOME/.cargo/env"
```
 - Jika sudah. langsung install
> 
```
cd bazuka
cargo install --path .
```
**Buat Wallet atau Impor Wallet**
 - Jika kalian sudah punya wallet nya silahkan import wallet dengan cara 
> 
```
bazuka init --network groth-6 --bootstrap 65.108.193.133:8765 --mnemonic "YOUR OLD MNEMONIC PHRASE"
```
Silahkan rubah `"YOUR OLD MNEMONIC PHRASE"` dengan mnemoric wallet kalian.

- Jika kalian belum punya atau ingin membuat wallet baru caranya :
> 
```
bazuka init --network groth-6 --bootstrap 65.108.193.133:8765
```
Pastikan kalian menuliskan frasa mnemonik yang dibuat untuk kalian di tempat yang aman! Semua hadiah akan masuk ke kunci publik ini, di mainnet mendatang!

- jalankan nodenya dengan screen, pastikan kalian sudah menginstal screen!

> 
```
screen -S bazuka
```
- kemudian jalankan
> 
```
bazuka node start --discord-handle "NAMA DISCORD#ID"
```
Ubah `"NAMA DISCORD#ID"` dengan Username discord kalian.
Kemudian `CTRL+A+D` untuk deattached screen. dan berjalan di layar belakang.

- Untuk cek nodenya
> 
```
screen -Rd bazuka
```

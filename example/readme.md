# Inery Json RPC (RPC API push transaction)
Inery Blockchain'de JSON RPC'yi çağırmak için aşağıdaki işlemleri sırası ile yapalım.
## Bilgiler
JSON RPC Örnek kodu örnek dizinde mevcuttur, [example](https://github.com/Oxumare/ineryjs/tree/master/example) değiştirmeyi deneyebilir ve nasıl çalıştığını anlayabilirsiniz, ayrıca kodunuzu çalıştırabilmek ve değerli sözleşme işlevini çağırabilmek için Hesabınızda Değerli Akıllı Sözleşmeye (Görev 3) sahip olmanız gerekir.
##  Başlayalım
Eski Nodejs kaldıralım
<br>
```shell
sudo apt-get remove nodejs
```
Curl yükleyelim
```shell
sudo apt-get install curl
```
Nodejs yükleyelim
```shell
curl -fsSL https://deb.nodesource.com/setup_19.x | sudo -E bash - &&\
sudo apt-get install -y nodejs
```
     
##  NPM kurulumu
```shell
sudo apt install npm
```
##  Kurulum
* Repoyu klonlayın
   ```
   git clone https://github.com/Oxumare/ineryjs.git
   ```
* ineryjs dizinine girin
   ```
   cd ineryjs
   ```
* NPM Paket kurun
   ```
   npm install
   ```
* Aşağıdaki Kod ile env-sample dosyasının ismini .env yapın 
   ```
   cp .env-sample .env
   ```
*  ```.env``` bilgileriniz düzenleyin
  ```
   nano .env
   ```
Burada açılan pencerede <br><br>
Aşağıdaki bilgileri inery testnet dashboard kısmında bulabilirsiniz.<br><br>
INERY_ACCOUNT="YOUR_INERY_ACCOUNT" <br>
PRIVATE_KEY="YOUR_PRIVATE_KEY"
NODE_URL="http://YOUR_NODE_URL:8888"
<br><br>
ctrl +X  Yes diyip çıkalım.
<br>
<img src="https://raw.githubusercontent.com/herculessx/Q-Network-Testnet/main/env-duzenle.png" >
##  8888 port açma 

```
sudo ufw allow 8888
```
<br>
## Çalıştırma
RPC örneğini çalıştıralım
```
npm run rpc-example
```

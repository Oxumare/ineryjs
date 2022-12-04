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
*  ```.env``` bilgilerinizi düzenleyin
  ```
   nano .env
   ```
Aşağıdaki bilgileri inery testnet dashboard kısmında bulabilirsiniz.

INERY_ACCOUNT="YOUR_INERY_ACCOUNT"
PRIVATE_KEY="YOUR_PRIVATE_KEY"
NODE_URL="http://YOUR_NODE_URL:8888"


ctrl +X + Y enter diyip çıkalım.


##  8888 portu açalım (Port kapalı olmamalı)

```
sudo ufw allow 8888
```
Portu bu adresden kontrol edelim. >> [Port Kontrol](https://dnschecker.org/port-scanner.php)

## Çalıştırma

RPC örneğini çalıştıralım

```
npm run rpc-example
```

Eğer işleminiz başarılı bir şekilde gerçekleşmiş ise aşağıdaki gibi json döngüsüne benzer bir çıktı almalısınız.Bu çıktıda transaction ID ve işlemin gerçekleştiği Blok yüksekliğini görebilirisiniz;

![Adsız](https://user-images.githubusercontent.com/43583832/205498792-e8775496-f892-4776-be83-bf5e44da3ad3.png)

İsterseniz bu işleminizi [Inery Explorer](https://explorer.inery.io/) sayfasından da kontrol edebilirisiniz. 

![Adsız1](https://user-images.githubusercontent.com/43583832/205498878-8e7d660b-b2ea-4b38-ad1b-e7926e6bf76b.png)



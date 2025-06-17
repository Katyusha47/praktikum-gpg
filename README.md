# praktikum-gpg

## Install gpg
Pertama, install terlebih dahulu gpg nya dengan cara:
```bash
sudo apt install gnupg
```
<img src="install gpg.png" width="800">

Setelah itu, generate terlebih dahulu user gpg nya dengan cara:
```bash
gpg --gen-key
```
<img src="gpg gen key 1.png" width="600">

Jika muncul seperti gambar diatas, langkah selanjutnya adalah masukkan nama kalian dan hanya 1(satu) kata saja.
Setelah itu, klik enter, lalu masukkan email kalian seperti gambar dibawah. Selanjutnya, pilih "o" lalu enter.

<img src="gpg gen key 2.png" width="600">

Selanjutnya, akan ada perintah untuk memasukkan passphrase. Masukkan angka "123" di kedua kolom tersebut:

<img src="gpg gen key 3.png" width="600">

Setelah itu klik OK. Lalu, jika muncul message warning seperti gambar dibawah, pilih opsi "Take this one anyway":

<img src="gpg gen key 4.png" width="600">

Jika sudah selesai, maka akan muncul seperti gambar dibawah (SCREENSHOT HASILNYA):

<img src="gpg gen key 5 (final).png" width="600">



## Export public & private gpg keys
Setelah melakukan instalasi dan setup gpg, langkah selanjutnya adalah melakukan export dan import public dan private keys.

### Export
Untuk melakukan export ikuti langkah langkah dibawah:
```bash
# Pertama, ketik command dibawah ini untuk meng export public keys
gpg -a --export >mypubkeys.asc

# Selanjutnya, ketik command berikut untuk meng export private keys
gpg -a --export-secret-keys >myprivatekeys.asc
```

Setelah melakukan export private keys, kalian akan diminta untuk memasukkan passphrase seperti gambar dibawah:
<img src="export passwd.png" width="700">

Jika muncul seperti digambar, maka masukkan password "123" seperti yang sudah dibuat sebelumnya.

Setelah itu, export gpg trustdb ke text file dengan cara:
```bash
gpg --export-ownertrust >otrust.txt
```

Jika sudah, hasilnya akan seperti gambar dibawah (SCREENSHOT HASILNYA).
<img src="export gpg.png" width="600">


### Import
Selanjutnya adalah melakukan import gpg keys. Caranya pertama import terlebih dahulu private keysnya seperti berikut:
```bash
gpg --import myprivatekeys.asc
```
<img src="import private.png" width="600">

Setelah muncul informasi private keysnya, import public keys dengan cara:
```bash
gpg --import mypubkeys.asc
```
<img src="import public.png" width="600">

Lalu kita cek kedua key ini apakah ada idalam trustdb yang sudah kita export sebelumnya. Caranya adalah:
```bash
gpg -K
```

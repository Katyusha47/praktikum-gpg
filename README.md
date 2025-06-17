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

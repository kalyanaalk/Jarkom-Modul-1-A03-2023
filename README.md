## No. 1

### User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.

Hal pertama yang dilakukan adalah menggunakan filter berikut.

```
ftp
```

Lalu mencari packet yang mengunggah suatu file. Di packet 147, ditemukan Request: STOR c75-GrabThePhisher.zip.

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/fbce19fb-f865-4da1-817f-c70ce539890c)

### a. Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut? 

Ditemukan bahwa sequence number (raw) adalah 258040667.

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/ce7899a3-f493-439e-ac28-d58bdd590bda)

### b. Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut? 

Ditemukan bahwa acknowledge number (raw) adalah 1044861039.

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/799d4956-a422-4ffd-9fe9-0c66fdcf06ab)

### c. Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

Response dari aktivitas berikut ditemukan di packet 149. Ditemukan bahwa sequence number (raw) adalah 1044861039.

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/d9c8f02a-95f6-44aa-b16d-dc006688318a)

### d. Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

Ditemukan bahwa acknowledge number (raw) adalah 258040696/

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/40d2ec5e-44b9-4c6c-b05b-193c2cfbe71d)

### Screenshot pengerjaan

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/5caa1298-6122-453b-90c7-a74aa53c80b9)

## No. 2

### Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

Portal praktikum jaringan komputer adalah 10.21.78.111. Karena itu, untuk mencarinya, digunakan filter berikut.

```
ip.addr == 10.21.78.111
```

Pilih satu paket dan lakukan Follow TCP Stream. Web server yang digunakan tertera di bagian server. Web server yang digunakan pada portal praktikum Jaringan Komputer adalah Gunicorn.

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/5d6a6dac-6cfc-48da-ac22-d75241c31575)

### Screenshot pengerjaan

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/4b938dcc-665f-4f0d-97f7-4a24c523a6cd)

## No. 3

### Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:

### a. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?

Untuk mencari banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702, digunakan filter berikut.

```
ip.addr == 239.255.255.250 and udp.port == 3702
```

Dengan menghitung total paket yang muncul dengan filter di atas, didapatkan bahwa  banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702 adalah 21 buah.

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/64b98f3a-3c95-40d4-abc0-bc7d266259b0)

### b. Protokol layer transport apa yang digunakan?

Seluruh paket dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702 memiliki protokol layer transport UDP, yang dapat dilihat pada kolom protokol.

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/b1fd30b7-01da-43e4-997b-b625fff72830)

### Screenshot pengerjaan

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/aff32528-d1de-46ca-8a7a-3c17c6ab444d)

## No. 4

### Berapa nilai checksum yang didapat dari header pada paket nomor 130?

Nilai checksum dapat dilihat di subtree User Datagram Protocol, dan didapatkan bahwa nilai checksum dari header packet 130 adalah 0x18e5.

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/4e28a257-b05a-4799-a7d6-d2a816c8bca6)

### Screenshot pengerjaan

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/48dc4744-abbf-4b8c-9107-1f118ab88f6c)

## No. 5

### Elshe menemukan suatu file packet capture yang menarik. Bantulah elshe untuk menganalisis file packet capture tersebut.

Di dalam file zip, terdapat file .txt yang membutuhkan password untuk dibuka. Karena itu, dari file .pcapng, dicari info password yang ditemukan di packet no. 14.

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/6bcd294e-ba1c-4640-953f-a7f44326a391)

Berikut adalah isi dari follow TCP stream.

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/07305ed7-a591-47f9-8858-773d2fa13346)

Hasil decode Base64 dari NWltcGxlUGFzNXdvcmQ= adalah 5implePas5word. Password ini digunakan untuk membuka file .txt. Isinya yaitu perintah untuk membuka pertanyaan lewat instance berikut.

```
nc 10.21.78.111 11111
```

### a. Berapa banyak packet yang berhasil di capture dari file pcap tersebut?

Terdapat 60 packet yang berhasil di capture dari file pcap tersebut.

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/5bdcb740-ea88-445b-8da3-525dc54838ac)

### b. Port berapakah pada server yang digunakan untuk service SMTP?

Port yang digunakan adalah port 25.

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/a58dbe30-d287-45c4-85b6-79c5e9433934)

### c. Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?

Yang merupakan public IP adalah 74.53.140.153, seperti yang bisa dilihat di poin 5b.

### Screenshot pengerjaan

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/77843558-371f-4e4e-bf3e-2e104879e0e4)

## No. 6

### Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.

### Clue 1: Sepertinya ada yang salah dengan penulisan tersebut secara KBBI. Ada sesuatu yang Besar di depan mata.

### Clue 2: Jenis cipher merupakan substitusi a1z26 Cipher

### Clue 3: Rentang Huruf yang digunakan Huruf A-R, 1-18 dengan Jawaban 6 Huruf.

### Clue 4: SOURCE ADDRESS ADALAH KUNCI SEMUANYA.

Pertama, dicari packet no. 7812. 

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/3048f075-3168-45fb-b012-9175f9d4f35e)

Source address dari packet no. 7812 adalah 104.18.14.101. Rentang huruf yang digunakan adalah A-R, 1-18 dengan jawaban 6 huruf. Maka, source address dipecah menjadi sebagai berikut.

10 4 18 14 10 1

Menggunakan a1z26 cipher dan menggunakan huruf kapital (dari clue pertama), didapatkan hasil berikut.

JDRNJA

### Screenshot pengerjaan

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/a15caae8-e6b7-4fb6-94ca-7e9bae3cb65f)

## No. 7

### Berapa jumlah packet yang menuju IP 184.87.193.88?

Untuk mencari packet yang menuju IP 184.87.193.88, digunakan filter berikut.

```
ip.dst == 184.87.193.88
```

Didapatkan bahwa jumlah packet yang menuju IP 184.87.193.88 adalah 6.

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/7ef2ab21-7ce9-45ca-87bf-229567a1d8c9)

### Screenshot pengerjaan

![image](https://github.com/kalyanaalk/Jarkom-Modul-1-A03-2023/assets/107338432/557529c1-3059-48f8-933b-f7369f46f2c8)

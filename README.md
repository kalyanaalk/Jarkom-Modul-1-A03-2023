# Jarkom-Modul-1-A03-2023

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


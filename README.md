# Jarkom-Modul-4-E11-2021
## Anggota Kelompok :
| Nama | NRP |
|------|-----|
|Rizqi Rifaldi|05111940000068|
|Yusuf Anfasya|05111940000077|
|Muhammad Subhan|05111940000204|

Pada soal shift Modul 4 kita disuruh untuk membuat subnetting dan routing menggunakan VLSM dan CIDR.

Topologi :

[![Whats-App-Image-2021-11-26-at-20-42-16.jpg](https://i.postimg.cc/TPDBydLW/Whats-App-Image-2021-11-26-at-20-42-16.jpg)](https://postimg.cc/yJ7LtzTV)

Untuk VLSM menggunakan Cisco Packet Tracer.
Untuk CIDR menggunakan GNS3.

Untuk di GNS3 CLOUD merupakan NAT1 jangan sampai salah agar bisa terkoneksi internet. Pembagian IP menggunakan Prefix IP yang telah ditentukan pada modul pengenalan.
Pembagian IP dan routing harus SE-EFISIEN MUNGKIN. Pastikan semua NODE pada GNS3 dapat melakukan ping ke its.ac.id


## VLSM
Pada VLSM ini kami menggunakan Cisco Packet Tracer. Subnetting yang kami terapkan pada topologi adalah sebagai berikut :

[![Whats-App-Image-2021-11-26-at-21-15-00.jpg](https://i.postimg.cc/9fVCjgQ9/Whats-App-Image-2021-11-26-at-21-15-00.jpg)](https://postimg.cc/ZWf18c3Y)

Dengan menggunakan subnetting tersebut, perhitungannya adalah :

|Subnet|Jumlah IP|Netmask|
|------|---------|-------|
|  A1  | 	 1001  |	/22  |
|  A2  |	2      | 	/30  |
|  A3  |	2      |	/30  |
|  A4  |	2      |	/30  |
|  A5  |	701    |	/22  |
|  A6  |	2      |	/30  |
|  A7  |	101    |	/25  |
|  A8  |	2021   |	/21  |
|  A9  |	521    |	/22  |
|  A10 |	502    |  /23  |
|  A11 |	13	   |  /28  |
|  A12 |	2      |	/30  |
|  A13 |	2      | 	/30  |
|  A14 |	252    |	/24  |
|  A15 |	721    |	/22  |

VLSM dari subnetting tersebut adalah :

[![Whats-App-Image-2021-11-26-at-22-19-16.jpg](https://i.postimg.cc/FsBfbLVq/Whats-App-Image-2021-11-26-at-22-19-16.jpg)](https://postimg.cc---/4mpNsnMb)

Setelah itu didapatkanlah pembagian IP dari setiap subnet sebagai berikut :

|Subnet|  Network ID  |       Netmask     |
|------|------------  |-------------------|
|  A1  | 192.205.4.0  |  255.255.252.0    |
|  A2  | 192.205.0.0  |  255.255.255.252  |
|  A3  | 192.205.0.4  |  255.255.255.252  |
|  A4  | 192.205.0.8  |  255.255.255.252  |
|  A5  | 192.205.8.0  |  255.255.252.0    |
|  A6  | 192.205.0.12 |  255.255.255.252  |
|  A7  | 192.205.0.128|  255.255.255.128  |
|  A8  | 192.205.24.0 |  255.255.248.0    |
|  A9  | 192.205.12.0 |  255.255.252.0    |
|  A10 | 192.205.2.0  |  255.255.254.0    |
|  A11 | 192.205.0.32 |  255.255.255.240  |
|  A12 | 192.205.0.16 |  255.255.255.252  |
|  A13 | 192.205.0.20 |  255.255.255.252  |
|  A14 | 192.205.1.0  |  255.255.255.0    |
|  A15 | 192.205.16.0 |  255.255.252.0    |

## CIDR

pada CIDR kita menggunakan gns3 untuk melakukan subnetting dan routing ,sebelumnya kita membuat topologi yang sama dengan packet tracer terlebih dahulu seperti :

![image](https://user-images.githubusercontent.com/77099292/143672890-51ffbebe-5ca4-4790-b6c6-e2a65f330a75.png)


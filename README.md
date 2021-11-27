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

### Subnetting
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

### Routing 

Routing pada tiap-tiap routernya adalah sebagai berikut :

#### Foosha
|Subnet|      IP     |Netmask|  Next Hop  |
|------|-------------|-------|------------|
|  A5  | 192.205.8.0 |  /22  |192.205.0.6 |
|  A1  | 192.205.4.0 |  /22  |192.205.0.6 |
|  A9  |192.205.12.0 |  /22  |192.205.0.14|
|  A7  |192.205.0.128|  /25  |192.205.0.2 |
|      |   0.0.0.0   |  /0   |192.205.0.6 |
|  A10 | 192.205.2.0 |  /23  |192.205.0.14|
|  A11 | 192.205.0.32|  /28  |192.205.2.1 |
|      |   0.0.0.0   |  /0   |192.205.0.14|
|  A12 |192.205.0.16 |  /30  |192.205.0.17|
#### Water 7

|Subnet|      IP     |Netmask|  Next Hop  |
|------|-------------|-------|------------|
|      |   0.0.0.0   |  /0   |192.205.0.5 |
|  A1  | 192.205.4.0 |  /22  |192.205.0.5 |
|  A8  |192.205.24.0 |  /21  |192.205.0.2 |
|  A7  |192.205.0.128|  /25  |192.205.0.2 |

#### Pucci

|Subnet|      IP     |Netmask|  Next Hop  |
|------|-------------|-------|------------|
|      |   0.0.0.0   |  /0   |192.205.0.1 |

#### Guanhao
|Subnet|      IP     |Netmask|  Next Hop  |
|------|-------------|-------|------------|
|      |   0.0.0.0   |  /0   |192.205.0.13|
|  A11 | 192.205.0.32|  /28  |192.205.2.3 |
|  A13 | 192.205.0.20|  /30  |192.205.0.18|
|  A14 | 192.205.1.0 |  /24  |192.205.0.18|
|      |   0.0.0.0   |  /0   |192.205.0.18|

#### Alabasta

|Subnet|      IP     |Netmask|  Next Hop  |
|------|-------------|-------|------------|
|      |   0.0.0.0   |  /0   |192.205.2.1 |

#### Oimo

|Subnet|      IP     |Netmask|  Next Hop  |
|------|-------------|-------|------------|
|      |   0.0.0.0   |  /0   |192.205.0.17|
|  A15 | 192.205.16.0|  /22  |192.205.1.3 |

#### Seastone

|Subnet|      IP     |Netmask|  Next Hop  |
|------|-------------|-------|------------|
|      |   0.0.0.0   |  /0   |192.205.1.1 |

### Hasil
Pada gambar dibawah adalah beberapa contoh hasil testing dari subnetting dan routing :

[![Whats-App-Image-2021-11-27-at-17-48-02.jpg](https://i.postimg.cc/fW52q4Z0/Whats-App-Image-2021-11-27-at-17-48-02.jpg)](https://postimg.cc/BtLBtVjq)

## CIDR

pada CIDR kita menggunakan gns3 untuk melakukan subnetting dan routing ,sebelumnya kita membuat topologi yang sama dengan packet tracer terlebih dahulu seperti :

![image](https://user-images.githubusercontent.com/77099292/143672890-51ffbebe-5ca4-4790-b6c6-e2a65f330a75.png)

Selanjutnya kita akan melakukan pembagian Subnet



### CIDR Tree

![cidrtree](SS\CIDRtree.png)

### Setting GNS 3

### Router

##### Foosha

```
auto lo 
iface lo inet loopback 

auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
	address 192.205.32.1
	netmask 255.255.252.0

auto eth2
iface eth2 inet static
	address 192.205.64.1
	netmask 255.255.255.252

auto eth3
iface eth3 inet static
	address 192.206.16.1
	netmask 255.255.255.252

auto eth4
iface eth4 inet static
	address 192.206.8.1
	netmask 255.255.255.252
```

##### Water7

```
auto eth0
iface eth0 inet static
	address 192.205.64.2
	netmask 255.255.255.252
gateway 192.205.64.1

auto eth1
iface eth1 inet static
	address 192.205.128.1
	netmask 255.255.252.0

auto eth2
iface eth2 inet static
	address 192.205.16.1
	netmask 255.255.255.252
```

##### Guanhao

```
auto eth0
iface eth0 inet static
	address 192.206.16.2
	netmask 255.255.255.252
gateway 192.206.16.1

auto eth1
iface eth1 inet static
	address 192.206.0.1
	netmask 255.255.254.0

auto eth2
iface eth2 inet static
	address 192.206.40.1
	netmask 255.255.255.252


auto eth3
iface eth3 inet static
	address 192.206.4.1
	netmask 255.255.252.0
```

##### Oimo

```
auto eth0
iface eth0 inet static
	address 192.206.40.2
	netmask 255.255.255.252
gateway 192.206.40.1

auto eth1
iface eth1 inet static
	address 192.206.36.1
	netmask 255.255.255.0

auto eth2
iface eth2 inet static
	address 192.206.48.1
	netmask 255.255.255.252

```

##### Pucci

```
auto eth0
iface eth0 inet static
	address 192.205.16.2
	netmask 255.255.255.252
gateway 192.205.16.1

auto eth1
iface eth1 inet static
	address 192.205.8.1
	netmask 255.255.255.128

auto eth2
iface eth2 inet static
	address 192.205.0.1
	netmask 255.255.248.0

```

##### Seastone

```
auto eth0
iface eth0 inet static
	address 192.206.36.3
	netmask 255.255.255.0
gateway 192.206.36.1

auto eth1
iface eth1 inet static
	address 192.206.32.1
	netmask 255.255.252.0
```

#### Server

##### Doroki

```
auto eth0
iface eth0 inet static
	address 192.206.8.2
	netmask 255.255.255.252
gateway 192.206.8.1
```

##### Fukurou

```
auto eth0
iface eth0 inet static
	address 192.206.48.2
	netmask 255.255.255.252
gateway 192.206.48.1
```

#### Client

##### Blueno

```

auto eth0
iface eth0 inet static
	address 192.205.32.2
	netmask 255.255.252.0
	gateway 192.205.32.1

```

##### CIPHER

```
auto eth0
iface eth0 inet static
	address 192.205.128.2
	netmask 255.255.252.0
gateway 192.205.128.1

```

##### Jipangu

```
auto eth0
iface eth0 inet static
	address 192.205.8.2
	netmask 255.255.255.128
gateway 192.205.8.1
```

##### COURTYARD

```
auto eth0
iface eth0 inet static
	address 192.205.0.3
	netmask 255.255.248.0
gateway 192.205.0.1

```

##### CALMBELT

```
auto eth0
iface eth0 inet static
	address 192.205.0.2
	netmask 255.255.248.0
gateway 192.205.0.1

```

##### ENIESLOBBY

```
auto eth0
iface eth0 inet static
	address 192.206.36.2
	netmask 255.255.255.0
gateway 192.206.36.1
```

##### ELENA

```
auto eth0
iface eth0 inet static
	address 192.206.32.2
	netmask 255.255.252.0
gateway 192.206.32.1
```

##### JABRA

```
auto eth0
iface eth0 inet static
	address 192.206.4.2
	netmask 255.255.252.0
gateway 192.206.4.1
```

##### MAINGATE

```
auto eth0
iface eth0 inet static
	address 192.206.0.2
	netmask 255.255.254.0
gateway 192.206.0.1
```

##### JORGE

```
auto eth0
iface eth0 inet static
	address 192.206.2.2
	netmask 255.255.254.0
gateway 192.206.2.1
```

### Routing

##### Foosha

##### Water7
```

echo 'nameserver 192.168.122.1' > /etc/resolv.conf

route add -net 192.205.8.0 netmask 255.255.255.128 gw 192.205.16.2

route add -net 192.205.0.0 netmask 255.255.248.0 gw 192.205.16.2

```
##### GUANHAO

```
echo 'nameserver 192.168.122.1' > /etc/resolv.conf

route add -net 192.206.2.0 netmask 255.255.255.240 gw 192.206.0.3

route add -net 192.206.48.0 netmask 255.255.255.252 gw 192.206.40.2

route add -net 192.206.36.0 netmask 255.255.255.0 gw 192.206.40.2

route add -net 192.206.32.0 netmask 255.255.252.0 gw 192.206.40.2

```

##### OIMO

```                                  

echo 'nameserver 192.168.122.1' > /etc/resolv.conf

route add -net 192.206.32.0 netmask 255.255.252.0 gw 192.206.36.3
```


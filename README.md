| Nama    | NRP     | 
| ------- | ------- | 
| Imam Nurhadi    | 5027221046     | 
| Jojo     | 5027221062     |

# VLSM - GN3
Teknik subnetting yang dikenal sebagai Variable Length Subnet Masking (VLSM) merupakan teknik yang digunakan untuk memaksimalkan pembagian alamat IP di dalam jaringan. Netmask besar disesuaikan dengan banyaknya komputer atau host yang membutuhkan alamat IP.
VLSM membagi jaringan besar menjadi subnet yang lebih kecil. Setiap subnet kemudian diberi netmask yang sesuai dengan jumlah host yang dibutuhkannya. Dengan demikian, netmask dengan jumlah host yang lebih besar akan memiliki bitmask yang lebih sedikit, sementara netmask dengan jumlah host yang lebih sedikit akan memiliki bitmask yang lebih besar.

Metode VLSM dilakukan menggunakan platform GNS3. Berikut adalah penjelasan lebih lanjutnya : 
## Tree
Berikut adalah tree untuk pembagian IP dimulai dari 10.78.0.0/20
![vlsmtree-it29](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/143849730/010c5484-f433-46b8-b9ba-bbdf45a2eae5)
## Pembagian IP
Berikut adalah pembagian IP yang diperoleh dari hasil pemecahan tree menjadi jaringan yang lebih kecil :
![image](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/143849730/20e9dfe3-8102-421e-9eeb-bb85d61c4241)
## Konfigurasi Network 
**JAWA**
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet dhcp

#A3
auto eth1
iface eth1 inet static
address 10.78.21.197
netmask 255.255.255.252

#A2
auto eth2
iface eth2 inet static
address 10.78.21.193
netmask 255.255.255.252

#A1
auto eth3
iface eth3 inet static
address 10.78.21.189
netmask 255.255.255.252
```
**SULAWESI**
```
auto lo
iface lo inet loopback

#A1
auto eth0
iface eth0 inet static
address 10.78.21.190
netmask 255.255.255.252
gateway 10.78.21.189

#A6
auto eth1
iface eth1 inet static
address 10.78.21.161
netmask 255.255.255.248

#A4
auto eth2
iface eth2 inet static
address 10.78.20.1
netmask 255.255.255.128
```
**KALIMANTAN**
```
auto lo
iface lo inet loopback

#A2
auto eth0
iface eth0 inet static
address 10.78.21.194
netmask 255.255.255.252
gateway 10.78.21.193

#A9
auto eth1
iface eth1 inet static
address 10.78.21.201
netmask 255.255.255.252
```
**SUMATERA**
```
auto lo
iface lo inet loopback

#A3
auto eth0
iface eth0 inet static
address 10.78.21.198
netmask 255.255.255.252
gateway 10.78.21.197

#A16
auto eth1
iface eth1 inet static
address 10.78.21.205
netmask 255.255.255.252

#A18
auto eth2
iface eth2 inet static
address 10.78.21.65
netmask 255.255.255.224
```
**PC-Marisa**
```
#A4
auto eth0
iface eth0 inet static
address 10.78.20.2
netmask 255.255.255.128
gateway 10.78.20.1
```
**PC-Gorontalo**
```
#A4
auto eth0
iface eth0 inet static
address 10.78.20.3
netmask 255.255.255.128
gateway 10.78.20.1
```
**MALUKU-UTARA**
```
auto lo
iface lo inet loopback

#A4
auto eth0
iface eth0 inet static
address 10.78.20.4
netmask 255.255.255.128
gateway 10.78.20.1

#A5
auto eth1
iface eth1 inet static
address 10.78.0.1
netmask 255.255.248.0
```
**Tobelo**
```
#A5
auto eth0
iface eth0 inet static
address 10.78.0.2
netmask 255.255.248.0
gateway 10.78.0.1
```
**Morotai**
```
#A5
auto eth0
iface eth0 inet static
address 10.78.0.3
netmask 255.255.248.0
gateway 10.78.0.1
```
**Ternate**
```
#A5
auto eth0
iface eth0 inet static
address 10.78.0.4
netmask 255.255.248.0
gateway 10.78.0.1
```
**MAKASSAR**
```
auto lo
iface lo inet loopback

#A6
auto eth0
iface eth0 inet static
address 10.78.21.162
netmask 255.255.255.248
gateway 10.78.21.161

#A7
auto eth1
iface eth1 inet static
address 10.78.21.169
netmask 255.255.255.248
```
**Galesong**
```
#A7
auto eth0
iface eth0 inet static
address 10.78.21.170
netmask 255.255.255.248
gateway 10.78.21.169
```
**Topejawa**
```
#A7
auto eth0
iface eth0 inet static
address 10.78.21.171
netmask 255.255.255.248
gateway 10.78.21.169
```
**BELAWA**
```
auto lo
iface lo inet loopback

#A6
auto eth0
iface eth0 inet static
address 10.78.21.163
netmask 255.255.255.248
gateway 10.78.21.161

#A8
auto eth1
iface eth1 inet static
address 10.78.21.1
netmask 255.255.255.192
```
**Madini**
```
#A8
auto eth0
iface eth0 inet static
address 10.78.21.2
netmask 255.255.255.192
gateway 10.78.21.1
```
**Baru**
```
#A8
auto eth0
iface eth0 inet static
address 10.78.21.3
netmask 255.255.255.192
gateway 10.78.21.1
```
**KALIMANTAN-UTARA**
```
auto lo
iface lo inet loopback

#A9
auto eth0
iface eth0 inet static
address 10.78.21.202
netmask 255.255.255.252
gateway 10.78.21.201

#A10
auto eth1
iface eth1 inet static
address 10.78.18.1
netmask 255.255.255.0

#A11
auto eth2
iface eth2 inet static
address 10.78.21.181
netmask 255.255.255.252
```
**Selimau**
```
#A10
auto eth0
iface eth0 inet static
address 10.78.18.2
netmask 255.255.255.0
gateway 10.78.18.1
```
**KALIMANTAN-TIMUR**
```
auto lo
iface lo inet loopback

#A11
auto eth0
iface eth0 inet static
address 10.78.21.182
netmask 255.255.255.252
gateway 10.78.21.181


#A12
auto eth1
iface eth1 inet static
address 10.78.21.177
netmask 255.255.255.252

#A13
auto eth2
iface eth2 inet static
address 10.78.16.1
netmask 255.255.254.0
```
**Bangkirai**
```
#A13
auto eth0
iface eth0 inet static
address 10.78.16.2
netmask 255.255.254.0
gateway 10.78.16.1
```
**Lamaru**
```
#A13
auto eth0
iface eth0 inet static
address 10.78.16.3
netmask 255.255.254.0
gateway 10.78.16.1
```
**KALIMANTAN-SELATAN**
```
auto lo
iface lo inet loopback

#A12
auto eth0
iface eth0 inet static
address 10.78.21.178
netmask 255.255.255.252
gateway 10.78.21.178

#A14
auto eth1
iface eth1 inet static
address 10.78.21.97
netmask 255.255.255.224

#A15
auto eth2
iface eth2 inet static
address 10.78.8.1
netmask 255.255.248.0
```
**Angsana**
```
#A14
auto eth0
iface eth0 inet static
address 10.78.21.98
netmask  255.255.255.224
gateway 10.78.21.97
```
**Bajuin**
```
#A15
auto eth0
iface eth0 inet static
address 10.78.8.2
netmask 255.255.248.0
gateway 10.78.8.1
```
**Takisung**
```
#A15
auto eth0
iface eth0 inet static
address 10.78.8.3
netmask 255.255.248.0
gateway 10.78.8.1
```
**Batakan**
```
#A15
auto eth0
iface eth0 inet static
address 10.78.8.4
netmask 255.255.248.0
gateway 10.78.8.1
```
**LAMPUNG**
```
auto lo
iface lo inet loopback

#A16
auto eth0
iface eth0 inet static
address 10.78.21.206
netmask 255.255.255.252
gateway 10.78.21.205

#A17
auto eth1
iface eth1 inet static
address 10.78.19.1 
netmask 255.255.255.0
```
**Sebuku**
```
#A17
auto eth0
iface eth0 inet static
address 10.78.19.2 
netmask 255.255.255.0
gateway 10.78.19.1
```
**Sebesi**
```
#A17
auto eth0
iface eth0 inet static
address 10.78.19.3 
netmask 255.255.255.0
gateway 10.78.19.1
```
**Samosir**
```
#A18
auto eth0
iface eth0 inet static
address 10.78.21.66
netmask 255.255.255.224
gateway 10.78.21.65
```
**Sibandang**
```
#A18
auto eth0
iface eth0 inet static
address 10.78.21.67
netmask 255.255.255.224
gateway 10.78.21.65
```
**SUMATERA-UTARA**
```
auto lo
iface lo inet loopback

#A18
auto eth0
iface eth0 inet static
address 10.78.21.68
netmask 255.255.255.224
gateway 10.78.21.65

#19
auto eth1
iface eth1 inet static
address 10.78.21.185
netmask 255.255.255.252
```
**ACEH**
```
auto lo
iface lo inet loopback

#19
auto eth0
iface eth0 inet static
address 10.78.21.186
netmask 255.255.255.252
gateway 10.78.21.185

#20
auto eth1
iface eth1 inet static
address 10.78.20.129 
netmask 255.255.255.128

#21
auto eth2
iface eth2 inet static
address 10.78.21.129
netmask 255.255.255.224
```
**Starland**
```
auto eth0
iface eth0 inet static
address 10.78.20.132
netmask 255.255.255.128
gateway 10.78.20.129
```
**Enang-Enang**
```
auto eth0
iface eth0 inet static
address 10.78.20.131 
netmask 255.255.255.128
gateway 10.78.20.129
```
**Berawanng-Tampu**
```
auto eth0
iface eth0 inet static
address 10.78.20.130 
netmask 255.255.255.128
gateway 10.78.20.129
```
**Sabang**
```
auto eth0
iface eth0 inet static
address 10.78.21.130
netmask 255.255.255.224
gateway 10.78.21.129
```
**Lambaro**
```
auto eth0
iface eth0 inet static
address 10.78.21.131
netmask 255.255.255.224
gateway 10.78.21.129
```

## Routing
Routing yang dilakukan hanya pada Sulawesi dikarenakan routing pada Kalimantan dan Sumatera tidak berhasil. Alhasil, node hanya dapat melakukan ping antar sesama node di area(A1-A21) yang sama. Sementara pada Sulawesi, node yang berbeda area berhasil melakukan ping satu sama lain, bukan hanya pada area yang sama saja. Akan tetapi, node dari Sulawesi tidak bisa melakukan ping terhadap node di Kalimantan dan Sumatera.<br>
**JAWA**
```
route add -net 10.78.20.0 netmask 255.255.255.128 gw 10.78.21.190
route add -net 10.78.0.0 netmask 255.255.248.0 gw 10.78.21.190
route add -net 10.78.21.160 netmask 255.255.255.248 gw 10.78.21.190
route add -net 10.78.21.168 netmask 255.255.255.248 gw 10.78.21.190
route add -net 10.78.21.0 netmask 255.255.255.192 gw 10.78.21.190

#KALIMANTAN
route add -net 10.78.21.200 netmask 255.255.255.252 gw 10.78.21.194
route add -net 10.78.18.0 netmask 255.255.255.0 gw 10.78.21.194
route add -net 10.78.21.180 netmask 255.255.255.252 gw 10.78.21.194
route add -net 10.78.21.176 netmask 255.255.255.252 gw 10.78.21.194
route add -net 10.78.16.0 netmask 255.255.254.0 gw 10.78.21.194
route add -net 10.78.21.96 netmask 255.255.255.224 gw 10.78.21.194
route add -net 10.78.8.0 netmask 255.255.248.0 gw 10.78.21.194

#SUMATERA
route add -net 10.78.21.204 netmask 255.255.255.252 gw 10.78.21.198
route add -net 10.78.19.0 netmask 255.255.255.0 gw 10.78.21.198
route add -net 10.78.21.64 netmask 255.255.255.224 gw 10.78.21.198
route add -net 10.78.21.184 netmask 255.255.255.252 gw 10.78.21.198
route add -net 10.78.20.128 netmask 255.255.255.128 gw 10.78.21.198
route add -net 10.78.21.128 netmask 255.255.255.224 gw 10.78.21.198
```
**SULAWESI**
```
#Maluku-Utara
route add -net 10.78.0.0 netmask 255.255.248.0 gw 10.78.20.4

#Makassar
route add -net 10.78.21.168 netmask 255.255.255.248 gw 10.78.21.162

#Belawa
route add -net 10.78.21.0 netmask 255.255.255.192 gw 10.78.21.163
```
**MALUKU-UTARA**
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.173.21.190
```
**BELAWA**
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.173.21.190
```
**MAKASSAR**
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.173.21.190
```

## Cisco Packet Tracker
Dalam pengerjaan modul 4 ini, kami di berikan case untuk membuat topologi sebagai berikut 

![Gambar_modul.png](Resource/Gambar_modul.png)

Dalam topologi tersebut, dilakukan Classing untuk menentukan setiap subnetnya!
Berikut merupakan step pengerjaan kami untuk Classing subnet

## Pembagian Prefix dan IP
###Pembagian Prefix
#### Identifikasi Kebutuhan Jaringan
1. **Tentukan jumlah host yang diperlukan dalam setiap subnet.**
2. **Ketahui jumlah total subnet yang dibutuhkan.**

#### Menghitung Ukuran Subnet
Gunakan formula berikut untuk menentukan ukuran subnet:

\[ 2^n - 2  >= {jumlah host} \]

dimana \( n \) adalah jumlah bit yang dialokasikan untuk host.

**Contoh:**
Jika kamu membutuhkan 50 host, maka:

\[ 2^6 - 2 = 62 \]

Jadi, kamu membutuhkan 6 bit untuk host.

#### Menentukan Prefix

Subnet mask memiliki total 32-bit. Jadi, jika 6 bit dialokasikan untuk host, maka:

\[ 32 - 6 = 26 \]

Prefix akan menjadi /26.

###Pembagian IP
Hasil pembagian IP dan prefix kami sebagai berikut :
![IP_Tree.jpg](Resource/IP_Tree.jpg)
Pembagian ip lakukan dengan tahap :
1. Layer Terluar merupan hierarki tertinggi.
2. Lalu akan dibagi 2 cabang yaitu wilayah kanan kiri dan wilayah bawah, atau bisa disebut H1 dan H2. Ip ditentukan dengan ip address pada subnet dibagi dengan yang lebih rendah. Disini /14 dibagi dengan /16 hasilnya yaitu 26144/65536 dan hasilnya adalah 4. Maka hasil tersebut ditaruh pada bit ke 3 ip dengan subnet lebih kecil yaitu /16.
3. Selanjutnya kita bisa lihat lagi untuk subnet lebih tinggi akan dibagi 256, untuk hasilnya 32768/256 = 128 maka kita taruh ke bit 4 dari ip dengan subnet lebih rendah, jika masih cukup (batas maksimalnya /19 bit ke 4 adalah 255) maka kita taruh ke bit 4, jika tidak cukup sisanya ditaruh ke bit 3. Namun karena turunannya bit ke
4. Namun untuk ip dengan prefix /25 dan /28 kita bisa langsung taruh 128 ke ip prefix /28 karena tidak bisa dibagi 256 dan masih cukup untuk bit ke 4 dari /28 
## Tabel Subnet

| Subnet | Network ID       | Netmask            | Broadcast         | Range IP                        |
|--------|------------------|--------------------|-------------------|---------------------------------|
| A1     | 192.235.132.0    | 255.255.255.128    | 192.235.132.127   | 192.235.132.1 - 192.235.132.126 |
| A2     | 192.235.132.128  | 255.255.255.240    | 192.235.132.143   | 192.235.132.129 - 192.235.132.142 |
| A3     | 192.235.133.0    | 255.255.255.252    | 192.235.133.3     | 192.235.133.1 - 192.235.133.2   |
| A4     | 192.235.134.0    | 255.255.255.224    | 192.235.134.31    | 192.235.134.1 - 192.235.134.30  |
| A5     | 192.235.136.0    | 255.255.255.252    | 192.235.136.3     | 192.235.136.1 - 192.235.136.2   |
| A6     | 192.235.140.0    | 255.255.255.0      | 192.235.140.255   | 192.235.140.1 - 192.235.140.254 |
| A7     | 192.235.148.0    | 255.255.255.252    | 192.235.148.3     | 192.235.148.1 - 192.235.148.2   |
| A8     | 192.237.0.0      | 255.255.255.252    | 192.237.0.3       | 192.237.0.1 - 192.237.0.2       |
| A9     | 192.235.1.0      | 255.255.255.252    | 192.235.1.3       | 192.235.1.1 - 192.235.1.2       |
| A10    | 192.235.128.0    | 255.255.255.0      | 192.235.128.255   | 192.235.128.1 - 192.235.128.254 |
| A11    | 192.235.64.0     | 255.255.255.252    | 192.235.64.3      | 192.235.64.1 - 192.235.64.2     |
| A12    | 192.235.32.0     | 255.255.255.0      | 192.235.32.255    | 192.235.32.1 - 192.235.32.254   |
| A13    | 192.235.16.0     | 255.255.255.252    | 192.235.16.3      | 192.235.16.1 - 192.235.16.2     |
| A14    | 192.235.8.0      | 255.255.255.224    | 192.235.8.31      | 192.235.8.1 - 192.235.8.30      |
| A15    | 192.235.0.0      | 255.255.248.0      | 192.235.7.255     | 192.235.0.1 - 192.235.7.254     |
| A16    | 192.235.68.0     | 255.255.255.252    | 192.235.68.3      | 192.235.68.1 - 192.235.68.2     |
| A17    | 192.235.12.0     | 255.255.255.248    | 192.235.12.7      | 192.235.12.1 - 192.235.12.6     |
| A18    | 192.235.36.0     | 255.255.255.252    | 192.235.36.3      | 192.235.36.1 - 192.235.36.2     |
| A19    | 192.235.20.0     | 255.255.255.192    | 192.235.20.63     | 192.235.20.1 - 192.235.20.62    |
| A20    | 192.235.8.0      | 255.255.255.192    | 192.235.8.63      | 192.235.8.1 - 192.235.8.62      |
| A21    | 192.235.4.0      | 255.255.252.0      | 192.235.7.255     | 192.235.4.1 - 192.235.7.254     |

A. Penggabungan dengan metoded CIDR dan hasil pembagian prefix dan subnetting
1. Setiap wilayah dan jalur router memiliki A Class masing-masing dengan subnet yang cukup untuk dibagi IP nya terhadap beberapa host dan device.
2. Topologi dibagi 3 wilayah besar, yaitu kiri, tengah, dan kanan. DImana Sumatera merupakan wilayan kiri, kalimantan wilayah tengah, dan sulawesi wilayah kanan. JAWA? **JAWAAA ADALAH KUNCI**
3. Setelagh Class A sudah dibagi, setiap wilayah akan memiliki tahap penggabungan. 2 Class A akan digabung mejadi satu dengan syarat berdekatan dan mejadi CLass baru yaitu Class B.
4. Setelah setiap wilayah memiliki 1 Class B masing masing, maka akan dilakukan penggabungan lagi yaitu pada Class B setiap wilayah akan digabungkan dengan Class A terdekatnya.

Seperti inilah hasil penggabungan kami
## Penggabungan

### Tabel Subnet B
| Subnet | Gabungan dari  |         |        |                |Netmask Akhir |
|--------|----------------|---------|--------|----------------|--------------|
|        | 1              |         |2       |                |              |
|        | Subnet         | Netmask | Subnet | Netmask        |              |
| B1     | A1             | /25     | A2     | /28            | /24          |
| B2     | A14            | /27     | A15    | /21            | /20          |
| B3     | A20            | /26     | A21    | /22            | /21          |

### Tabel Subnet C
| Subnet | Gabungan dari |          |        |                | Netmask Akhir |
|--------|----------------|---------|--------|----------------|----------------|
|        | 1              |         | 2      |                |                |
|        | Subnet         | Netmask | Subnet | Netmask        |                |
| C1     | B1             | /24     | A3     | /30            | /23            |
| C2     | B2             | /20     | A13    | /30            | /19            |
| C3     | B3             | /21     | A17    | /30            | /20            |

### Tabel Subnet D
| Subnet | Gabungan dari  |         |        |                | Netmask Akhir  |
|--------|----------------|---------|--------|----------------|----------------|
|        | 1              |         | 2      |                |                |
|        | Subnet         | Netmask | Subnet | Netmask        |                |
| D1     | C1             | /23     | A4     | /27            | /22            |
| D2     | C2             | /19     | A12    | /23            | /18            |
| D3     | C3             | /20     | A19    | /26            | /19            |

### Tabel Subnet E
| Subnet | Gabungan dari |          |        |                | Netmask Akhir  |
|--------|----------------|---------|--------|----------------|----------------|
|        | 1              |         | 2      |                |                |
|        | Subnet         | Netmask | Subnet | Netmask        |                |
| E1     | D1             | /22     | A5     | /30            | /21            |
| E2     | D2             | /18     | A11    | /30            | /17            |
| E3     | D3             | /19     | A18    | /30            | /18            |

### Tabel Subnet F
| Subnet | Gabungan dari  |         |        |                | Netmask Akhir | 
|--------|----------------|---------|--------|----------------|----------------|
|        | 1              |         | 2      |                |                |
|        | Subnet         | Netmask | Subnet | Netmask        |                |
| F1     | E1             | /21     | A6     | /24            | /20            |
| F2     | E2             | /17     | A10    | /24            | /16            |
| F3     | E3             | /18     | A16    | /30            | /17            |

### Tabel Subnet G
| Subnet | Gabungan dari  |         |        |                | Netmask Akhir  |
|--------|----------------|---------|--------|----------------|----------------|
|        | 1              |         | 2      |                |                |
|        | Subnet         | Netmask | Subnet | Netmask        |                |
| G1     | F1             | /20     | A7     | /30            | /19            |
| G2     | F2             | /16     | A9     | /30            | /15            |

### Tabel Subnet H
| Subnet | Gabungan dari  |         |        |                | Netmask Akhir  |
|--------|----------------|---------|--------|----------------|----------------|
|        | 1              |         | 2      |                |                |
|        | Subnet         | Netmask | Subnet | Netmask        |                |
| H1     | G1             | /19     | F3     | /17            | /16            |
| H2     | G2             | /15     | A8     | /30            | /14            |

### Tabel Subnet I
| Subnet | Gabungan dari  |         |        |                | Netmask Akhir  |
|--------|----------------|---------|--------|----------------|----------------|
|        | 1              |         | 2      |                |                |
|        | Subnet         | Netmask | Subnet | Netmask        |                |
| I1     | H1             | /16     | H2     | /14            | /13            |

### Hasil CPT
Maka hasil cpt akan sebagai berikut 
![Gambar_CPT.png](Resource/Gambar_CPT.png)


### Routing
#### Subnetting
Dalam pengerjaan ini, kami melakukan subnetting dengan metode berikut :
1. Memilih interface yang dipilih, ```interface <Nama interface>```
2. Melakukan input ip address yang sudah di bagi dengan netmasknya sesuai pembagian prefix ```ip address <IP address> <Netmask>```
3. Perubahan di jalankan dengan command ```no shutdown``` atau bisa disingkat ```no sh``

Contoh penerapan :
```sh
int fa0/1
ip address 192.235.132.1 255.255.255.128
no sh
```
#### Routing
Dalam pengerjaan ini, kami melakukan subnetting dengan metode berikut :
1. Memilih rute untuk di set up ```ip route <Destination network ID> <Netmask> <Gateway>```
   - Destination network ID adalah network ID yang kita tuju, jika A1 menuju A5 maka A5 yang dimasukkan
   - Netmask adalah netmask dari node yang dituju
   - Gateaway merupakan ip dari interface yang menghalangi rute kita diawal

Contoh penerapan melakukan route ACEH menuju SUMATERA :
Router ACEH
```sh
ip route 192.235.134.0 255.255.255.224 192.235.133.1
```
Router SUMATERA
```sh
ip route 192.235.133.0 255.255.255.252 192.235.134.2
```

Router ACEH menuju node A4 karena sebelum SUMATERA dengan gateaway fa0/1 SUMATERA-UTARA
Router SUMATERA menuju node A3 karena sebelum ACEH dengan gateaway fa0/0 SUMATERA-UTARA

### Praktek Langsung
https://drive.google.com/file/d/1Hfbzz-_OUvJXV-50-y5HRVHpSPsXdkxm/view?usp=drive_link

atau bisa download di resource

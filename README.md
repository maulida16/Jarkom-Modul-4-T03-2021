# Jarkom-Modul-4-T03-2021

![image](https://user-images.githubusercontent.com/73152464/143670615-8cc86580-1726-4e49-a348-687e66012381.png)

- Soal shift dikerjakan pada Cisco Packet Tracer dan GNS3 menggunakan metode perhitungan CLASSLESS yang berbeda.
Keterangan: Bila di CPT menggunakan VLSM, maka di GNS3 menggunakan CIDR atau Sebaliknya
- Jika tidak ada pemberitahuan revisi soal dari asisten, berarti semua soal BERSIFAT BENAR dan DAPAT DIKERJAKAN.
- Untuk di GNS3 CLOUD merupakan NAT1 jangan sampai salah agar bisa terkoneksi internet.
- Pembagian IP menggunakan Prefix IP yang telah ditentukan pada modul pengenalan
- Pembagian IP dan routing harus SE-EFISIEN MUNGKIN.
- Pastikan semua NODE pada GNS3 dapat melakukan ping ke its.ac.id

## VLSM

### Perhitungan VLSM
![image](https://user-images.githubusercontent.com/61416036/143677577-688734da-54f2-4a0e-b434-cee5dfdc5d05.png)
Dari topologi pada soal, kami memberikan pengelompokan subnet dan penamaan tiap subnet seperti gambar diatas.
| Subnet | Jumlah IP | Netmask |
| --- | --- | --- |
| A4 | 2021 | /21 |
| A1 | 1001 | /22 |
| A2 | 701 | /22 |
| A7 | 521 | /22 |
| A8 | 721 | /22 |
| A12 | 502 | /23 |
| A9 | 252 | /24 |
| A3 | 101 | /25 |
| A11 | 13 | /28 |
| A5 | 2 | /30 |
| A6 | 2 | /30 |
| A10 | 2 | /30 |
| A13 | 2 | /30 |
| A14 | 2 | /30 |
| A15 | 2 | /30 |
| Total | 5845 | /19 |

Bila dilihat dari tabel, kita akan menggunakan netmask /19 untuk memberikan pengalamatan IP pada 15 subnet.

![image](https://user-images.githubusercontent.com/61416036/143677910-6aea6f5c-f902-4e77-898d-d50b73048ff4.png)
Sehingga tree yang digunakan adalah sebagai berikut.

Sesuai dengan soal, berikut topologi jaringan di Cisco Packet Tracer

![image](https://user-images.githubusercontent.com/73152464/143673829-9277abf5-2534-4f87-8eb6-8dcc08a54e81.png)

Dengan konfigurasi IP di masing-masing router adalah sebagai berikut:

- Foosha
 1. Mengarah ke Blueno dengan IP Address 10.43.16.1 dan Subnet Mask 255.255.252.0
 2. Mengarah ke Water7 dengan IP Address 10.43.0.5 dan Subnet Mask 255.255.255.252
 3. Mengarah ke Doriki dengan IP Address 10.43.0.21 dan Subnet Mask 255.255.255.252
 4. Mengarah ke Guanhao dengan IP Address 10.43.0.13 dan Subnet Mask 255.255.255.252
- Guanhao
 1. Mengarah ke Jabra dengan IP Address 10.43.28.1 dan Subnet Mask 255.255.252.0
 2. Mengarah ke Maingate dan Alabasta dengan IP Address 10.43.2.1 dan Subnet Mask 255.255.254.0
 3. Mengarah ke Oiimo dengan IP Address 10.43.0.9 dan Subnet Mask 255.255.255.252
 4. Mengarah ke Foosha dengan IP Address 10.43.0.14 dan Subnet Mask 255.255.255.252
- Alabasta
 1. Mengarah ke Guanhao dengan IP Address 10.43.2.4 dan Subnet Mask 255.255.254.0
 2. Mengarah ke Jorge dengan IP Address 10.43.0.49 dan Subnet Mask 255.255.255.240
- Oiimo
 1. Mengarah ke Guanhao dengan IP Address 10.43.0.10 dan Subnet Mask 255.255.255.252
 2. Mengarah ke Ennieslobby dan Seastone dengan IP Address 10.43.1.1 dan Subnet Mask 255.255.255.0
 3. Mengarah ke Fukurou dengan IP Address 10.43.0.17 dan Subnet Mask 255.255.255.252
- Seastone
 1. Mengarah ke Oiimo dengan IP Address 10.43.1.3 dan Subnet Mask 255.255.255.0
 2. Mengarah ke Elena dengan IP Address 10.43.12.1 dan Subnet Mask 255.255.252.0
- Water7
 1. Mengarah ke Foosha dengan IP Address 10.43.0.6 dan Subnet Mask 255.255.255.252
 2. Mengarah ke Pucci dengan IP Address 10.43.0.1 dan Subnet Mask 255.255.255.252
 3. Mengarah ke Cipher dengan IP Address 10.43.24.1 dan Subnet Mask 255.255.252.0
- Pucci
 1. Mengarah ke Water7 dengan IP Address 10.43.0.2 dan Subnet Mask 255.255.255.252
 2. Mengarah ke Courtyard dan Calmbelt dengan IP Address 10.43.8.1 dan Subnet Mask 255.255.248.0
 3. Mengarah ke Jipangu dengan IP Address 10.43.0.129 dan Subnet Mask 255.255.255.128

Konfigurasi di masing-masing PC adalah sebagai berikut:

- Blueno

![image](https://user-images.githubusercontent.com/73152464/143674447-05a4fe50-ce89-4cf7-b553-32fbddcc1080.png)
 
- Cipher

![image](https://user-images.githubusercontent.com/73152464/143674465-d37d9406-c32b-4634-af90-02bba046c795.png)

- Jipangu

![image](https://user-images.githubusercontent.com/73152464/143674481-48901913-487f-495a-830f-ddd73be69a46.png)

- Courtyard

![image](https://user-images.githubusercontent.com/73152464/143674494-b84b1d4b-dc75-42f2-a249-b3acda3d223d.png)

- Calmbelt

![image](https://user-images.githubusercontent.com/73152464/143674511-cd41d622-d5e3-4e2b-ada2-917977076b06.png)

- Jabra

![image](https://user-images.githubusercontent.com/73152464/143674522-dc195dc1-bced-40d2-bf67-ee13964e6f5b.png)

- Elena

![image](https://user-images.githubusercontent.com/73152464/143674539-0b2910b4-ff98-4102-b571-022c4788bb4d.png)

- Ennieslobby

![image](https://user-images.githubusercontent.com/73152464/143674552-716ba85b-f395-4cd1-9124-d61bb96f4ebd.png)

- Jorge

![image](https://user-images.githubusercontent.com/73152464/143674565-1157e787-703d-4294-8b8a-bba955291e02.png)

- Maingate

![image](https://user-images.githubusercontent.com/73152464/143674578-c7fc861f-b028-4ee2-b109-36b750df95c5.png)

- Fukurou

![image](https://user-images.githubusercontent.com/73152464/143674586-dedb0ac3-36ef-4e1d-9130-1f771bd591f6.png)

- Doriki

![image](https://user-images.githubusercontent.com/73152464/143674596-ff57ed7f-8fe1-4fbf-a07c-57ddf3b898b7.png)

Pengaturan Routing dari tiap-tiap router:

- Foosha

![image](https://user-images.githubusercontent.com/73152464/143679276-0825f194-f994-4257-b762-48a527763317.png)

![image](https://user-images.githubusercontent.com/73152464/143679288-5d22b28a-a29e-4000-b86e-f2c419960b36.png)

![image](https://user-images.githubusercontent.com/73152464/143679302-dfceb918-a8b5-4483-b065-68a2de146a98.png)

- Guanhao

![image](https://user-images.githubusercontent.com/73152464/143674804-d3aa3e67-a4a9-4114-a7e5-eb15b3c8229b.png)

![image](https://user-images.githubusercontent.com/73152464/143674811-e65ec6c0-346e-4abd-81ed-8bce72af3600.png)

- Alabasta

![image](https://user-images.githubusercontent.com/73152464/143674827-27bcebab-33d5-4b4e-8d32-0779e34bcf7a.png)

- Oiimo

![image](https://user-images.githubusercontent.com/73152464/143674831-a76ccd00-c490-4bd5-a936-5fe6212c78a5.png)

- Seastone

![image](https://user-images.githubusercontent.com/73152464/143674840-b82764c5-7688-41e8-ba3b-e6e3e564f832.png)

- Water7

![image](https://user-images.githubusercontent.com/73152464/143674845-e1140f59-bc22-4726-ad13-e4282ef2d087.png)

- Pucci

![image](https://user-images.githubusercontent.com/73152464/143674854-0bd67d39-f13e-4c60-a8d4-c56c9dd3b3b6.png)


Testing dari Jipangu ke Ennieslobby dengan Simulator

![image](https://user-images.githubusercontent.com/73152464/143674894-008a706c-ebdf-4e41-b9aa-21ef76b200d2.png)

Dari Ennieslobby kembali ke Jipangu

![image](https://user-images.githubusercontent.com/73152464/143674910-cc4b4678-d94e-4db9-8d64-f4787a42b13c.png)



## CIDR

### Perhitungan CIDR
Dari proses penggabungan didapat subnet terbesar dengan netmask /15.
![image](https://user-images.githubusercontent.com/61416036/143678008-850f17e2-76f1-429a-9a34-5b7e204222e4.png)

Sehingga tree yang digunakan adalah sebagai berikut.
![image](https://user-images.githubusercontent.com/61416036/143678137-9ecde6a9-7ce0-4f9d-aaf1-d83496a5758d.png)

Pembagian IP adalah sebagai berikut
| Subnet | Alamat IP | Netmask |
| --- | --- | --- |
| A4 | 10.43.8.0 | /21 |
| A1 | 10.43.16.0 | /22 |
| A2 | 10.43.24.0 | /22 |
| A7 | 10.43.28.0 | /22 |
| A8 | 10.43.12.0 | /22 |
| A12 | 10.43.2.0 | /23 |
| A9 | 10.43.1.0 | /24 |
| A3 | 10.43.0.128 | /25 |
| A11 | 10.43.0.48 | /28 |
| A5 | 10.43.0.0 | /30 |
| A6 | 10.43.0.4 | /30 |
| A10 | 10.43.0.8 | /30 |
| A13 | 10.43.0.12 | /30 |
| A14 | 10.43.0.16 | /30 |
| A15 | 10.43.0.20 | /30 |

#### Topologi GNS3
![topologi](https://user-images.githubusercontent.com/73921231/143685696-28c2edb9-6743-4c45-beb9-34123648f1b6.jpg)

#### `route -n`

##### Foosha
![foosha](https://user-images.githubusercontent.com/73921231/143685755-4cf815fd-3fdc-4b5f-8468-7be2d425fa7b.jpg)

##### Guanhao
![guanhao](https://user-images.githubusercontent.com/73921231/143685782-080d030d-6afd-477c-adf0-4d987c3713f2.jpg)

##### Oimo
![oimo](https://user-images.githubusercontent.com/73921231/143685805-df3b03e0-9165-4696-9a89-1c67ac2ebce2.jpg)

##### Water7
![water7](https://user-images.githubusercontent.com/73921231/143685820-18548ef2-0ddf-4b0d-bbef-b20177eae299.jpg)

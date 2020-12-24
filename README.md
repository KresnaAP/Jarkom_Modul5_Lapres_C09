# Modul5_C09
Kelompok C09
- 05111840000028  M. Frediansyah Sinaga
- 05111840000072  Kresna Adhi Pramana

Praktikum Modul 5 berupa *Firewall*.


## Soal
* Tugas pertama kalian yaitu membuat topologi jaringan sesuai dengan rancangan yang diberikan
    Bibah seperti dibawah ini :
    ![Soal](img/soal.PNG)
    Keterangan : 
    * SURABAYA diberikan IP TUNTAP
    * MALANG merupakan DNS Server diberikan IP DMZ
    * MOJOKERTO merupakan DHCP Server diberikan IP DMZ
    * MADIUN dan PROBOLINGGO merupakan WEB Server
    * Setiap Server diberikan memory sebesar 128M
    * Client dan Router diberikan memori sebesar 96M
    * Jumlah host pada subnet SIDOARJO 200 Host
    * Jumlah host pada subnet GRESIK 210 Host
* Karena kalian telah mempelajari Subnetting dan Routing, Bibah meminta kalian untuk membuat
    topologi tersebut menggunakan teknik CIDR atau VLSM . Setelah melakukan subnetting, (C) kalian
    juga diharuskan melakukan routing agar setiap perangkat pada jaringan tersebut dapat terhubung.
* Tugas berikutnya adalah memberikan ip pada subnet SIDOARJO dan GRESIK secara dinamis
    menggunakan bantuan DHCP SERVER (Selain subnet tersebut menggunakan ip static). Kemudian
    kalian mengingat bahwa kalian harus setting DHCP RELAY pada router yang menghubungkannya,
    seperti yang kalian telah pelajari di masa lalu.

___

1. Agar topologi yang kalian buat dapat mengakses keluar, kalian diminta untuk mengkonfigurasi
    SURABAYA menggunakan iptables, namun Bibah tidak ingin kalian menggunakan
    MASQUERADE.
2. Kalian diminta untuk mendrop semua akses SSH dari luar Topologi (UML) Kalian pada server
    yang memiliki ip DMZ (DHCP dan DNS SERVER) pada SURABAYA demi menjaga keamanan.
3. Karena tim kalian maksimal terdiri dari 3 orang, Bibah meminta kalian untuk membatasi DHCP
    dan DNS server hanya boleh menerima maksimal 3 koneksi ICMP secara bersamaan yang berasal dari
    mana saja menggunakan iptables pada masing masing server , selebihnya akan di DROP.
    kemudian kalian diminta untuk membatasi akses ke MALANG yang berasal dari SUBNET
    SIDOARJO dan SUBNET GRESIK dengan peraturan sebagai berikut:
4. Akses dari subnet SIDOARJO hanya diperbolehkan pada pukul 07.00 - 17.00 pada hari Senin
    sampai Jumat.
5. Akses dari subnet GRESIK hanya diperbolehkan pada pukul 17.00 hingga pukul 07.00 setiap
    harinya.
    Selain itu paket akan di REJECT.
    Karena kita memiliki 2 buah WEB Server, 
6. Bibah ingin SURABAYA disetting sehingga setiap
    request dari client yang mengakses DNS Server akan didistribusikan secara bergantian pada
    PROBOLINGGO port 80 dan MADIUN port 80.
7. Bibah ingin agar semua paket didrop oleh firewall (dalam topologi) tercatat dalam log pada setiap
    UML yang memiliki aturan drop.
    Bibah berterima kasih kepada kalian karena telah mau membantunya. Bibah juga mengingatkan agar
    semua aturan iptables harus disimpan pada sistem atau paling tidak kalian menyediakan script sebagai
    backup.
    
## Jawaban

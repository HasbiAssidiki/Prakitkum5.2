# Prakitkum5.2
## Dictionary
## Input data mahasiswa

## Flowchart  
![Screenshot (50)](https://user-images.githubusercontent.com/115614317/204571606-fe03a706-780c-4cb6-8cc2-2e58dfa397d0.png)  

## Penjelasan Program
* `data = {}`, adalah sebuah variabel bertipe *dictionary Kosong / tidak bervalue*, ini berfungsi untuk menampung inputan kyboard/user.

* `while True:`, adalah sebuah perulangan while, yang akan terus mengulang karna nilai nya *True* dan nanti akan berhenti dengan perintah *break*

* `print()`, artinya output kosong untuk membuat jarak antara outputan lain.

* `lanjut = str(input('(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar: '))`, artinya sebuah variabel bernama/inisial 'lanjut' yang di inputkan data bertipe string dengan tampilan input *(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar:*.

* `if lanjut.lower() == 't':`

    `print('Tambah Data')`

    `nama = str(input('Nama\t\t: '))`

    `nim = str(input('NIM\t\t: '))`

    `uts = int(input('Nilai UTS\t: '))`

    `uas = int(input('Nilai UAS\t: '))`

    `tugas = int(input('Nilai Tugas\t: '))`

    `akhir = round(float((tugas*0.3)+(uts*0.35)+(uas*0.35)),2)`

    `data[nama]=nim, uts, uas, tugas, akhir`

, perintah `lower()` memiliki arti yakni untuk membuat semua yang di inputkan menjadi huruf kecil,dan `(\t)` adalah tab berfungsi untuk mengatur jarak spasi, jadi arti keseluruhan nya yakni jika variabel *inputan pada varibel `lanjut`.lower() seperti `'t'` maka tampilkan `Tambah Data`, input nama bertipe data string `Nama: `, input nim bertipe data string `NIM: `, input uts bertipe data integer `Nilai UTS: `, input UAS bertipe data integer `Nilai UAS: `, input tugas bertipe data integer `Nilai Tugas: `. Pada  varibel `akhir` menggunakan operator aritmatika dan bertipe data float, dan juga memiliki perintah `round(,2)` yang memiliki arti yakni untuk mengambil angka dibelakang koma sebanyak yang kita inginkan disana saya hanya menginginkan 2 angka di belakang koma, terakhir kita juga memasukan inputan tadi kedalam *data[nama]* agar nanti masuk kedalam `data = {}` atau dictionary kosong yang tadi dibuat.

* `elif lanjut.lower() == 'l':`, artinya jika variabel *inputan pada varibel 'lanjut'*.lower() seperti *'l'* maka.....*

* `if data.items():`

    `print('Daftar Nilai')`

    `print('='*84)`

    `print(f"|{'NO':^4}|{'NAMA':^20}|{'NIM':^20}|{'TUGAS':^10}|{'UTS':^6}|{'UAS':^6}|{'AKHIR':^10}|")`

    `print('='*84)`

    `n = 0`

    `for a in data.items():`

    `n += 1`

    `print("|{no:^4}|{0:^20}|{1:^20}|{2:^10}|{3:^6}|{4:^6}|{5:^10}|"`

    `.format(a[0][:13], a[1][0], a[1][1], a[1][2], a[1][3], a[1][4], no = n))`

    `print('='*84)` 

, perintah `items()` berfungsi untuk mengembalikan daftar yang berisi tuple untuk setiap pasangan nilai keys, ini berarti jika didalam items `data` dictionary ada sebuah data maka tampilkan : *'Daftar Nilai'*, '='sebanyak 84 kali, (^)artinya untuk memposisikan ditengah, format NO-NAMA-NIM-TUGAS-UTS-UAS-AKHIR untuk angka pada format yakni posisi tampilannya. input varibel n berfungsi untuk outputan nomor nanti. perulangan for variabel 'a' di dalam data.items(): didalam proses perulangan ini pada variabel *n* akan ada proses assigment tambah 1, lalu output menggunakan format seperti sebelumnya tetapi di format ke(*a*index ke-0, *a*dimensi ke-1 index ke-0,*a*dimensi ke-1 index ke-1, *a*dimensi ke-1 index ke-2, *a*dimensi ke-1 index ke-3, *a*dimensi ke-1 index ke-4, dan `no` sama dengan `n`)

*   `else:`

    `print('Daftar Nilai')`

    `print('='*84)`

    `print(f"|{'NO':^4}|{'NAMA':^20}|{'NIM':^20}|{'TUGAS':^10}|{'UTS':^6}|{'UAS':^6}|{'AKHIR':^10}|")`

    `print('='*84)`

    `print(f"|{'TIDAK ADA DATA':^82}|")`

    `print('='*84)`

, artinya jika didalam items `data` dictionary ada sebuah data maka tampilkan: *'Daftar Nilai'*, '='sebanyak 84 kali, (^)artinya untuk memposisikan ditengah, format NO-NAMA-NIM-TUGAS-UTS-UAS-AKHIR untuk angka pada format yakni posisi tampilan nya. Print atau tampilkan menggunakan format 'TIDAK ADA DATA' : letaknya ditengah pada jarak 84.

* `elif lanjut.lower() == 'u':`

    `print("Ubah Data")`

    `nama = str(input('Nama\t\t: '))`

, artinya jika variabel *inputan pada varibel 'lanjut'*.lower() seperti *'u'* maka tampilkan *'Ubah Data'* dan juga input pada variabel `nama` bertipe data string,

* `if nama in data.keys():`

    `nim = str(input('NIM\t\t: '))`

    `uts = int(input('Nilai UTS\t: '))`

    `uas = int(input('Nilai UAS\t: '))`

    `tugas = int(input('Nilai Tugas\t: '))`

    `akhir = round(float((tugas*0.3)+(uts*0.35)+(uas*0.35)),2)`

    `data[nama] = nim, uts, uas, tugas, akhir`

, artinya jika inputan pada variabel `nama` sebelumnya ada di dalam data.keys() maka input variabel `nim` bertipe data string, `uts, uas, tugas` bertipe data integer dan `akhir` bertipe data float yang di kasih perintah `round()` sebelumnya sudah dibahas arti dari perintah tersebut, lalu kita inputkan pada `data` dictionary agar nanti data pada `data`dictionary berganti/terubah.

*   `else:`

    `print(f"Nama {nama} Tidak Tersedia")`

, artinya jika inputan pada variabel `nama` tidak ada dalam `data.keys` maka tampilkan Nama tidak tersedia menggunakan format (`nama`).

* `elif lanjut.lower() == 'h':`

    `print('Hapus Data')`

    `nama = str(input('Nama\t\t: '))`

, artinya jika variabel *inputan pada varibel 'lanjut'*.lower() seperti *'h'* maka tampilkan *'Hapus Data'* dan juga input pada variabel `nama` bertipe data string,

*   `if nama in data.keys():`

    `del data[nama]`

, artinya jika inputan pada variabel `nama` sebelumnya ada di dalam data.keys() maka gunakan perintah menghapus data pada dictionary `data`[nama].

*   `else:`

    `print(f"Nama {nama} Tidak Tersedia")`

, artinya jika inputan pada variabel `nama` tidak ada dalam `data.keys` maka tampilkan Nama tidak tersedia menggunakan format (`nama`).

* `elif lanjut.lower() == 'c':`

    `print('Data Cari')`

    `nama = str(input('Nama\t\t: '))`

, artinya jika variabel *inputan pada varibel 'lanjut'*.lower() seperti *'h'* maka tampilkan *'Data Cari'* dan juga input pada variabel `nama` bertipe data string,
*   `if nama in data.keys():`

    `print('='*79)`

    `print(f"|{'NAMA':^20}|{'NIM':^20}|{'TUGAS':^10}|{'UTS':^6}|{'UAS':^6}|{'AKHIR':^10}|")`

    `print('='*79)`

    `print("|{0:^20}|{1:^20}|{2:^10}|{3:^6}|{4:^6}|{5:^10}|"`

    `.format(nama, nim, tugas, uts, uas, akhir))`

    `print('='*79)`

, artinya jika inputan pada variabel `nama` sebelumnya ada di dalam data.keys() maka tampilkan : *'Cari Data'*, '='sebanyak 79 kali, (^)artinya untuk memposisikan ditengah, format NO-NAMA-NIM-TUGAS-UTS-UAS-AKHIR, untuk angka pada format yakni posisi tampilannya.

*   `else:`

    `print(f"Nama {nama} Tidak Tersedia")`

, artinya jika inputan pada variabel `nama` tidak ada dalam `data.keys` maka tampilkan Nama tidak tersedia menggunakan format (`nama`).

* `elif lanjut.lower() == 'k':`

    `print('Selesai')`

    `break`

, artinya jika variabel *inputan pada varibel 'lanjut'*.lower() seperti selain dari yang tersedia maka tampilkan 'Selesai' dan program pun berakhir.
      
* `else:`

    `print('Pilih tindakan yang tersedia')`

, artinya jika variabel *inputan pada varibel 'lanjut'*.lower() seperti selain dari yang tersedia maka tampilkan 'Pilih tindakan yang tersedia

## Program  

![Screenshot (36)](https://user-images.githubusercontent.com/115614317/204572751-37971775-e515-45d9-94ac-f3ea04c88470.png)  

![Screenshot (37)](https://user-images.githubusercontent.com/115614317/204572783-cd795412-ec16-41d0-9990-2b82f2407e5b.png)  

![Screenshot (38)](https://user-images.githubusercontent.com/115614317/204572841-9889762f-4239-4091-b167-5b855206d717.png)  

## Hasil Program

![Screenshot (39)](https://user-images.githubusercontent.com/115614317/204573575-b5a8df51-03fe-4f80-93fd-7660a7e576e5.png)

![Screenshot (40)](https://user-images.githubusercontent.com/115614317/204573597-522b2c1f-78ed-4903-9ab7-c6d564f347ca.png)

![Screenshot (41)](https://user-images.githubusercontent.com/115614317/204573616-1a200fa9-2df5-46b5-8351-a6a0f58aaaa3.png)

![Screenshot (42)](https://user-images.githubusercontent.com/115614317/204573643-a4a5d900-a69d-4150-87d5-d20ca56ed35a.png)

![Screenshot (43)](https://user-images.githubusercontent.com/115614317/204573698-8df45423-aeef-4565-862f-e019459b2bcc.png)


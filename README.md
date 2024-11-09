# Fitri Ramadhani
# NIM: 312410085
# Kelas: TI.24.A.1

# Program 1
Import library random untuk menghasilkan angka acak from random import random 

# Deskripsi Program
program ini bertujuan untuk menghasilkan dan menampilkan n bilangan acak yang lebih kecil dari 0.5. Berikut penjelasan dari tiap bagian kode:

1. Input: Program meminta pengguna untuk memasukkan sebuah bilangan bulat (n), yang merepresentasikan jumlah bilangan acak yang harus dihasilkan dan lebih kecil dari 0.5.

2. Inisialisasi Variabel: Variabel count diinisialisasi dengan nilai 0. Variabel ini digunakan untuk menghitung berapa banyak bilangan acak yang sudah ditemukan yang memenuhi syarat (kurang dari 0.5).

3. Loop while: Program menjalankan loop while yang akan terus berulang sampai nilai count sama dengan n. Setiap iterasi dalam loop melakukan hal berikut:
 -Menghasilkan sebuah bilangan acak num antara 0 dan 1 menggunakan fungsi random() dari modul random.
 -Memeriksa apakah num kurang dari 0.5. Jika ya, maka nilai count akan dinaikkan 1, dan num akan ditampilkan dalam format yang menunjukkan urutan data (data ke-count => num).

# Kode Program
```python
from random import random

# Meminta input jumlah bilangan acak yang lebih kecil dari 0.5
n = int(input("Masukkan nilai N: "))
count = 0

# Loop untuk menghasilkan dan menampilkan bilangan acak yang kurang dari 0.5
while count < n:
    num = random()
    if num < 0.5:
        count += 1
        print(f"data ke-{count} => {num}")

print("Selesai")

```
# Output Program
![Flowchart](https://github.com/fitrirmdhni22/lab3.py/blob/main/hasilrun1.png)

# Cara  Kerja Program
1. Meminta Input Pengguna:
-Program dimulai dengan meminta pengguna untuk memasukkan sebuah bilangan bulat n. Nilai n ini mewakili jumlah bilangan acak yang harus dihasilkan yang nilainya kurang dari 0.5.
2. Inisialisasi Variabel Penghitung:
-Variabel count diinisialisasi ke 0. Variabel ini digunakan untuk melacak berapa banyak bilangan acak yang sudah memenuhi syarat (num < 0.5) yang telah dihasilkan.
3. Memulai Loop while:
-Program memasuki loop while, yang akan terus berjalan sampai jumlah bilangan acak yang memenuhi syarat (count) sama dengan nilai n.
-Pada setiap iterasi:
-Program menghasilkan bilangan acak num antara 0 dan 1 menggunakan random().
-Program kemudian memeriksa apakah num kurang dari 0.5:
-Jika num < 0.5: Program menaikkan count sebesar 1, lalu menampilkan num beserta urutannya dalam format "data ke-{count} => {num}".
-Jika num >= 0.5: Program melewatkan bilangan tersebut dan tidak mencetak apapun. Nilai count juga tidak berubah sehingga loop tetap berjalan.
4. Mengakhiri Program:
-Loop while akan berhenti ketika count mencapai nilai n, yang artinya jumlah bilangan acak yang kurang dari 0.5 yang diinginkan telah tercapai.
-Program menampilkan pesan "Selesai" sebagai tanda bahwa proses telah berakhir.

# Program 2
Menghitung keuntungan pengusaha investasi

# Deskripsi Program 
Program ini bertujuan untuk menghitung dan menampilkan laba yang diperoleh setiap bulan selama periode delapan bulan, berdasarkan persentase laba yang berbeda setiap dua bulan. Berikut adalah deskripsi lengkap dari cara kerja program:
1. Inisialisasi Modal Awal:
-Program dimulai dengan mendefinisikan variabel modal_awal sebesar 100 juta (100,000,000) sebagai modal awal usaha.
-Variabel total_laba juga diinisialisasi ke 0 untuk menyimpan jumlah keseluruhan laba yang diperoleh selama delapan bulan.
Menampilkan Header Output:
2.Program menampilkan teks "Laba per bulan:" untuk memberi tahu pengguna bahwa hasil laba bulanan akan segera ditampilkan.
3. Menghitung Laba Bulanan:
-Program menggunakan loop for untuk iterasi dari bulan 1 hingga 8, menghitung laba sesuai ketentuan berikut:
   -Bulan ke-1 dan ke-2: Tidak ada laba (nilai laba diatur ke 0).
   -Bulan ke-3 dan ke-4: Laba sebesar 1% dari modal_awal, dihitung dengan modal_awal * 0.01.
   -Bulan ke-5 dan ke-6: Laba sebesar 5% dari modal_awal, dihitung dengan modal_awal * 0.05.
   -Bulan ke-7: Laba tetap sebesar 5% dari modal_awal.
   -Bulan ke-8: Laba menurun menjadi 3% dari modal_awal, dihitung dengan modal_awal * 0.03.
   -Setelah menghitung laba untuk setiap bulan, program mencetak hasil laba bulan tersebut dalam format "Laba bulan ke-{bulan} sebesar: {laba}".
   -Setiap laba bulanan kemudian ditambahkan ke total_laba untuk menghitung akumulasi laba selama delapan bulan.
4. Menampilkan Total Laba:
Setelah loop selesai, program menampilkan total laba yang diperoleh selama delapan bulan dalam format "Total laba adalah: {total_laba}".

# Kode Program
```python
# Modal awal
modal_awal = 100000000
total_laba = 0

print("Laba per bulan:")

# Menghitung laba per bulan
for bulan in range(1, 9):
    if bulan == 1 or bulan == 2:
        laba = 0  # Bulan pertama dan kedua belum ada laba
    elif bulan == 3 or bulan == 4:
        laba = modal_awal * 0.01  # Bulan ketiga dan keempat laba 1%
    elif bulan == 5 or bulan == 6:
        laba = modal_awal * 0.05  # Bulan kelima dan keenam laba 5%
    elif bulan == 7:
        laba = modal_awal * 0.05  # Bulan ketujuh laba tetap 5%
    elif bulan == 8:
        laba = modal_awal * 0.03  # Bulan kedelapan laba turun menjadi 3%
    
    print(f"Laba bulan ke-{bulan} sebesar: {laba}")
    total_laba += laba  # Menambahkan laba bulanan ke total laba

print(f"Total laba adalah: {total_laba}")
```
# Output Program
![Flowchart](https://github.com/fitrirmdhni22/lab3.py/blob/main/hasilrun2.png?raw=true)

# Cara Kerja Program
Program berjalan dalam loop delapan kali, menghitung laba berdasarkan bulan, mencetak laba bulanan, dan menambahkan laba tersebut ke total_laba. Setelah selesai, program menampilkan total laba yang diperoleh selama delapan bulan.

# Program 3
Membuat ATM sederhana

# Deskripsi Program
Program ini mensimulasikan mesin ATM sederhana dengan dua fitur utama:
Menampilkan Saldo: Setiap kali pengguna melakukan transaksi atau memeriksa saldo, program menampilkan jumlah saldo terkini.
Tarik Uang: Pengguna dapat memasukkan jumlah yang ingin ditarik, dan saldo akan berkurang jika saldo mencukupi.
Keluar: Pengguna dapat keluar dari program.

# Kode Program
```python
def atm():
    saldo = 1000000  # Initial balance
    while True:
        print(f"Saldo saat ini: Rp {saldo}")
        print("1. Tarik Uang")
        print("2. Keluar")
        
        pilihan = input("Pilih menu (1/2): ")
        
        if pilihan == '1':
            try:
                jumlah_penarikan = int(input("Masukkan jumlah penarikan: "))
                if jumlah_penarikan <= saldo:
                    saldo -= jumlah_penarikan
                    print("Penarikan berhasil!")
                else:
                    print("Saldo tidak mencukupi.")
            except ValueError:
                print("Input tidak valid. Masukkan angka.")
        elif pilihan == '2':
            print("Terima kasih telah menggunakan ATM!")
            break
        else:
            print("Pilihan tidak valid. Coba lagi.")
        print()

# Run the ATM function
atm()
```

# Output Program
![Flowchart](https://github.com/fitrirmdhni22/lab3.py/blob/main/hasilrun3.png?raw=true)

# Cara Kerja Program
1. Inisialisasi Saldo:
-Program dimulai dengan mendefinisikan variabel saldo sebesar 1 juta rupiah (1,000,000) sebagai saldo awal pengguna.
2. Memulai Loop Tak Terbatas:
-Program menggunakan while True: untuk menjalankan menu utama secara berulang hingga pengguna memilih untuk keluar.
3. Menampilkan Menu dan Saldo:
-Di awal setiap iterasi, program menampilkan saldo terkini dan dua pilihan menu:
  1. Tarik Uang
  2. Keluar
4. Menerima Pilihan Pengguna:
-Program meminta pengguna untuk memasukkan pilihan (1 atau 2). Jika pengguna memasukkan:
   1. (Tarik Uang): Program meminta pengguna memasukkan jumlah uang yang ingin ditarik. Program kemudian:
      -Memeriksa Saldo: Jika jumlah_penarikan lebih kecil atau sama dengan saldo, penarikan berhasil, saldo berkurang sesuai jumlah penarikan, dan pesan sukses ditampilkan.
      -Saldo Tidak Mencukupi: Jika jumlah penarikan melebihi saldo, program menampilkan pesan bahwa saldo tidak mencukupi.
      -Input Tidak Valid: Jika pengguna memasukkan nilai bukan angka (misalnya huruf), program menampilkan pesan kesalahan "Input tidak valid".
   2. (Keluar): Program menampilkan pesan terima kasih dan menghentikan loop dengan break, mengakhiri program.
-Pilihan Lain: Jika pengguna memasukkan pilihan selain 1 atau 2, program menampilkan pesan "Pilihan tidak valid."
5. Pengulangan Menu:
-Setelah setiap transaksi atau kesalahan input, program kembali ke awal loop, menampilkan saldo dan menu lagi hingga pengguna memilih opsi keluar.
Program ini terus menampilkan saldo dan memungkinkan penarikan uang, kecuali jika pengguna memilih untuk keluar.

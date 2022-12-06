# praktikum6

LATIHAN mengubah fungsi menggunakan lambda![Screenshot (154)](https://user-images.githubusercontent.com/116137169/205904241-0791a6f3-423b-4b38-ba04-a831405906a5.png)

 buatlah seperti gambar berikut ![Screenshot (155)](https://user-images.githubusercontent.com/116137169/205905788-e2db1b25-6737-438d-abaf-46594c7f9e82.png)

 
 

          print ("NAMA : Abdul aziz")
          print("NIM : 312210022")
          print(30*"=")
          import math
          def a(x):
          return x**2
            a = lambda x: x**2, a
          print(a(2))

          def b(x, y):
            return math.sqrt(x*2 + y*2)
            b = lambda x, y: x*2 + y*2, b
          print(b(2, 4))

          def c(*args):
            return sum(args) / len(args)
            c = lambda*args: sum(args) / len(args)
          print(c(10, 50))

          def d(s):
            return "".join(set(s))
            d = lambda s: "".join(set(s))
            
HASIL RUN
![Screenshot (156)](https://user-images.githubusercontent.com/116137169/205905990-5107d6fd-cd7d-4750-a9f8-59d9a0dd57ac.png)

 # PRAKTIKUM 6
![Screenshot (157)](https://user-images.githubusercontent.com/116137169/205907279-0b4214f7-f173-4070-9429-a09e373d7b3d.png)
    
    from os import system
    s_nama = []
    s_nim = []
    s_tugas = []
    s_uts = []
    s_uas = []
    s_akhir = []


    def judul():
        print('==================================')
        print('|     Daftar Nilai Mahasiswa     |')
        print('==================================')


    def menu():
        system('cls')
        print('=====================================')
        print('Input Data Nilai Mahasiswa'.center(40))
        print('=====================================')
        print('|    1. Tambah Data                 |')
        print('|    2. Tampilkan Data Mahasiswa    |')
        print('|    3. Ubah Data Mahasiswa         |')
        print('|    4. Hapus Data Mahasiswa        |')
        print('|    5. Selesai                     |')
        print('=====================================')
        choose = input('Pilih Menu  : ')
        if choose == '1':
            tambah()
        elif choose == '2':
            tampilkan()
        elif choose == '3':
            ubah()
        elif choose == '4':
            hapus()
        elif choose == '5':
            selesai()
        else:
            tidak = input('Menu Tidak Ada')
            system('cls')
          menu()


    def tambah():
        system('cls')
        judul()
        print('Tambah Data'.center(40))
        print('==================================')
        nama = input('Nama     : ')
        s_nama.append(nama)
        nim = input('NIM       : ')
        s_nim.append(nim)

        system('cls')
        judul()
        print('Tambah Data'.center(40))
        print('==================================')
        tugas = float(input('Nilai Tugas    : '))
        s_tugas.append(tugas)

        uts = float(input('Nilai UTS        : '))
        s_uts.append(uts)

        uas = float(input('Nilai UAS        : '))
        s_uas.append(uas)

        total = tugas * 0.30 + uts * 0.35 + uas * 0.35
        s_akhir.append(total)
        print('Data Tersimpan'.center(40))
        kembali = input('Kembali [Enter]')
        menu()


    def tampilkan():
        system('cls')
        judul()

        for i in range(len(s_nim)):
            print('%d. Nama         : %s' % (i + 0, s_nama[i]))
            print('    NIM          : %s' % s_nim[i])
            print('    Nilai Tugas  : %.2f' % s_tugas[i])
            print('    UTS          : %.2f' % s_uts[i])
            print('    UAS          : %.2f' % s_uas[i])
            print('    Nilai Akhir  : %.2f' % s_akhir[i])
            print('-----------------------------')
        kembali = input('Kembali Tekan [Enter]')
          menu()


    def ubah():
        rubah = input('Ubah Biodata Tekan [B]   : ')
        if rubah == 'B' or rubah == 'b':
            i = int(input('Masukkan Nomor Urut  : '))
        if (i > len(s_nim[i])):
            print('Nomor Urut Salah')
        else:
            namabaru = input('Nama      : ')
            s_nama[i] = namabaru
    kembali = input('Kembali Tekan [Enter]')
    menu()


    def hapus():
        system('cls')
        judul()
        print('Hapus Data'.center(40))
        print('=================================')
        i = int(input('Masukkan Nomor Urut  : '))

    if (i > len(s_nim[i])):
        tidak = input('NIM Tidak Ada')
        hapus()

    else:
        s_nim.remove(s_nim[i])
        s_nama.remove(s_nama[i])
        s_tugas.remove(s_tugas[i])
        s_uts.remove(s_uts[i])
        s_uas.remove(s_uas[i])
        s_akhir.remove(s_akhir[i])

    print('Data Berhasil Di Hapus')
    kembali = input('Kembali Tekan [Enter]')
    menu()


    def selesai():
        system('cls')


    menu()

hasil run
 menambahkan dan menampilkan data
![Screenshot (158)](https://user-images.githubusercontent.com/116137169/205912908-68c7a96d-d517-47d6-82de-59c573b47922.png)
![Screenshot (159)](https://user-images.githubusercontent.com/116137169/205912947-3348c5d4-7c64-43f2-8379-1512293641ba.png)

 mengubah data
 ![Screenshot (161)](https://user-images.githubusercontent.com/116137169/205913951-0da9a395-ca9e-4847-8508-8d6850b4b453.png)
 ![Screenshot (162)](https://user-images.githubusercontent.com/116137169/205913992-345eafa8-aaf8-40e3-b70f-557d1cb29cb0.png)
 
 menghapus data
 ![Screenshot (166)](https://user-images.githubusercontent.com/116137169/205914888-ed48bbfe-0f6d-4e7c-9d80-9247014cca30.png)
![Screenshot (167)](https://user-images.githubusercontent.com/116137169/205914934-be201ecf-ad52-43ca-92a8-bd29bbc2d7ea.png)


Definisikan dictionary terlebih dahulu data = {}.
Membuat fungsi
Fungsi tampilkan(), untuk menambahkan data def tampilkan()
Fungsi tambah(), untuk menampilkan data def tambah()
Fungsi hapus(nama), untuk menghapus nama pada data def hapus(nama)
Fungsi ubah(nama), untuk mengubah nama pada data def ubah(nama)
Menggunakan Perulangan while True: dapat diartikan perulangan akan terus mengulang jika inputan benar dan masuk kedalam proses jika tidak maka perulangan berhenti atau lanjut ke proses selanjutnya. Gunakan statement if untuk memproses perintah yang di inginkan sesuai inputan.
Untuk menambahkan data pilih "[1] Tambah" gunakan fungsi if gunakan perintah "1", lalu masukan nama, nim, tugas, uts, uas, nilaiakhir, nilai akhir didapat dari = ((tugas)*30/100 + (uts)*35/100 + (uas)*35/100.
Lalu jika ingin memilih "[2] Lihat" gunakan fungsi 'elif' dan gunakan fungsi 'for x in data.items():' untuk melihat data pada tabel data yang kita inputkan, dengan perintah "2". Jika data tidak terdaftar maka akan tampil "TIDAK ADA DATA" atau = 0.
Lalu untuk menampilan pilihan "[3] Ubah" gunakan fungsi 'elif' kemudian gunakan fungsi 'if nama in data.keys():' kemudian input nama, nim, nilai tugas, nilai uts, nilai uas untuk mengubah data nama kemudian gunakan fungsi 'else' untuk menampilkan data nama yang kita ingin ubah tidak ada.
Untuk menghapus data pilih "[4] Hapus" gunakan fungsi 'elif' kemudian gunakan fungsi 'if nama in data.keys():' kemudian fungsi 'del.data[nama] jika nama yang kita hapus tidak ada dalam tabel maka gunakan fungsi 'else' untuk menampilkan "TIDAK ADA DATA".
Untuk keluar maka gunakan fungsi else dan exit() atau gunakan perintah [5] Keluar.
Selesai.
 # flowchart
  ![image](https://user-images.githubusercontent.com/116137169/205915299-6d105f2f-9196-4ccd-a3ba-1633dcb28368.png)










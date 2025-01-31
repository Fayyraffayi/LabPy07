# LabPy07
# Tugas Pemrograman P10
# Flowchart
![WhatsApp Image 2024-11-27 at 00 37 56](https://github.com/user-attachments/assets/c1612450-2c5d-49e5-8968-056d69a97c2f)
# Codingan
 
     Daftar untuk menyimpan data mahasiswa
     mahasiswa = []

     def tambah(nama, nilai):
         """Menambahkan data mahasiswa ke dalam daftar."""
         mahasiswa.append({"nama": nama, "nilai": nilai})
         print(f"Data {nama} berhasil ditambahkan.")

     def tampilkan():
         """Menampilkan semua data mahasiswa."""
         if not mahasiswa:
            print("Tidak ada data mahasiswa.")
              return
         print("Daftar Nilai Mahasiswa:")
         for index, mhs in enumerate(mahasiswa, start=1):
              print(f"{index}. Nama: {mhs['nama']}, Nilai: {mhs['nilai']}")

    def hapus(nama):
        """Menghapus data mahasiswa berdasarkan nama."""
        global mahasiswa
        _mhs = [mhs for mhs in mahasiswa if mhs["nama"] != nama]
        if len(_mhs) < len(mahasiswa):
        mahasiswa = _mhs
        print(f"Data {nama} berhasil dihapus.")
        else:
        print(f"Data {nama} tidak ditemukan.")

    def ubah(nama, nilai_baru):
         """Mengubah data mahasiswa berdasarkan nama."""
            for mhs in mahasiswa:
            if mhs["nama"] == nama:
                mhs["nilai"] = nilai_baru
                print(f"Data {nama} berhasil diubah menjadi nilai {nilai_baru}.")
                return
           print(f"Data {nama} tidak ditemukan.")

     def menu():
         """Menampilkan menu utama."""
          while True:
             print("\nMenu:")
           print("1. Tambah Data")
           print("2. Tampilkan Data")
           print("3. Hapus Data")
           print("4. Ubah Data")
           print("5. Keluar")
           pilihan = input("Pilih opsi (1-5): ")

        if pilihan == '1':
            nama = input("Masukkan nama mahasiswa: ")
            nilai = input("Masukkan nilai mahasiswa: ")
            tambah(nama, nilai)
        elif pilihan == '2':
            tampilkan()
        elif pilihan == '3':
            nama = input("Masukkan nama mahasiswa yang ingin dihapus: ")
            hapus(nama)
        elif pilihan == '4':
            nama = input("Masukkan nama mahasiswa yang ingin diubah: ")
            nilai_baru = input("Masukkan nilai baru: ")
            ubah(nama, nilai_baru)
        elif pilihan == '5':
            print("Terima kasih!")
            break
        else:
            print("Pilihan tidak valid. Silakan coba lagi.")

     if __name__ == "__main__":
       menu()

# penjelasannya
Penjelasan Berikut adalah penjelasan mengenai kode yang Anda berikan, yang merupakan program sederhana untuk mengelola data mahasiswa. Program ini memungkinkan pengguna untuk menambah, menampilkan, menghapus, dan mengubah data mahasiswa. Mari kita bahas setiap bagian dari kode tersebut:
# 1. Daftar untuk menyimpan Data Mahasiswa
    - mahasiswa = []
 - Di sini, kami mendeklarasikan sebuah daftar kosong bernama mahasiswa yang akan digunakan untuk menyimpan data siswa dalam bentuk kamus.

# 2. Fungsi `tambah`
    - def tambah(nama, nilai):
           """Menambahkan data mahasiswa ke dalam daftar."""
           mahasiswa.append({"nama": nama, "nilai": nilai})
           print(f"Data {nama} berhasil ditambahkan.")
 - Fungsi ini menerima dua parameter: namadan nilai. Fungsi ini akan menambahkan kamus baru ke dalam daftar mahasiswayang berisi nama dan nilai siswa, lalu mencetak pesan bahwa data berhasil ditambahkan.

# 3. Fungsi `tampilkan`
    - def tampilkan():
      """Menampilkan semua data mahasiswa."""
      if not mahasiswa:
          print("Tidak ada data mahasiswa.")
          return
      print("Daftar Nilai Mahasiswa:")
      for index, mhs in enumerate(mahasiswa, start=1):
          print(f"{index}. Nama: {mhs['nama']}, Nilai: {mhs['nilai']}")
 - Fungsi ini menampilkan semua data siswa yang ada dalam list. Jika daftar kosong, akan dicetak pesan bahwa tidak ada data. Jika ada data, akan mencetak nama dan nilai setiap siswa dengan nomor urut.

# 4. Fungsi `hapus`
    - def hapus(nama):
      """Menghapus data mahasiswa berdasarkan nama."""
      global mahasiswa
      _mhs = [mhs for mhs in mahasiswa if mhs["nama"] != nama]
      if len(_mhs) < len(mahasiswa):
          mahasiswa = _mhs
          print(f"Data {nama} berhasil dihapus.")
      else:
           print(f"Data {nama} tidak ditemukan.")
 - Fungsi ini menghapus data siswa berdasarkan nama. Fungsi ini membuat list baru `_mhs` yang berisi semua siswa kecuali yang namanya sesuai dengan parameter `nama`. Jika ada perubahan pada list (artinya data dihapus dan dihapus), maka akan mencetak pesan bahwa data berhasil dihapus.

# 5. Fungsi `ubah`
    - def ubah(nama, nilai_baru):
      """Mengubah data mahasiswa berdasarkan nama."""
      for mhs in mahasiswa:
          if mhs["nama"] == nama:
              mhs["nilai"] = nilai_baru
              print(f"Data {nama} berhasil diubah menjadi nilai {nilai_baru}.")
              return
      print(f"Data {nama} tidak ditemukan.")
 - Fungsi ini digunakan untuk mengubah nilai siswa berdasarkan nama. Jika nama ditemukan, nilai siswa akan diperbarui dengan nilai baru yang diberikan. Jika tidak ditemukan, akan tercetak pesan bahwa data tidak ditemukan.

# 6. Fungsi `menu`
    - def menu():
      """Menampilkan menu utama."""
      while True:
          print("\nMenu:")
          print("1. Tambah Data")
          print("2. Tampilkan Data")
          print("3. Hapus Data")
          print("4. Ubah Data")
          print("5. Keluar")
          pilihan = input("Pilih opsi (1-5): ")
 - Fungsi ini menampilkan menu utama dan meminta pengguna untuk memilih opsi. Menu ini akan terus ditampilkan hingga pengguna memilih untuk keluar.

# 7. Berikan Pilihan Pengguna
Bagian dalam fungsi `menu` menangani pilihan pengguna:
 - **Tambah Data** : Meminta pengguna memasukkan nama dan nilai, lalu memanggil fungsi `tambah`.
 - **Tampilkan Data** : Memanggil fungsi `tampilkan`.
 - **Hapus Data** : Meminta pengguna memasukkan nama siswa yang ingin dihapus, lalu memanggil fungsi `hapus`.
 - **Ubah Data** : Meminta pengguna memasukkan nama dan nilai baru, lalu memanggil fungsi `ubah`.
 - **Keluar** : Mencetak pesan terima kasih dan keluar dari loop.

# 8. Menjalankan Program
    - if __name__ == "__main__":
      menu()
 - agian ini memastikan bahwa fungsi `menu()` hanya akan dijalankan jika skrip ini dijalankan sebagai program utama, bukan jika diimpor sebagai modul.Kesimpulan Program ini adalah aplikasi manajemen data siswa yang sederhana. Pengguna dapat menambahkan, melihat, menghapus, dan mengubah data siswa melalui antarmuka teks. Program ini menggunakan daftar dan kamus untuk menyimpan dan mengelola data.

# Hasil Output
# Tambahkan Data
![Screenshot 2024-11-29 233554](https://github.com/user-attachments/assets/72b410ff-1692-44bd-bd47-64f80d8e349d)

# Tampilkan Data
![Screenshot 2024-11-29 233615](https://github.com/user-attachments/assets/8d93b8c7-0693-48ac-965b-4fd885a98ab6)

# Hapus Data
![Screenshot 2024-11-29 233640](https://github.com/user-attachments/assets/89aaddbd-49fc-4e54-8782-b329af7c0cca)

# Ubah Data
![Screenshot 2024-11-29 233834](https://github.com/user-attachments/assets/6a8f1e40-3081-4418-8880-c5a4df354b2e)

# Keluar
![Screenshot 2024-11-29 233854](https://github.com/user-attachments/assets/6a7e16c4-ac6a-47fe-a39b-cd486d7e2965)


   

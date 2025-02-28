**Program Penghitung Biaya Pengiriman**  

Program ini dirancang untuk menghitung biaya pengiriman barang berdasarkan sejumlah parameter, seperti berat paket, jarak pengiriman, jenis layanan, dan status keanggotaan pelanggan.  

### **Fitur Program**  

- Perhitungan biaya pengiriman mengikuti aturan berikut:  
  - Biaya dasar: **Rp 10.000** untuk semua pengiriman.  
  - Tambahan **Rp 5.000** jika berat paket melebihi **5 kg**.  
  - Tambahan **Rp 8.000** jika jarak pengiriman lebih dari **10 km**.  
  - Tambahan **Rp 20.000** untuk layanan **express**.  
  - Diskon **10%** untuk pelanggan dengan status **member**.  
- Antarmuka berbasis **command line** yang mudah digunakan.  
- Validasi input untuk mencegah kesalahan saat memasukkan data.  
- Format output mengikuti standar pemisah ribuan dalam bahasa Indonesia.  

### **Cara Menggunakan Program**  

1. Jalankan program menggunakan perintah:  
   ```bash
   python nama_file.py
   ```  
2. Masukkan informasi yang diminta, seperti:  
   - Berat paket (dalam **kg**).  
   - Jarak pengiriman (dalam **km**).  
   - Jenis layanan pengiriman (**biasa** atau **express**).  
   - Status keanggotaan (**member** atau **non-member**).  
3. Program akan menghitung dan menampilkan total biaya pengiriman secara rinci.  

### **Struktur Program**  

Program ini terdiri dari dua fungsi utama:  

1. **`hitung_biaya_pengiriman()`**  
   - Fungsi ini menerima empat parameter utama:  
     - **berat_paket**  
     - **jarak_pengiriman**  
     - **jenis_pengiriman**  
     - **status_keanggotaan**  
   - Fungsi ini mengembalikan total biaya pengiriman setelah semua perhitungan diterapkan.  

2. **`main()`**  
   - Fungsi ini bertanggung jawab untuk:  
     - Menampilkan informasi mengenai ketentuan biaya.  
     - Meminta input dari pengguna.  
     - Memvalidasi input agar sesuai format yang diharapkan.  
     - Memanggil fungsi `hitung_biaya_pengiriman()` untuk menghitung total biaya.  
     - Menampilkan hasil akhir dalam format yang rapi.  

### **Contoh Penggunaan Program**  

```  
=== PROGRAM PENGHITUNG BIAYA PENGIRIMAN ===  
Ketentuan biaya pengiriman:  
- Biaya dasar: Rp 10.000  
- Tambahan Rp 5.000 jika berat paket > 5 kg  
- Tambahan Rp 8.000 jika jarak pengiriman > 10 km  
- Tambahan Rp 20.000 jika menggunakan layanan express  
- Diskon 10% untuk member  
==============================================  

Masukkan berat paket (kg): 7  
Masukkan jarak pengiriman (km): 15  

Pilih jenis pengiriman:  
1. Biasa  
2. Express  
Masukkan pilihan (1/2): 2  

Status keanggotaan:  
1. Member  
2. Non-member  
Masukkan pilihan (1/2): 1  

=== RINCIAN BIAYA PENGIRIMAN ===  
Berat paket: 7 kg  
Jarak pengiriman: 15 km  
Jenis pengiriman: express  
Status keanggotaan: member  
------------------------------  
TOTAL BIAYA: Rp 38.700,00  
```  

### **Penanganan Kesalahan (Error Handling)**  

- Program menggunakan mekanisme `try-except` untuk mengantisipasi kesalahan, seperti pengguna memasukkan input yang bukan angka pada bagian berat paket atau jarak pengiriman.  
- Dengan adanya validasi input, program dapat berjalan dengan lancar tanpa mengalami crash akibat kesalahan pengguna.  
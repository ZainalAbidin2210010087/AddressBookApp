# NAMA : ZAINAL ABIDIN

# NPM  : 2210010087

# KELAS : 5B NONREG BANJARMASIN 

# ( #UJIAN TENGAH SEMESTER )

**AddressBookGUI** adalah aplikasi sederhana berbasis Java yang menyediakan antarmuka pengguna grafis (GUI) untuk mengelola daftar kontak. Pengguna dapat menambahkan, mengubah, menghapus, dan melihat informasi kontak yang mencakup nama, alamat, dan nomor telepon.

## Fitur

1. **Tambah Kontak**: Memungkinkan pengguna untuk menambahkan kontak baru ke dalam daftar dengan mengisi nama, alamat, dan nomor telepon.
2. **Ubah Kontak**: Memungkinkan pengguna untuk mengubah informasi kontak yang sudah ada.
3. **Hapus Kontak**: Memungkinkan pengguna untuk menghapus kontak yang dipilih dari daftar.
4. **Lihat Kontak**: Menampilkan informasi kontak ketika kontak dipilih dari daftar.
5. **Bersihkan Kolom**: Otomatis mengosongkan kolom input setelah menambahkan atau memperbarui kontak.

## Struktur Kode

- **`contactMap`**: Sebuah `HashMap` yang menyimpan kontak dengan nama kontak sebagai kunci dan objek `Contact` sebagai nilai.
- **`listModel`**: Sebuah `DefaultListModel` yang digunakan untuk mengisi JList dengan daftar nama kontak untuk mempermudah pemilihan dan pengelolaan.
- **Aksi Tombol**:
  - `addButtonActionPerformed`: Menambah kontak baru.
  - `updateButtonActionPerformed`: Mengubah informasi kontak yang sudah ada.
  - `deleteButtonActionPerformed`: Menghapus kontak yang dipilih.
- **Metode Pembantu `clearFields`**: Mengosongkan semua kolom input untuk nama, alamat, dan nomor telepon.

### Contoh Kode (Bagian Utama)

```java
private void addButtonActionPerformed(java.awt.event.ActionEvent evt) {                                          
    String name = nameField.getText();
    String address = addressField.getText();
    String phone = phoneField.getText();

    if (!name.isEmpty() && !address.isEmpty() && !phone.isEmpty()) {
        Contact contact = new Contact(name, address, phone);
        contactMap.put(name, contact);
        listModel.addElement(name);
        clearFields();
    } else {
        JOptionPane.showMessageDialog(this, "Mohon isi semua field");
    }
}  
```

## Cara Menggunakan

1. **Tambah Kontak**:
   - Isi kolom **Nama**, **Alamat**, dan **Telepon**.
   - Klik tombol **TAMBAH** untuk menambahkan kontak ke dalam daftar.
   
2. **Ubah Kontak**:
   - Pilih kontak dari daftar yang ingin diubah.
   - Isi ulang kolom dengan informasi baru, lalu klik tombol **UBAH**.

3. **Hapus Kontak**:
   - Pilih kontak dari daftar yang ingin dihapus.
   - Klik tombol **HAPUS**.

4. **Lihat Kontak**:
   - Klik pada kontak di daftar untuk menampilkan detailnya di kolom input.

## Teknologi yang Digunakan

- **Java Swing**: Untuk membangun antarmuka pengguna grafis (GUI).
- **Java Collections (HashMap)**: Untuk menyimpan data kontak dengan efisien.
- **Java Event Handling**: Untuk menangani aksi tombol dan pemilihan kontak.

## Keunggulan

- **Antarmuka Sederhana**: Mudah dipahami dan digunakan oleh pengguna.
- **Efisien dalam Manajemen Kontak**: Penyimpanan dan pengambilan data kontak yang cepat dengan menggunakan `HashMap`.
- **Validasi Input**: Memastikan semua kolom terisi sebelum menambah atau memperbarui kontak.
  
## Cara Menjalankan Program

1. Pastikan Anda sudah memiliki **Java Development Kit (JDK)** yang terinstal.
2. Buka program ini di IDE seperti **NetBeans** atau **Eclipse**.
3. Jalankan program dengan menjalankan metode `main` dari kelas `AddressBookGUI`.



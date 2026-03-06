# Konverter Latin ke Arab Pegon

Aplikasi berbasis web interaktif untuk mengonversi teks abjad Latin menjadi tulisan Arab Pegon secara _real-time_. Dilengkapi dengan fitur dikte suara, _rich text editor_, dan sistem kamus kustomisasi (CRUD) yang disesuaikan dengan dialek Nusantara.

---

## 🚀 Fitur Utama & Ketikan

- **Konversi Real-Time:** Teks Latin yang diketik akan langsung berubah menjadi huruf Arab Pegon secara otomatis tanpa perlu menekan tombol "Convert".
- **Integrasi Rich Text Editor (Quill.js):** Pengguna tidak hanya mengetik di kotak teks biasa, melainkan di editor canggih. Format teks seperti **Tebal (Bold)**, _Miring (Italic)_, dan Garis Bawah (Underline) pada teks Latin akan ikut terbawa ke hasil tulisan Pegon-nya.
- **Format Right-to-Left (RTL) Otomatis:** Kotak hasil Pegon dikunci secara ketat agar penulisan dan perataannya selalu dimulai dari kanan ke kiri, sesuai kaidah baku penulisan bahasa Arab.
- **Dukungan Angka & Tanda Baca Arab:** Selain abjad, aplikasi otomatis mengonversi angka (`0-9` menjadi `٠-٩`) dan tanda baca standar (seperti `?` menjadi `؟` dan `,` menjadi `،`).

## 🎤 Fitur Suara (Aksesibilitas)

- **Dikte Suara (Voice-to-Text):** Pengguna bisa mengetik tanpa menyentuh keyboard. Cukup klik tombol "Gunakan Suara" dan mulai berbicara dalam bahasa Indonesia.
- **Preview Suara Live:** Teks hasil suara dan terjemahan Pegon-nya akan muncul kata-per-kata secara _live_ di layar saat pengguna masih berbicara.

## ⚙️ Fitur Pengaturan & Kamus Kustom (CRUD)

- **Kamus Abjad Lengkap:** Sudah dibekali dengan aturan bawaan untuk huruf tunggal maupun ganda khas Pegon Nusantara (seperti `ng` → `ڠ`, `ny` → `ڽ`, `c` → `چ`, `p` → `ف`).
- **Tambah Kata Serapan (Add):** Pengguna bisa memasukkan aturan khusus untuk kata tertentu. Misalnya mengatur agar kata `alloh` otomatis menjadi `الله` atau `muhammad` menjadi `محمد`.
- **Edit Huruf Bawaan (Edit):** Jika pengguna tidak cocok dengan bentuk huruf Pegon bawaan skrip, mereka bisa mengubahnya sendiri (misalnya mengubah `e` dari `ي` menjadi bentuk pepet lain).
- **Hapus Aturan (Delete):** Aturan yang tidak terpakai bisa dihapus dari tabel dengan satu klik.
- **Penyimpanan Permanen (LocalStorage):** Semua perubahan, penambahan, dan editan kamus akan tersimpan di memori browser. Jika web ditutup dan dibuka lagi besok, kamus _custom_ pengguna tidak akan hilang.
- **Tombol Reset Aman:** Terdapat tombol **Reset ke Bawaan** untuk mengembalikan seluruh kamus ke setelan awal jika pengguna melakukan kesalahan saat mengedit.

## 🧠 Logika & Algoritma Pintar

- **Prioritas Kata Terpanjang:** Algoritma membaca kata dari yang paling panjang terlebih dahulu. Jadi jika ada aturan untuk kata `alloh` dan huruf `a`, sistem tidak akan memecah kata "alloh" menjadi ejaan huruf tunggal.
- **Penyesuaian Vokal Awal Kata:** Sistem cukup pintar untuk mendeteksi apakah huruf vokal (a, i, u, e, o) berada di awal kata atau kalimat. Jika di awal, sistem otomatis menambahkan huruf Alif pendamping (misal: "ikan" menjadi "إيكان").

## 🎨 Tampilan & UX (Pengalaman Pengguna)

- **Pilihan Font Arab Eksklusif:** Pengguna bisa memilih 3 jenis kaligrafi Arab (_Amiri_, _Scheherazade New_, atau _Noto Naskh Arabic_) langsung dari _dropdown_ untuk memperindah hasil tulisan Pegon.
- **Salin Cerdas (Rich Copy):** Tombol "Salin Pegon" tidak hanya menyalin teks mentah, tetapi juga menyalin format (seperti _bold/italic_). Saat di-_paste_ ke Microsoft Word atau WhatsApp, formatnya akan tetap rapi.
- **Indikator Visual:** Tombol mikrofon akan berkedip (animasi) saat merekam suara, dan tombol salin akan berubah warna menjadi hijau dengan centang ("✔ Tersalin!") sebagai umpan balik visual bahwa aksi berhasil.

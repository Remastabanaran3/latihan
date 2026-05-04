# Rencana Implementasi: Website Profil Pribadi

## Ikhtisar

Implementasi website profil pribadi sebagai halaman statis satu file (`index.html`) menggunakan HTML, CSS, dan JavaScript murni. Pendekatan incremental dimulai dari struktur HTML semantik, lalu styling, kemudian perilaku interaktif, dan diakhiri dengan pengujian komprehensif.

## Tugas

- [ ] 1. Buat struktur HTML semantik dan kerangka halaman
  - Buat file `index.html` dengan elemen semantik: `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`
  - Tambahkan section dengan ID yang sesuai: `tentang`, `informasi`, `keahlian`, `pengalaman`, `kontak`
  - Isi konten hardcoded untuk semua section sesuai model data di desain (ProfilPemilik, Keahlian, EntriPengalaman, TautanSosial)
  - Pastikan elemen `<img>` foto profil memiliki atribut `alt` deskriptif dan handler `onerror` untuk fallback avatar emoji
  - Tambahkan atribut `lang="id"` pada elemen `<html>`
  - _Persyaratan: 1.1, 1.2, 1.3, 1.4, 2.1, 3.1, 4.1, 5.1, 6.1, 9.2, 9.3_

- [ ] 2. Implementasi header identitas dan bagian konten
  - [ ] 2.1 Implementasi header identitas (cover, avatar, nama, jabatan, lokasi)
    - Buat elemen cover/banner dekoratif dengan gradient CSS
    - Tambahkan foto profil / avatar emoji dengan atribut `alt` deskriptif
    - Tampilkan nama lengkap dalam `<h1>`, jabatan dalam `<p>`, lokasi dalam `<p>`
    - Pastikan seluruh konten header terlihat tanpa scroll (above the fold)
    - _Persyaratan: 1.1, 1.2, 1.3, 1.4, 1.5_

  - [ ] 2.2 Implementasi bagian "Tentang Saya"
    - Buat `<section id="tentang">` dengan `<h2>` dan paragraf bio
    - Pastikan CSS menggunakan `overflow: visible` (tidak ada `text-overflow: ellipsis`)
    - _Persyaratan: 2.1, 2.2, 2.3_

  - [ ] 2.3 Implementasi bagian "Informasi Pribadi"
    - Buat grid item informasi dengan label dan nilai untuk field wajib (nama, email, lokasi)
    - Tambahkan field opsional (telepon, tanggal lahir, status) dengan penanganan `display: none` jika tidak tersedia
    - Tata letak grid 2 kolom di desktop
    - _Persyaratan: 3.1, 3.2, 3.3_

  - [ ] 2.4 Implementasi bagian "Keahlian"
    - Buat container dengan `display: flex; flex-wrap: wrap` untuk tag keahlian
    - Render setiap keahlian sebagai `<span class="skill-tag">`
    - _Persyaratan: 4.1, 4.2, 4.3_

  - [ ] 2.5 Implementasi bagian "Pengalaman"
    - Buat daftar entri pengalaman dalam tampilan timeline vertikal
    - Setiap entri memuat: nama posisi, nama perusahaan/lembaga, periode waktu
    - Urutkan entri dari terbaru ke terlama dalam HTML
    - _Persyaratan: 5.1, 5.2, 5.3_

  - [ ] 2.6 Implementasi bagian "Kontak & Sosial"
    - Buat tombol email dengan `href="mailto:..."` 
    - Buat tombol tautan sosial eksternal dengan `target="_blank"` dan `rel="noopener noreferrer"`
    - Sembunyikan tombol platform yang tidak tersedia
    - _Persyaratan: 6.1, 6.2, 6.3, 6.4, 6.5_

- [ ] 3. Implementasi CSS — styling dan desain responsif
  - [ ] 3.1 Buat stylesheet embedded untuk layout dan visual
    - Tambahkan `<style>` embedded di `<head>`
    - Styling untuk semua komponen: header, nav, card section, skill tag, timeline pengalaman, tombol sosial, footer
    - Gunakan system font stack (tanpa CDN eksternal)
    - Pastikan kontras warna memenuhi WCAG AA (rasio minimal 4.5:1)
    - _Persyaratan: 9.1, 9.4_

  - [ ] 3.2 Implementasi desain responsif (mobile-first)
    - Tambahkan media query untuk lebar < 768px: tata letak satu kolom, grid informasi 1 kolom
    - Pastikan tidak ada overflow horizontal pada viewport 320px–1920px
    - Tambahkan `word-break: break-word` pada elemen teks panjang
    - Tambahkan `min-width: 320px` pada container utama
    - _Persyaratan: 8.1, 8.2, 8.4_

- [ ] 4. Implementasi JavaScript — navigasi interaktif
  - [ ] 4.1 Implementasi smooth scroll dan navigasi sticky
    - Buat `<nav>` dengan `position: sticky; top: 0` dan daftar tautan ke setiap section
    - Implementasi fungsi `initSmoothScroll(navLinks)` untuk scroll mulus saat tautan nav diklik
    - _Persyaratan: 7.1, 7.2_

  - [ ] 4.2 Implementasi highlight navigasi aktif dengan IntersectionObserver
    - Implementasi fungsi `initActiveNavObserver(sections, navLinks)` menggunakan `IntersectionObserver`
    - Sorot item nav yang sesuai dengan section yang sedang terlihat di viewport
    - _Persyaratan: 7.3_

  - [ ] 4.3 Implementasi menu hamburger untuk mobile
    - Buat tombol hamburger (`<button>`) yang terlihat di layar < 768px
    - Implementasi fungsi `toggleMobileMenu(menuButton, navList)` untuk toggle tampilan menu
    - Sembunyikan daftar navigasi secara default di mobile, tampilkan saat tombol diklik
    - _Persyaratan: 8.3_

- [ ] 5. Checkpoint — Verifikasi tampilan dan fungsionalitas dasar
  - Pastikan semua section tampil dengan benar di browser
  - Pastikan navigasi sticky berfungsi, smooth scroll bekerja, dan hamburger menu toggle di mobile
  - Pastikan tidak ada overflow horizontal pada berbagai ukuran viewport
  - Tanyakan kepada pengguna jika ada pertanyaan sebelum melanjutkan ke pengujian.

- [ ] 6. Siapkan lingkungan pengujian
  - Inisialisasi proyek Node.js dengan `package.json` (jika belum ada)
  - Instal dependensi pengujian: `jest`, `jest-environment-jsdom`, `@jest/globals`, `fast-check`, `axe-core`
  - Buat file konfigurasi Jest (`jest.config.js`) dengan environment jsdom
  - Buat file helper pengujian untuk me-load dan me-parse `index.html` ke dalam jsdom
  - _Persyaratan: 9.1, 9.2, 9.3, 9.4_

- [ ] 7. Tulis unit test untuk struktur HTML dan konten
  - [ ] 7.1 Tulis unit test untuk header dan elemen semantik
    - Test: header menampilkan nama, foto/avatar, jabatan, lokasi
    - Test: elemen semantik ada (`<header>`, `<main>`, `<section>`, `<footer>`, `<nav>`)
    - Test: semua elemen `<img>` memiliki atribut `alt` yang tidak kosong
    - _Persyaratan: 1.1, 1.2, 1.3, 1.4, 9.2, 9.3_

  - [ ]* 7.2 Tulis property test untuk Properti 11 — Atribut alt pada semua gambar
    - **Properti 11: Atribut Alt pada Semua Gambar**
    - **Memvalidasi: Persyaratan 9.3**
    - Generate halaman dengan berbagai jumlah gambar, verifikasi semua `<img>` memiliki atribut `alt` yang tidak kosong

  - [ ] 7.3 Tulis unit test untuk bagian konten
    - Test: section "Tentang Saya" ada dan berisi teks bio
    - Test: section informasi pribadi memiliki field wajib (nama, email, lokasi)
    - Test: section keahlian ada dan berisi tag keahlian
    - Test: section pengalaman ada dan berisi minimal satu entri
    - Test: section kontak ada dan berisi minimal satu metode kontak
    - Test: tautan sosial dirender sebagai elemen `<a>`
    - _Persyaratan: 2.1, 3.1, 4.1, 5.1, 6.1, 6.2_

- [ ] 8. Tulis unit test dan property test untuk fungsi validasi dan rendering
  - [ ] 8.1 Implementasi dan uji fungsi `validateBio(text)`
    - Buat fungsi `validateBio(text)` yang mengembalikan `true` untuk string 50–1000 karakter
    - Tulis unit test: bio tepat 50 karakter (valid), bio tepat 1000 karakter (valid), bio 49 karakter (invalid), bio 1001 karakter (invalid), string kosong (invalid)
    - _Persyaratan: 2.2_

  - [ ]* 8.2 Tulis property test untuk Properti 1 — Validasi panjang bio
    - **Properti 1: Validasi Panjang Bio**
    - **Memvalidasi: Persyaratan 2.2**
    - Generate string dengan panjang acak, verifikasi `validateBio(text)` menerima panjang 50–1000 dan menolak di luar rentang

  - [ ]* 8.3 Tulis property test untuk Properti 2 — Teks bio tidak terpotong
    - **Properti 2: Teks Bio Ditampilkan Lengkap**
    - **Memvalidasi: Persyaratan 2.3**
    - Generate bio valid (50–1000 karakter), render ke DOM, verifikasi `textContent.length === input.length`

  - [ ]* 8.4 Tulis property test untuk Properti 3 — Konsistensi rendering item informasi
    - **Properti 3: Konsistensi Rendering Item Informasi**
    - **Memvalidasi: Persyaratan 3.2, 3.3**
    - Generate item informasi acak, render, verifikasi setiap item memiliki elemen label dan nilai yang tidak kosong dengan struktur HTML identik

  - [ ]* 8.5 Tulis property test untuk Properti 4 — Jumlah tag keahlian
    - **Properti 4: Setiap Keahlian Dirender Sebagai Elemen Terpisah**
    - **Memvalidasi: Persyaratan 4.2**
    - Generate array keahlian acak, render, verifikasi `querySelectorAll('.skill-tag').length === input.length`

- [ ] 9. Tulis property test untuk pengalaman dan tautan sosial
  - [ ]* 9.1 Tulis property test untuk Properti 5 — Kelengkapan entri pengalaman
    - **Properti 5: Kelengkapan Data Entri Pengalaman**
    - **Memvalidasi: Persyaratan 5.2**
    - Generate entri pengalaman acak, render, verifikasi setiap entri mengandung teks posisi, institusi, dan periode

  - [ ]* 9.2 Tulis property test untuk Properti 6 — Urutan pengalaman terbaru ke terlama
    - **Properti 6: Urutan Pengalaman Terbaru ke Terlama**
    - **Memvalidasi: Persyaratan 5.3**
    - Generate entri dengan nilai `urutan` acak, render, verifikasi urutan DOM mencerminkan urutan dari nilai terkecil ke terbesar

  - [ ]* 9.3 Tulis property test untuk Properti 7 — Format tautan email
    - **Properti 7: Format Tautan Email**
    - **Memvalidasi: Persyaratan 6.3**
    - Generate alamat email acak yang valid, render, verifikasi atribut `href === "mailto:" + email`

  - [ ]* 9.4 Tulis property test untuk Properti 8 — Perilaku tautan sosial
    - **Properti 8: Perilaku Tautan Sosial**
    - **Memvalidasi: Persyaratan 6.4, 6.5**
    - Generate kombinasi tautan sosial tersedia/tidak tersedia, render, verifikasi hanya tautan `tersedia = true` yang dirender dan memiliki `target="_blank"` serta `rel="noopener noreferrer"`

- [ ] 10. Tulis unit test untuk navigasi dan property test untuk responsivitas
  - [ ] 10.1 Tulis unit test untuk navigasi
    - Test: nav ada dan berisi tautan ke semua section
    - Test: setiap tautan nav memiliki `href` yang sesuai dengan ID section
    - Test: fungsi highlight nav menambahkan class aktif yang benar
    - Test: tombol hamburger terlihat di mobile, menu tersembunyi secara default
    - _Persyaratan: 7.1, 7.2, 7.3, 8.3_

  - [ ]* 10.2 Tulis property test untuk Properti 9 — Tidak ada overflow horizontal
    - **Properti 9: Tidak Ada Overflow Horizontal di Semua Viewport**
    - **Memvalidasi: Persyaratan 8.1, 8.4**
    - Generate lebar viewport acak 320–1920px, render, verifikasi tidak ada elemen yang memiliki lebar melebihi lebar viewport

  - [ ]* 10.3 Tulis property test untuk Properti 10 — Tata letak satu kolom di mobile
    - **Properti 10: Tata Letak Satu Kolom di Mobile**
    - **Memvalidasi: Persyaratan 8.2**
    - Generate lebar viewport acak 320–767px, render, verifikasi grid informasi pribadi menggunakan tata letak satu kolom

- [ ] 11. Checkpoint akhir — Pastikan semua tes lulus
  - Jalankan seluruh suite pengujian (`jest --run` atau `npx jest`)
  - Pastikan semua unit test dan property test lulus
  - Tanyakan kepada pengguna jika ada pertanyaan sebelum menyelesaikan implementasi.

## Catatan

- Tugas yang ditandai dengan `*` bersifat opsional dan dapat dilewati untuk MVP yang lebih cepat
- Setiap tugas merujuk pada persyaratan spesifik untuk keterlacakan
- Checkpoint memastikan validasi incremental di setiap tahap
- Property test memvalidasi properti kebenaran universal (Properti 1–11 dari dokumen desain)
- Unit test memvalidasi contoh spesifik dan kondisi edge case
- Semua CSS dan JavaScript disematkan langsung di `index.html` (tidak ada file terpisah)
- Library pengujian: Jest + jsdom untuk unit test, fast-check untuk property-based test, axe-core untuk aksesibilitas

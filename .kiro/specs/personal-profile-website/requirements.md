# Dokumen Persyaratan

## Pendahuluan

Website profil pribadi adalah halaman web statis yang berfungsi sebagai kartu identitas digital seseorang di internet. Website ini memungkinkan pemilik untuk memperkenalkan diri, menampilkan keahlian dan pengalaman, serta memudahkan orang lain untuk mengenal dan menghubungi mereka. Target pengguna website ini adalah siapa saja yang mengunjungi tautan profil — mulai dari rekruter, rekan kerja, klien potensial, hingga kenalan baru.

## Glosarium

- **Website**: Halaman web profil pribadi yang dibangun dengan HTML, CSS, dan JavaScript
- **Pengunjung**: Orang yang membuka dan melihat halaman profil
- **Pemilik**: Orang yang memiliki dan mempersonalisasi profil tersebut
- **Bagian (Section)**: Blok konten tematik dalam halaman (misalnya: Tentang Saya, Keahlian)
- **Navigasi**: Menu atau tautan yang membantu pengunjung berpindah antar bagian
- **Tautan Sosial**: Tombol atau ikon yang mengarah ke platform eksternal (email, LinkedIn, GitHub, dll.)
- **Responsif**: Tampilan yang menyesuaikan diri dengan berbagai ukuran layar perangkat

---

## Persyaratan

### Persyaratan 1: Tampilan Identitas Utama

**User Story:** Sebagai pengunjung, saya ingin melihat identitas utama pemilik profil secara langsung saat halaman dibuka, agar saya dapat segera mengetahui siapa orang ini.

#### Kriteria Penerimaan

1. THE Website SHALL menampilkan nama lengkap pemilik di bagian paling atas halaman.
2. THE Website SHALL menampilkan foto profil atau avatar pemilik di bagian header.
3. THE Website SHALL menampilkan jabatan atau profesi pemilik di bawah nama.
4. THE Website SHALL menampilkan lokasi atau kota domisili pemilik.
5. WHEN halaman pertama kali dimuat, THE Website SHALL menampilkan bagian identitas utama tanpa memerlukan scroll.

---

### Persyaratan 2: Bagian Tentang Saya

**User Story:** Sebagai pengunjung, saya ingin membaca deskripsi singkat tentang pemilik profil, agar saya dapat memahami latar belakang dan kepribadiannya.

#### Kriteria Penerimaan

1. THE Website SHALL menampilkan bagian "Tentang Saya" yang berisi teks deskripsi diri pemilik.
2. THE Website SHALL menampilkan teks bio dengan panjang minimal 50 karakter dan maksimal 1000 karakter.
3. WHEN teks bio melebihi batas tampilan, THE Website SHALL menampilkan seluruh teks tanpa terpotong.

---

### Persyaratan 3: Bagian Informasi Pribadi

**User Story:** Sebagai pengunjung, saya ingin melihat informasi dasar pemilik profil secara terstruktur, agar saya dapat dengan cepat menemukan detail yang saya butuhkan.

#### Kriteria Penerimaan

1. THE Website SHALL menampilkan bagian informasi pribadi yang memuat minimal: nama lengkap, email, dan lokasi.
2. THE Website SHALL menampilkan setiap item informasi dengan label yang jelas dan nilai yang terbaca.
3. WHERE informasi opsional tersedia (seperti nomor telepon atau tanggal lahir), THE Website SHALL menampilkan informasi tersebut dalam tata letak yang konsisten.

---

### Persyaratan 4: Bagian Keahlian

**User Story:** Sebagai pengunjung, saya ingin melihat daftar keahlian pemilik profil, agar saya dapat menilai kompetensi dan bidang keahliannya.

#### Kriteria Penerimaan

1. THE Website SHALL menampilkan bagian keahlian yang memuat daftar skill atau kompetensi pemilik.
2. THE Website SHALL menampilkan setiap keahlian sebagai elemen visual yang terpisah dan mudah dibaca (misalnya tag atau badge).
3. WHEN jumlah keahlian melebihi lebar satu baris, THE Website SHALL menampilkan keahlian secara melingkar ke baris berikutnya tanpa terpotong.

---

### Persyaratan 5: Bagian Pengalaman atau Riwayat

**User Story:** Sebagai pengunjung, saya ingin melihat riwayat pengalaman kerja atau pendidikan pemilik profil, agar saya dapat memahami perjalanan karier atau akademiknya.

#### Kriteria Penerimaan

1. THE Website SHALL menampilkan bagian pengalaman yang memuat minimal satu entri riwayat (kerja atau pendidikan).
2. THE Website SHALL menampilkan setiap entri pengalaman dengan informasi: nama posisi/institusi, nama perusahaan/lembaga, dan periode waktu.
3. THE Website SHALL menampilkan entri pengalaman secara berurutan dari yang paling baru ke yang paling lama.

---

### Persyaratan 6: Bagian Kontak dan Tautan Sosial

**User Story:** Sebagai pengunjung, saya ingin menemukan cara untuk menghubungi atau mengikuti pemilik profil di platform lain, agar saya dapat terhubung dengan mereka.

#### Kriteria Penerimaan

1. THE Website SHALL menampilkan bagian kontak yang memuat minimal satu metode kontak (email atau nomor telepon).
2. THE Website SHALL menampilkan tautan sosial sebagai tombol atau ikon yang dapat diklik.
3. WHEN pengunjung mengklik tautan email, THE Website SHALL membuka aplikasi email default dengan alamat tujuan yang sudah terisi.
4. WHEN pengunjung mengklik tautan sosial eksternal (LinkedIn, GitHub, dll.), THE Website SHALL membuka tautan tersebut di tab baru.
5. IF tautan sosial tidak tersedia untuk platform tertentu, THEN THE Website SHALL menyembunyikan tombol platform tersebut.

---

### Persyaratan 7: Navigasi Halaman

**User Story:** Sebagai pengunjung, saya ingin dapat berpindah antar bagian halaman dengan mudah, agar saya tidak perlu scroll panjang untuk menemukan informasi tertentu.

#### Kriteria Penerimaan

1. THE Website SHALL menampilkan menu navigasi yang memuat tautan ke setiap bagian utama halaman.
2. WHEN pengunjung mengklik tautan navigasi, THE Website SHALL menggulir halaman secara mulus ke bagian yang dituju.
3. WHILE pengunjung menggulir halaman, THE Website SHALL menyorot item navigasi yang sesuai dengan bagian yang sedang terlihat.

---

### Persyaratan 8: Desain Responsif

**User Story:** Sebagai pengunjung yang mengakses dari perangkat mobile, saya ingin tampilan profil tetap nyaman dibaca, agar saya dapat menikmati konten tanpa hambatan.

#### Kriteria Penerimaan

1. THE Website SHALL menampilkan tata letak yang dapat dibaca pada lebar layar minimal 320px hingga 1920px.
2. WHEN lebar layar kurang dari 768px, THE Website SHALL menyesuaikan tata letak menjadi satu kolom vertikal.
3. WHEN lebar layar kurang dari 768px, THE Website SHALL menampilkan menu navigasi dalam format yang sesuai untuk layar kecil (misalnya menu hamburger atau navigasi vertikal).
4. THE Website SHALL memastikan semua teks dapat dibaca tanpa perlu zoom horizontal pada perangkat mobile.

---

### Persyaratan 9: Performa dan Aksesibilitas Dasar

**User Story:** Sebagai pengunjung, saya ingin halaman profil dapat dimuat dengan cepat dan mudah diakses, agar pengalaman membaca profil menjadi menyenangkan.

#### Kriteria Penerimaan

1. THE Website SHALL memuat seluruh konten halaman dalam waktu kurang dari 3 detik pada koneksi internet standar (minimal 10 Mbps).
2. THE Website SHALL menggunakan elemen HTML semantik yang tepat (seperti `<header>`, `<main>`, `<section>`, `<footer>`) untuk mendukung aksesibilitas.
3. THE Website SHALL menyertakan atribut `alt` yang deskriptif pada setiap elemen gambar.
4. THE Website SHALL memiliki kontras warna antara teks dan latar belakang yang memenuhi standar WCAG AA (rasio kontras minimal 4.5:1 untuk teks normal).

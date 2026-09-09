# LAB-WEB-07-2026
## Praktikum Web 07 2026 - Universitas Hasanuddin (First time as an Aslab btw)

Selamat datang di repositori  **Praktikum Pemrograman Web 2026 — Universitas Hasanuddin**!  

## Informasi Anggota Web 07

**Asisten Lab:** Reynaldy Al (H071231057)

**Daftar Praktikan:**
| NIM | Nama Lengkap |
| :--- | :--- |
| H071251026 | Muhammad Mahathir |
| H071251028 | Aliyah Fitraturramadhani |
| H071251052 | Ilmi Ahmad Alfaridzi |
| H071251080 | Dylan Dwi Putra Patarai |
| H071251086 | Riskia Nur Azizah Ismail |
| H071251093 | Imam Arief Rachmat |

---

## Konsep Dasar: Apa itu Branch `main` vs Branch `<NIM>`?

Sebelum mulai mengetik perintah Git, penting untuk memahami konsep **Branch** (percabangan):

* **Branch `main` (Jalur Utama):**  
  `main` adalah cabang utama yang berisi sumber kode resmi dan stabil dari asisten lab. Jalur ini ibarat "pohon induk" yang tidak boleh diubah sembarangan oleh praktikan secara langsung agar kode utama tetap bersih dan tidak bentrok dengan praktikan lain.

* **Branch `<NIM>` (Ruang Kerja Pribadi Kalian):**  
  Branch NIM (misalnya `H071211074`) adalah salinan cabang mandiri tempat kalian bereksperimen, mengerjakan tugas, dan menyimpan kode mingguan. Dengan membuat branch terpisah menggunakan NIM, pekerjaan kalian tidak akan mengganggu praktikan lain dan memudahkan asisten dalam memeriksa serta menilai tugas kalian.

---

## Standar Industri: Semantic Commit Messages

Biasakan menulis pesan *commit* yang jelas dan bermakna. Hindari pesan singkat yang tidak informatif seperti *"update"*, *"tugas selesai"*, atau *"bismillah"*.

Gunakan format standar berikut:
```text
<tipe>: <penjelasan singkat perubahan>
```

| Tipe | Kapan Digunakan? | Contoh Pesan Commit |
| :--- | :--- | :--- |
| **`feat:`** | Menambah fitur baru atau mengumpulkan tugas pertemuan baru | `feat: menyelesaikan tugas praktikum 1 form registrasi` |
| **`fix:`** | Memperbaiki error, bug logika, atau kesalahan ketik (typo) | `fix: memperbaiki error validasi pada input email` |
| **`style:`** | Mengubah tampilan/CSS tanpa mengubah logika kode program | `style: merapikan tata letak grid dan padding tabel` |
| **`docs:`** | Menambah atau memperbarui dokumentasi/catatan (file README, komentar kode) | `docs: menambahkan catatan cara menjalankan web lokal` |
| **`refactor:`** | Merapikan atau merestrukturisasi kode/folder tanpa mengubah hasil fungsi | `refactor: memindahkan file css ke folder terpisah` |

---

## Aturan & Langkah Pengumpulan Tugas

> ⚠️ **Catatan Penting Penggantian Tanda Kurung `< >`:**  
> Bagian yang diapit tanda `<...>` adalah instruksi variabel yang wajib diganti dengan data asli kalian tanpa menyertakan tanda kurungnya.  
> *Contoh:* `mkdir <NIM>` diketik menjadi `mkdir H071211074`.

### Langkah 1: Fork Repositori ke Akun Pribadi
1. Buka halaman repositori utama praktikum ini di browser GitHub.
2. Klik tombol **Fork** di pojok kanan atas layar.
3. Centang opsi penyimpanan default, lalu klik **Create fork**. Sekarang repositori ini sudah tersalin ke profil GitHub pribadi kalian.

### Langkah 2: Clone ke Komputer Lokal
Buka terminal (Git Bash / PowerShell / Command Prompt), lalu unduh repositori hasil fork kalian ke laptop:

```bash
git clone <URL-repositori-hasil-fork-kalian>
```
*Contoh:*
```bash
git clone https://github.com/username-kalian/LAB-WEB-07-2026.git
```
Setelah proses selesai, masuk ke dalam folder repositori:
```bash
cd LAB-WEB-07-2026
```

### Langkah 3: Buat Branch Baru Menggunakan NIM
Pastikan kalian tidak bekerja di branch `main`. Buat cabang kerja baru sekaligus berpindah ke sana dengan mengetik:

```bash
git checkout -b <NIM>
```
*Contoh:*
```bash
git checkout -b H071211074
```

### Langkah 4: Susun Struktur Direktori Tugas
Agar repositori tetap rapi dan terorganisir, ikuti aturan struktur folder berikut:
1. Buat folder utama menggunakan **NIM** kalian (jika belum ada).
2. Di dalam folder NIM tersebut, buat subfolder untuk pertemuan tugas dengan format: `tugas-praktikum-<nomor_pertemuan>` (semua huruf kecil, tanpa spasi).
3. Masukkan seluruh file tugas ke dalam subfolder pertemuan tersebut.

**Contoh Susunan Folder:**
```text
LAB-WEB-07-2026/
├── H071211074/
│   ├── tugas-praktikum-1/
│   │   ├── index.html
│   │   ├── style.css
│   │   └── script.js
│   └── tugas-praktikum-2/
│       ├── index.html
│       └── style.css
└── README.md
```

### Langkah 5: Simpan & Unggah Kode (Commit & Push)
Setelah tugas selesai dikerjakan, diuji, dan diasistensikan:

1. Daftarkan semua perubahan file ke staging area:
   ```bash
   git add .
   ```
2. Simpan perubahan dengan pesan semantic commit:
   ```bash
   git commit -m "feat: mengumpulkan tugas praktikum 1"
   ```
3. Unggah branch tugas kalian ke GitHub:
   ```bash
   git push -u origin <NIM>
   ```
   *Contoh:*
   ```bash
   git push -u origin H071211074
   ```

### Langkah 6: Mengajukan Pull Request (PR)
1. Buka repositori hasil fork kalian di browser GitHub.
2. Klik tombol hijau **Compare & pull request** yang muncul di atas daftar file.
3. Pastikan konfigurasi percabangan sudah benar:
   * **Base repository:** `repositori-utama-lab/LAB-WEB-07-2026` | **base:** `main`
   * **Head repository:** `<akun-kalian>/LAB-WEB-07-2026` | **compare:** `<NIM>`
4. Beri judul Pull Request dengan format:
   ```text
   [TUGAS-<NO>] - <NIM> - <NAMA LENGKAP>
   ```
   *Contoh Judul:* `[TUGAS-1] - H071211074 - Reyhan`
5. Klik **Create pull request**. Asisten lab akan memeriksa tugas kalian melalui PR tersebut.

---

### Q & A
Jika mengalami kendala teknis seperti Git conflict, error terminal, atau pertanyaan mengenai instruksi praktikum tanya ka nahh!!

Semangat Mahasiswaaa

# Template Tesis FMIPA UGM

**v1.0** | Template LaTeX untuk Proposal Tesis dan Tesis di Fakultas Matematika dan Ilmu Pengetahuan Alam, Universitas Gadjah Mada.

*LaTeX template for Master's Thesis Proposal and Thesis at the Faculty of Mathematics and Natural Sciences, Universitas Gadjah Mada.*

---

## Fitur / Features

- Mendukung **Proposal Tesis** (4 bab) dan **Tesis** (6 bab)
- Bilingual: Bahasa Indonesia dan English
- Sesuai dengan ketentuan penulisan terbaru FMIPA UGM
- Theorem environments (Definisi, Teorema, Lema, Akibat, Proposisi)
- Sistem sitasi Harvard (author-year) dengan biblatex
- Format bibliografi sesuai panduan FMIPA UGM
- Penomoran otomatis (gambar, tabel, persamaan per bab)
- Template lampiran lengkap (Surat Pernyataan AI, Bukti Submit Paper, dll.)

---

## Cara Penggunaan / How to Use

### 1. Clone Repository

```bash
git clone https://github.com/khalilullahalfaath/template-tesis-fmipa.git
cd template-tesis-fmipa
```

### 2. Pilih Mode / Select Mode

Edit baris `\documentclass` di `main.tex`:

```latex
% Proposal Tesis (Bahasa Indonesia)
\documentclass[proposaltesis,bahasa]{ugmfmipa}

% Proposal Tesis (English)
\documentclass[proposaltesis,english]{ugmfmipa}

% Tesis (Bahasa Indonesia)
\documentclass[tesis,bahasa]{ugmfmipa}

% Tesis (English)
\documentclass[tesis,english]{ugmfmipa}
```

### 3. Isi Informasi / Fill Information

Edit bagian `Information Input` di `main.tex`:

```latex
\author{Nama Lengkap}{NIM}
\titleind{Judul Tesis dalam Bahasa Indonesia}
\titleeng{Thesis Title in English}
\program{Nama Prodi}{Nama Koordinator}{NIP}
\departmenthead{Nama Ketua Departemen}{NIP}
\yearsubmit{2026}
\examdate{1 Januari 2026}
\addsupervisor{Nama Pembimbing 1, S.Kom., M.Cs., Ph.D.}{NIP}
\addsupervisor{Nama Pembimbing 2, S.Kom., M.Cs., Ph.D.}{NIP}
```

### 4. Compile

```bash
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

Atau menggunakan `latexmk`:

```bash
latexmk -pdf main.tex
```

---

## Struktur Dokumen / Document Structure

### Proposal Tesis (4 Bab)

| Bagian | Isi |
|--------|-----|
| **Bagian Awal** | Halaman Judul, Halaman Pengesahan, Daftar Isi, Daftar Gambar, Daftar Tabel, Intisari, Abstract |
| **Bagian Utama** | Bab 1. Pendahuluan, Bab 2. Tinjauan Pustaka, Bab 3. Metodologi Penelitian, Bab 4. Jadwal Penelitian |
| **Bagian Akhir** | Daftar Pustaka, Lampiran (Paper Referensi Utama, Surat Pernyataan Penggunaan AI) |

### Tesis (6 Bab)

| Bagian | Isi |
|--------|-----|
| **Bagian Awal** | Halaman Judul, Halaman Pengesahan, Daftar Isi, Daftar Gambar, Daftar Tabel, Intisari, Abstract |
| **Bagian Utama** | Bab 1. Pendahuluan, Bab 2. Tinjauan Pustaka, Bab 3. Metodologi Penelitian, Bab 4. Implementasi, Bab 5. Hasil Penelitian dan Pembahasan, Bab 6. Kesimpulan dan Saran |
| **Bagian Akhir** | Daftar Pustaka, Lampiran (Surat Pernyataan Plagiasi, Surat Pernyataan Penggunaan AI, Bukti Submit Paper, Paper Yang di Submit, Hasil Pengecekan Similaritas) |

---

## Struktur Folder / Folder Structure

```
template-tesis-fmipa/
├── main.tex                    # Dokumen utama
├── ugmfmipa.cls                # Document class (formatting rules)
├── references.bib              # Database referensi
├── packages/
│   └── fmipabib.sty           # Style bibliografi FMIPA
├── contents/
│   ├── abstract/
│   │   ├── intisari.tex       # Intisari (Bahasa Indonesia)
│   │   └── abstract.tex       # Abstract (English)
│   ├── chapter-1/             # Bab 1: Pendahuluan
│   ├── chapter-2/             # Bab 2: Tinjauan Pustaka
│   ├── chapter-3/             # Bab 3: Metodologi Penelitian
│   ├── chapter-4/             # Bab 4: Jadwal (proposal) / Implementasi (tesis)
│   ├── chapter-5/             # Bab 5: Hasil Penelitian dan Pembahasan (tesis)
│   ├── chapter-6/             # Bab 6: Kesimpulan dan Saran (tesis)
│   ├── appendix/              # Lampiran
│   ├── dedication/            # Halaman Persembahan (opsional)
│   ├── endorsement/           # Halaman Pengesahan (PDF)
│   ├── nomenclature/          # Daftar Lambang dan Singkatan (opsional)
│   ├── preface/               # Kata Pengantar (opsional)
│   └── statement/             # Pernyataan Bebas Plagiasi (opsional)
└── sample/
    ├── logougm.png            # Logo UGM (berwarna)
    └── logougm-mono.png       # Logo UGM (monokrom)
```

---

## Ketentuan yang Didukung / Supported Guidelines

| Kategori | Ketentuan |
|----------|-----------|
| **Kertas** | A4, margin atas 4cm, kiri 4cm, bawah 3cm, kanan 3cm |
| **Font** | Times 12pt, spasi 1.5 (teks utama), spasi 1 (TOC, abstrak, bibliografi) |
| **Penomoran Halaman** | Romawi kecil (front matter, bawah tengah), Arab (main matter, kanan atas), bawah tengah untuk halaman judul bab |
| **Judul Bab** | Bold, 14pt, kapital, center, nomor Romawi besar |
| **Judul Section** | Bold, 12pt, Title Case, nomor Arab (1.1) |
| **Judul Subsection** | Bold, 12pt, sentence case, nomor Arab (1.1.1) |
| **Subsubsection** | Bold, 12pt, tanpa nomor |
| **Tabel** | Caption bold di atas, nomor per bab (Tabel 4.1) |
| **Gambar** | Caption normal di bawah, nomor per bab (Gambar 3.1) |
| **Persamaan** | Nomor per bab dalam kurung, rata kanan (3.1) |
| **Bibliografi** | Harvard (author-year), DOI ditampilkan, hanging indent |
| **Sampul** | Logo UGM 5.5cm, judul bilingual (Indonesia + English italic) |

---

## Halaman Opsional / Optional Pages

Beberapa halaman bersifat opsional dan di-comment out secara default di `main.tex`. Uncomment jika diperlukan:

```latex
% Halaman Pernyataan Bebas Plagiasi
\chapterstatement{contents/statement/statement}

% Halaman Persembahan
\chapterdedication{contents/dedication/dedication}

% Kata Pengantar
\chapterpreface{contents/preface/preface}

% Daftar Lambang dan Singkatan
\chapternomenclature{contents/nomenclature/nomenclature}
```

---

## Theorem Environments

Template menyediakan environment untuk penulisan matematika:

```latex
\begin{definisi}
Sebuah graf $G = (V, E)$ adalah pasangan himpunan simpul $V$ dan himpunan sisi $E$.
\end{definisi}

\begin{teorema}
Untuk setiap graf $G$ dengan $n$ simpul, berlaku $|E| \leq \binom{n}{2}$.
\end{teorema}

\begin{lema} ... \end{lema}
\begin{akibat} ... \end{akibat}
\begin{proposisi} ... \end{proposisi}
\begin{proof} ... \end{proof}
```

Untuk mode English, gunakan: `theorem`, `definition`, `lemma`, `corollary`, `proposition`.

---

## Sitasi / Citation

Template ini menggunakan sistem sitasi **Harvard (author-year)** dengan biblatex. Perintah `\cite` sudah dikonfigurasi agar otomatis menghasilkan output **dengan kurung**.

### Perintah Sitasi yang Tersedia

| Perintah | Output | Keterangan |
|----------|--------|------------|
| `\cite{ross2004}` | (Ross, 2004) | Sitasi standar dengan kurung |
| `\cite{ross2004, nagle2004}` | (Ross, 2004; Nagle et al., 2004) | Sitasi ganda |
| `\textcite{ross2004}` | Ross (2004) | Sitasi naratif (nama di luar kurung) |

### Contoh Penggunaan

```latex
% Sitasi di akhir kalimat
Deteksi objek telah berkembang pesat dalam beberapa tahun terakhir \cite{ross2004}.

% Sitasi naratif (nama penulis sebagai bagian kalimat)
Menurut \textcite{ross2004}, deteksi objek dapat dilakukan secara real-time.

% Sitasi ganda
Beberapa penelitian telah membahas topik ini \cite{ross2004, nagle2004}.
```

### Catatan Penting

- Semua referensi harus didaftarkan di file `references.bib`
- Gunakan `\cite` untuk sitasi standar (otomatis dengan kurung)
- Gunakan `\textcite` jika nama penulis menjadi bagian dari kalimat
- DOI akan otomatis ditampilkan di daftar pustaka jika tersedia di file `.bib`

---

## Prasyarat / Prerequisites

- **TeX Distribution**: MiKTeX atau TeX Live (terbaru)
- **Engine**: pdfLaTeX
- **Bibliography**: Biber (backend untuk biblatex)
- **Packages**: Semua package yang dibutuhkan akan otomatis ter-install saat compile pertama kali (MiKTeX) atau sudah tersedia di TeX Live full.

---

## Kontributor / Contributors

- [Khalilullah Al Faath](https://github.com/khalilullahalfaath)
- Jeremiah Manurung

Template ini dikembangkan berdasarkan template DTETI UGM yang disesuaikan untuk FMIPA UGM.

---

## Lisensi / License

Template ini dilisensikan di bawah [MIT License](LICENSE).

---

## Changelog

### v1.0 (2026-05-03)

**Initial Release** - Template yang sesuai dengan ketentuan penulisan terbaru FMIPA UGM.

- Mendukung Proposal Tesis (4 bab) dan Tesis (6 bab)
- Bilingual support (Bahasa Indonesia / English)
- Format sesuai ketentuan FMIPA UGM (margin, font, spacing, penomoran)
- Theorem environments (Definisi, Teorema, Lema, Akibat, Proposisi)
- Bibliografi Harvard style dengan DOI support
- Template lampiran lengkap sesuai ketentuan terbaru
- Contoh isi bab untuk Magister Ilmu Komputer (Computer Vision / Deep Learning)

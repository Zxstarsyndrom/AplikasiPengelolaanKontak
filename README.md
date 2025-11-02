# Aplikasi Pengelolaan Kontak

Aplikasi desktop untuk mengelola data kontak (**CRUD**, **pencarian**, **ekspor CSV**) menggunakan **Java Swing** dan **SQLite**. Proyek dikemas sebagai **NetBeans (Ant Project)** sehingga mudah dibuka dan dijalankan.
<img width="427" height="654" alt="image" src="https://github.com/user-attachments/assets/eda9735c-5917-4f14-bc0b-4a7ec288be58" />

[![Build](https://github.com/Zxstarsyndrom/AplikasiPengelolaanKontak/actions/workflows/build.yml/badge.svg)](https://github.com/Zxstarsyndrom/AplikasiPengelolaanKontak/actions/workflows/build.yml)
![Java](https://img.shields.io/badge/Java-Swing-blue)
![DB](https://img.shields.io/badge/DB-SQLite-informational)

---

## Daftar Isi
- [Ringkasan](#ringkasan)
- [Fitur](#fitur)
- [Arsitektur & Tech Stack](#arsitektur--tech-stack)
- [Struktur Proyek](#struktur-proyek)
- [Prasyarat](#prasyarat)
- [Cara Menjalankan](#cara-menjalankan)
  - [Melalui NetBeans](#melalui-netbeans)
  - [Melalui Ant (Terminal)](#melalui-ant-terminal)
- [Ekspor CSV](#ekspor-csv)
- [Skema Database (Opsional)](#skema-database-opsional)
- [Build Artefak (JAR)](#build-artefak-jar)
- [Cuplikan Antarmuka (Opsional)](#cuplikan-antarmuka-opsional)
- [Roadmap](#roadmap)
- [Kontribusi](#kontribusi)
- [Lisensi](#lisensi)
- [Kredit](#kredit)

---

## Ringkasan
- **Tujuan**: Menyediakan pengelolaan kontak yang sederhana dan cepat pada lingkungan desktop.  
- **Fitur utama**: tambah, ubah, hapus, cari kontak; ekspor tabel ke **CSV**.  
- **Penyimpanan**: file database lokal **`contacts.db`** (SQLite) agar instalasi ringan dan portabel.

---

## Fitur
- **CRUD Kontak**: tambah, lihat, ubah, hapus  
- **Pencarian Cepat**: berdasarkan **nama**, **nomor telepon**, atau **kategori**  
- **Ekspor CSV**: data tabel diekspor ke `.csv` (Excel/Google Sheets)  
- **Portabel**: tanpa server—cukup file SQLite di dalam repo  

> Kolom standar: **ID**, **Nama**, **Nomor Telepon**, **Kategori**. Silakan sesuaikan di kode jika struktur diubah.

---

## Arsitektur & Tech Stack
| Layer | Teknologi |
|------:|-----------|
| UI | Java **Swing/AWT** |
| Database | **SQLite** (`contacts.db`) |
| Build System | **NetBeans (Ant)** – `nbproject/`, `build.xml` |

---

## Struktur Proyek
```text
AplikasiPengelolaanKontak/
├─ lib/            # (opsional) dependensi .jar (mis. driver SQLite)
├─ nbproject/      # metadata NetBeans (Ant)
├─ src/            # source code Java (UI + logic/DAO)
├─ contacts.db     # database SQLite contoh
├─ build.xml       # build script Ant (NetBeans)
└─ manifest.mf     # manifest aplikasi

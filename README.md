# aiportal
Kumpulan alat bantu berbasis HTML5-JS seperti aiTools, aiGames, MiniTools, MiniGames, dan MiniSys (Python)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/Frontend-HTML5%20%7C%20Tailwind%20JS-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![Python](https://img.shields.io/badge/MiniSys-Python%20Backend-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Total Tools](https://img.shields.io/badge/Koleksi-125%20Tools%20%2B%2022%20Widgets-indigo)](#daftar--penjelasan-singkat-tiap-tool)

## Ikhtisar
**aiPortal** adalah portal berbasis web yang menyatukan **125 aplikasi web dan utilitas** beserta **22 widget interaktif** ke dalam satu ekosistem terpadu. 

Proyek ini dirancang untuk menjadi halaman beranda (*start page*) sekaligus kotak perkakas digital serbaguna yang mencakup:
1. **Portal Utama (`index.html`):** Antarmuka modern bergaya *glassmorphism* dengan dua mode utama—**Tab Tautan** (direktori terklasifikasi dengan pencarian cepat) dan **Tab Widget** (dasbor produktivitas yang dapat dikustomisasi).
2. **aiTools & aiGames (14 Tools):** Koleksi alat bantu dan gim interaktif berbasis kecerdasan buatan (AI).
3. **MiniTools (55 Tools) + MiniSys (1 Modul Python):** Kumpulan utilitas produktivitas, pengolah dokumen, desain, finansial, hingga sistem mikro lokal berbasis Python.
4. **MiniGames (55 Tools):** Kumpulan gim arkade klasik, teka-teki strategi, hingga simulasi interaktif.

---

## Basis Sistem
* **Arsitektur Hibrida (Static Single-File + Micro-Backend):**
  * **Antarmuka & 124 Tools Mandiri:** Dibangun menggunakan HTML5, Tailwind CSS (via CDN), dan Vanilla JavaScript dalam format *single-file* (`.html`) yang berjalan 100% di sisi klien (*client-side*).
  * **Modul `MiniSys`:** Berjalan di atas *runtime* **Python** (port lokal `http://localhost:5000`) menggunakan arsitektur web ringan dengan penyimpanan berbasis berkas CSV (`url_database.csv`) dan kunci enkripsi/sesi lokal (`secret.key`).
* **Manajemen State Lokal:** Menggunakan `localStorage` pada peramban untuk menyimpan tata letak widget (*drag & drop* via SortableJS), tema (Terang/Gelap), catatan, daftar tugas, hingga progres gim secara persisten tanpa memerlukan akun daring.
* **Konektivitas Adaptif:** Dilengkapi detektor status jaringan otomatis (*Online/Offline Banner*) yang menyesuaikan fungsi widget berbasis internet (Cuaca Open-Meteo, RSS Berita, dan API AI).

---

## Struktur Direktori Proyek
Agar seluruh tautan di dalam `index.html` berfungsi dengan benar, susun ekstraksi berkas Anda ke dalam struktur folder berikut:

```text
aiPortal/
├── index.html               # Halaman utama portal & dasbor 22 widget
├── aitools/                 # Ekstrak isi aiTools.zip (14 file HTML)
├── minitools/               # Ekstrak isi MiniTools.zip (55 file HTML)
├── minigames/               # Ekstrak isi MiniGames.zip (55 file HTML)
└── minisys/                 # Ekstrak isi MiniSys.zip (Modul Python lokal)
    ├── app.py               # Server utama aplikasi MiniSys
    ├── requirements.txt     # Daftar dependensi Python
    ├── secret.key           # Kunci keamanan/enkripsi lokal
    ├── start.bat            # Skrip peluncur otomatis (Windows)
    ├── url_database.csv     # Basis data lokal berbentuk CSV
    └── templates/
        └── index.html       # Antarmuka web MiniSys
```

---

## Daftar & Penjelasan Singkat Tiap Komponen

### 0. Portal Utama (`index.html` — aiPortal Dashboard)
Halaman utama proyek yang memiliki fitur navigasi tab, mode Gelap/Terang (*Dark/Light Mode*), pencarian *real-time* dengan penyorotan kata kunci (*highlight*), tombol **Kejutan** (8 efek *easter egg* visual interaktif), serta **22 Widget Dasbor** yang dapat diatur urutan maupun visibilitasnya:
* **Waktu & Kalender:** Jam Lokal, Jam Dunia (multi-zona waktu), Kalender Bulanan, Timer Fokus (Pomodoro), dan Stopwatch.
* **Produktivitas & Catatan:** Daftar Tugas (*To-Do List*), Catatan Cepat (*auto-save*), Habit Tracker (reset harian otomatis), Pintasan Web (*Bookmarks*), Keuangan Mini, Kalkulator, dan Penghitung (*Counter*).
* **Informasi & Media:** Pencarian Google, Cuaca Dinamis (Open-Meteo), Feed Berita RSS (dapat dikustomisasi), Web/YouTube Viewer, Pemutar Musik MP3 Lokal, Pemutar Video MP4 Lokal, dan Album Memori (kompresi foto lokal).
* **Hiburan & Relaksasi:** Kutipan Motivasi Acak, Relaksasi Pernapasan (*Zen Mode*), serta gim **2048** bawaan.

---

### 1. Kategori Kecerdasan Buatan (`aitools/` — 14 Tools)
| Nama File | Penjelasan Singkat |
| :--- | :--- |
| `aiExpertEngine.html` | Mesin sistem pakar berbasis aturan dan AI untuk konsultasi/analisis topik spesifik. |
| `aiGis.html` | Pemetaan cerdas dan analisis data geografis/spasial berbantuan AI. |
| `aiKaraoke.html` | Pemutar karaoke interaktif dengan sinkronisasi lirik atau pemrosesan vokal/audio cerdas. |
| `aiLab.html` | Ruang eksperimen terpadu untuk menguji pembelajaran mesin dengan Python dan AI. |
| `aiLookup.html` | Alat pencarian informasi cepat dan ringkasan fakta berbasis AI. |
| `aiMediaGen.html` | Antarmuka generator media (gambar/audio/visual) berbasis kecerdasan buatan. |
| `aiQuiz.html` | Pembuat dan simulator kuis otomatis dari materi atau topik yang diberikan. |
| `aiRef.html` | Asisten pencarian referensi, sitasi, dan manajemen literatur cerdas. |
| `MyAI.html` | Asisten AI personal serbaguna untuk kebutuhan harian. |
| `MyAIBuild.html` | Pembangun prototipe aplikasi, kode, atau komponen web berbasis perintah AI. |
| `MyAIChat.html` | Antarmuka percakapan (*chatbot*) interaktif yang bersih dan responsif. |
| `MyAIFlow.html` | Perancang alur kerja (*workflow*) otomatis dan *chaining* perintah AI. |
| `MyAILive.html` | Asisten AI mode *real-time* / interaktif langsung (suara/teks). |
| `MyAIMeme.html` | Generator meme otomatis lengkap dengan ide teks/caption dari AI. |

---

### 2. Kategori Produktivitas, Utilitas & Sistem (`minitools/` & `minisys/` — 56 Tools)

#### A. Modul Backend Lokal (`minisys/`)
| Nama Komponen | Penjelasan Singkat |
| :--- | :--- |
| `MiniSys` (`app.py`) | Aplikasi web mikro berbasis Python (`http://localhost:5000`) yang dilengkapi antarmuka HTML (`templates/index.html`), penyimpanan data terstruktur (`url_database.csv`), kunci keamanan (`secret.key`), dan peluncur instan (`start.bat`). |

#### B. Dokumen, Teks & Kantor (`minitools/`)
| Nama File | Penjelasan Singkat |
| :--- | :--- |
| `Aksara.html` | Alat konversi, pembelajaran, atau pengetikan aksara Nusantara/khusus. |
| `BackOffice.html` | Dasbor manajemen operasional dan administrasi bisnis internal. |
| `DocEdit.html` | Pengolah kata (*rich text editor*) ringan berbasis web. |
| `DocuWiki.html` | Sistem dokumentasi pribadi dan basis pengetahuan bergaya Wiki. |
| `Draftr.html` | Aplikasi penulisan draf artikel atau cerita bebas gangguan (*distraction-free*). |
| `FrontDesk.html` | Sistem pencatatan buku tamu, resepsionis, dan antrean layanan depan. |
| `MyDiary.html` | Jurnal harian pribadi dengan pencatatan suasana hati dan pencarian arsip. |
| `PDFEdit.html` | Alat bantu manipulasi dokumen PDF (gabung, pisah, atau anotasi dasar). |
| `RecPPAT.html` | Alat bantu pencatatan/administrasi dokumen akta atau administrasi pertanahan (PPAT). |
| `Teleprompt.html` | Layar *teleprompter* otomatis dengan pengaturan kecepatan gulir teks untuk presentasi/video. |
| `Textr.html` | Utilitas manipulasi teks massal (ubah kapitalisasi, hapus duplikat, hitung kata, dll.). |
| `WorkSpace.html` | Ruang kerja terpadu untuk mengelola tugas, catatan, dan tautan harian. |

#### C. Data, Keuangan & Analisis (`minitools/`)
| Nama File | Penjelasan Singkat |
| :--- | :--- |
| `CalFit.html` | Kalkulator kalori, indeks massa tubuh (BMI), dan pelacak kebugaran harian. |
| `Cell.html` | Aplikasi lembar kerja (*spreadsheet*) ringan dengan dukungan rumus dasar. |
| `ChartMaker.html` | Pembuat grafik dan visualisasi data instan (batang, garis, lingkaran). |
| `CoreVert.html` | Konverter serbaguna untuk satuan ukuran, mata uang, dan format data. |
| `Fin.html` | Aplikasi pencatatan keuangan pribadi, pemasukan, pengeluaran, dan anggaran. |
| `Matcher.html` | Alat pencocokan dan perbandingan dua daftar data untuk mencari kesamaan/perbedaan. |
| `SmartGraph.html` | Pembuat diagram relasi, *mind map*, dan grafik jaringan cerdas. |
| `SQLGen.html` | Generator kueri SQL visual untuk mempermudah pembuatan perintah basis data. |
| `XMLSX.html` | Alat konversi dan pembaca struktur data antara XML, Excel/CSV, dan JSON. |

#### D. Desain, Media & Visual (`minitools/`)
| Nama File | Penjelasan Singkat |
| :--- | :--- |
| `DMG.html` | Alat bantu pembuatan/pengelolaan aset grafis atau materi digital. |
| `EasyStudio.html` | Studio desain mini untuk membuat poster, kartu, atau konten media sosial. |
| `Fontr.html` | Pratinjau, pembanding, dan pengelola tipografi/font web. |
| `Galeri.html` | Penampil dan pengelola galeri foto lokal dengan mode *slideshow*. |
| `Harmoni.html` | Generator palet warna harmonis untuk kebutuhan desain UI/UX dan grafis. |
| `Kanvas.html` | Papan gambar digital bebas (*freehand drawing*) dengan berbagai pilihan kuas. |
| `Komposer.html` | Alat penyusun komposisi tata letak visual atau musik sederhana. |
| `Origami.html` | Panduan interaktif atau simulator lipatan kertas origami. |
| `Slider.html` | Pembuat presentasi *slide* sederhana langsung dari *browser*. |
| `Vect.html` | Editor grafis vektor (SVG) ringan untuk membuat ilustrasi dan ikon. |
| `VidEdit.html` | Pemotong dan editor video dasar langsung di sisi klien (*browser*). |

#### E. Utilitas Web, Pemetaan & Sistem (`minitools/`)
| Nama File | Penjelasan Singkat |
| :--- | :--- |
| `Diag.html` | Pembuat diagram alir (*flowchart*), UML, dan arsitektur sistem. |
| `EasyGen.html` | Generator serbaguna (QR Code, password acak, UUID, kode *dummy*, dll.). |
| `FastHand.html` | Aplikasi tes dan latihan kecepatan mengetik 10 jari (WPM). |
| `Fidget.html` | Kumpulan mainan virtual pelepas stres (*fidget toys*) interaktif. |
| `FileDrop.html` | Utilitas berbagi atau memproses file lokal secara cepat dengan *drag-and-drop*. |
| `FormBuild.html` | Pembuat formulir survei dan isian web secara visual. |
| `GeoTag.html` | Alat melihat, menyunting, atau menyematkan koordinat GPS (EXIF) pada foto/data. |
| `Hajatan.html` | Aplikasi manajemen acara/hajatan (daftar tamu, anggaran, susunan acara). |
| `Ikhlas.html` | Aplikasi utilitas ibadah/islami (jadwal salat, tasbih digital, atau catatan amal). |
| `Impress.html` | Pembuat halaman profil portofolio atau kartu nama digital yang menarik. |
| `InFeeds.html` | Pembaca berita/umpan RSS terpadu dalam satu halaman bersih. |
| `InfoPage.html` | Pembuat halaman informasi/pengumuman satu layar siap tampil. |
| `InfoPost.html` | Pembuat kartu infografis atau pengumuman ringkas siap bagikan. |
| `LensOCR.html` | Ekstraktor teks dari gambar (*Optical Character Recognition*) berbasis *browser*. |
| `OffGrid.html` | Kumpulan utilitas darurat dan alat bantu yang dirancang bekerja penuh saat *offline*. |
| `Page.html` | Pembuat halaman web statis (*landing page*) sederhana secara visual. |
| `Parti.html` | Alat perencanaan pesta/acara dan pembagian tugas atau patungan biaya. |
| `PasaDena.html` | Sistem manajemen data/katalog khusus terstruktur. |
| `QuickBoard.html` | Papan klip (*clipboard*) sementara dan papan catatan tempel cepat. |
| `Quizr.html` | Pembuat dan pemutar kuis interaktif untuk keperluan edukasi atau acara. |
| `RandNamer.html` | Generator nama acak (nama orang, merek, karakter, atau proyek). |
| `Undian.html` | Aplikasi pengacak nama/nomor undian (*doorprize*) dengan animasi menarik. |
| `VizGis.html` | Penampil dan visualisasi data geografis/peta interaktif berbasis GeoJSON/KML. |

---

### 3. Kategori Gim & Simulasi Interaktif (`minigames/` — 55 Tools)

#### A. Gim Klasik & Arcade
| Nama File | Penjelasan Singkat |
| :--- | :--- |
| `BallOn.html` | Gim arkade pantulan bola melewati rintangan. |
| `Block.html` / `BlockBlast.html` | Gim menyusun dan menghancurkan balok bergaya *puzzle* papan. |
| `Bomber.html` | Gim aksi klasik meletakkan bom untuk menghancurkan rintangan dan musuh. |
| `BrickBreaker.html` | Gim klasik memantulkan bola untuk memecahkan susunan batu bata. |
| `Destroyer.html` | Gim aksi menembak dan menghancurkan target atau armada musuh. |
| `DinoOnline.html` | Gim lari tanpa akhir (*endless runner*) melompati rintangan ala Dino Chrome. |
| `DuckHunt.html` | Gim menembak target bebek terbang klasik. |
| `Force.html` | Gim aksi/fisika berbasis gaya dorong dan gravitasi. |
| `GoBlock.html` | Gim teka-teki menggeser atau mengarahkan balok ke titik tujuan. |
| `GulaGula.html` | Gim *match-3* bertema permen warna-warni. |
| `Labirin.html` | Gim mencari jalan keluar dari labirin yang menantang. |
| `Pacman.html` | Gim arkade klasik memakan titik di labirin sambil menghindari hantu. |
| `Pinball.html` | Simulasi mesin *pinball* klasik dengan fisika pantulan bola. |
| `PingPong.html` | Gim tenis meja/Pong klasik pemain tunggal maupun ganda. |
| `RetroSport.html` | Kumpulan gim olahraga bergaya retro piksel. |
| `Snake.html` | Gim ular klasik memakan umpan agar tumbuh semakin panjang. |
| `SpaceStecu.html` | Gim tembak-menembak pesawat luar angkasa (*space shooter*). |
| `Tetris.html` | Gim menyusun balok jatuh (*tetromino*) klasik. |
| `WhackdBol.html` | Gim ketangkasan memukul objek yang muncul cepat (*whack-a-mole*). |
| `YaBalapan.html` | Gim balapan kendaraan berkecepatan tinggi. |
| `Zuma.html` | Gim menembak bola warna untuk memutus rantai bola yang berjalan. |

#### B. Teka-Teki, Kartu & Papan Strategi
| Nama File | Penjelasan Singkat |
| :--- | :--- |
| `BrainGame.html` | Kumpulan mini-gim untuk melatih daya ingat, logika, dan fokus otak. |
| `Catur.html` | Gim papan catur klasik lengkap dengan aturan langkah standar. |
| `Congklak.html` | Gim tradisional congklak/dakon digital. |
| `Duo.html` | Gim kartu mencocokkan warna dan angka (ala UNO). |
| `Merge.html` | Gim menggabungkan angka atau objek serupa untuk mencapai level tertinggi (ala 2048). |
| `Minesweeper.html` | Gim deduksi logika klasik menyapu ranjau di papan kotak. |
| `Nono.html` | Gim teka-teki logika gambar *Nonogram / Picross*. |
| `Onet.html` | Gim mencocokkan dua ikon identik dengan jalur penghubung maksimal tiga garis. |
| `PushPull.html` | Gim teka-teki mendorong dan menarik kotak (*Sokoban-style*). |
| `Puzzle.html` | Gim menyusun potongan gambar (*jigsaw/sliding puzzle*). |
| `Reversi.html` | Gim papan strategi membalik keping hitam-putih (Othello). |
| `Solitaire.html` | Gim kartu klasik Klondike Solitaire. |
| `Spider.html` | Gim kartu Spider Solitaire dengan tingkat kesulitan bervariasi. |

#### C. Simulasi, Ketangkasan & Lainnya
| Nama File | Penjelasan Singkat |
| :--- | :--- |
| `Ava.html` | Pembuat dan kustomisasi karakter/avatar interaktif. |
| `CyberSim.html` | Simulasi dunia siber, peretasan, atau manajemen jaringan virtual. |
| `DelSim.html` | Simulasi logistik dan pengantaran paket/kurir. |
| `Effector.html` | Alat/gim eksperimen efek visual dan partikel interaktif. |
| `FoneSim.html` | Simulasi antarmuka ponsel pintar lengkap dengan aplikasi mini di dalamnya. |
| `KDKMP.html` | Gim/simulasi bertema lokal atau tantangan khusus interaktif. |
| `LoketRush.html` | Gim manajemen waktu melayani antrean loket dengan cepat. |
| `Nambang.html` | Gim simulasi menambang sumber daya alam dan meningkatkan peralatan. |
| `OnFire.html` | Gim aksi/simulasi pemadaman kebakaran atau bertahan dari rintangan api. |
| `Sawit.html` | Simulasi manajemen perkebunan kelapa sawit dan panen. |
| `ShopSim.html` | Simulasi mengelola toko, stok barang, dan melayani pembeli. |
| `SimCraft.html` | Simulasi merakit (*crafting*) dan membangun dunia berbasis blok. |
| `SimTok.html` | Simulasi membuat konten dan mengelola akun media sosial video pendek. |
| `SkillJump.html` | Gim ketangkasan melompati platform vertikal setinggi mungkin. |
| `SkillSpace.html` | Gim ketangkasan navigasi di ruang angkasa dengan presisi tinggi. |
| `SkillTower.html` | Gim ketangkasan menumpuk menara blok secara presisi. |
| `SoundLab.html` | Laboratorium sintesis suara, *beatmaker*, dan eksperimen audio interaktif. |
| `WhatSim.html` | Simulasi aplikasi perpesanan instan untuk skenario cerita atau dialog. |
| `WindOS.html` | Simulasi sistem operasi desktop klasik berbasis web lengkap dengan jendela aplikasi. |
| `Wireng777.html` | Simulasi mesin ketangkasan/putaran angka hiburan. |

---

## Cara Pasang & Penggunaan

### 1. Persiapan Struktur Folder
1. Buat folder utama bernama `aiPortal` dan letakkan file `index.html` di dalamnya.
2. Ekstrak arsip `aiTools.zip`, `MiniTools.zip`, `MiniGames.zip`, dan `MiniSys.zip` ke dalam subfolder masing-masing (`aitools/`, `minitools/`, `minigames/`, dan `minisys/`) sesuai bagian [Struktur Direktori Proyek](#-struktur-direktori-proyek).

### 2. Menjalankan Portal Utama (`aiPortal`)
* **Cara Instan:** Klik ganda `index.html` untuk membukanya langsung di peramban (*browser*) Anda. Anda dapat menjadikannya halaman beranda (*Home/New Tab*) browser.
* **Menggunakan Local Web Server (Direkomendasikan):**
  ```bash
  # Menggunakan Python 3 dari dalam folder aiPortal
  python -m http.server 8080
  ```
  Kemudian buka `http://localhost:8080` di peramban Anda.

### 3. Menjalankan Modul `MiniSys` (Opsional)
Agar tautan **MiniSys** di dalam kategori *MiniTools* (`http://localhost:5000`) dapat diakses, jalankan server Python-nya terlebih dahulu:

**Untuk Pengguna Windows:**
1. Masuk ke folder `minisys/`.
2. Klik ganda pada berkas `start.bat` (atau jalankan melalui Command Prompt).

**Untuk Pengguna Linux / macOS / Manual:**
```bash
cd minisys
pip install -r requirements.txt
python app.py
```
Setelah server aktif di `http://localhost:5000`, klik tautan **MiniSys** dari halaman utama `aiPortal`.

---

## ⚠️ Keterbatasan Sistem
1. **Sensitivitas Huruf Besar/Kecil (*Case-Sensitivity*) pada OS Berbasis Unix:** Beberapa tautan di dalam `index.html` (khususnya pada direktori `aitools/` seperti `airef.html` atau `aimediagen.html`) ditulis dengan huruf kecil (*lowercase*), sementara nama berkas aslinya menggunakan *CamelCase* (misalnya `aiRef.html`). Pada Windows hal ini berjalan normal, namun jika di-hosting di **Linux** atau **GitHub Pages**, pastikan nama berkas disamakan huruf kecilnya atau sesuaikan atribut `href` di `index.html`.
2. **Penyimpanan Lokal Terikat Browser (*Browser-Bound*):** Seluruh pengaturan widget, daftar tugas, catatan, foto, dan progres gim disimpan di `localStorage` peramban setempat. Menghapus data penjelajahan (*Clear Site Data*) akan mengatur ulang portal ke kondisi awal.
3. **Ketergantungan Internet & API Eksternal:** Fitur portal utama memerlukan koneksi internet untuk memuat Tailwind CSS, FontAwesome, SortableJS, Canvas Confetti, data cuaca (Open-Meteo), serta berita (rss2json). Modul **aiTools** juga memerlukan API Key aktif dari penyedia AI terkait.
4. **Keterbatasan `MiniSys` di Hosting Statis:** Karena `MiniSys` berjalan menggunakan Python (`app.py`), modul ini hanya dapat dijalankan secara lokal atau di server yang mendukung *runtime* Python (tidak dapat berjalan langsung di GitHub Pages statis).

---

## Lisensi (MIT License)

Seluruh kode sumber dalam proyek **aiPortal** beserta kumpulan modul dan perangkat lunak di dalamnya dirilis di bawah **Lisensi MIT (MIT License)**.

### Ringkasan Hak & Ketentuan
* **Bebas Digunakan:** Diizinkan untuk penggunaan pribadi, edukasi, maupun komersial.
* **Bebas Dimodifikasi:** Diizinkan mengubah kode sumber, menambah tautan, atau membuat widget baru.
* **Bebas Didistribusikan:** Diizinkan menyalin, mempublikasikan ulang, atau menggabungkannya ke dalam proyek lain.
* **Kewajiban:** Menyertakan pemberitahuan hak cipta (*copyright notice*) dan teks lisensi MIT ini pada salinan perangkat lunak.
* ⚠️ **Penafian Garansi:** Perangkat lunak disediakan *"sebagaimana adanya"* (*as is*), tanpa jaminan dalam bentuk apa pun.

```text
MIT License

Copyright (c) 2026 aiPortal Project

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

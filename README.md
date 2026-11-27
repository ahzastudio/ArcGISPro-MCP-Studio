# Panduan Lengkap ArcGIS Pro & ArcMap AI Agent + MCP Studio v1.6.4

Selamat datang di panduan resmi **AhzaStudio AI Agent & MCP Studio v1.6.4**. Versi ini menyatukan dukungan **ArcGIS Pro 3.0 s/d 3.7+** dan **ArcMap 10.3 s/d 10.8.2** dalam **1 Lisensi Terpadu** pada perangkat yang sama, dilengkapi pembuatan folder & File Geodatabase otomatis saat ekspor multi-layer, port MCP permanen terpisah antara ArcGIS Pro (`8000`) dan ArcMap (`8001`), dukungan **FreeLLMAPI (Local)**, model **Gemini 4** & Free Tier, serta tabel vektor layout langsung di ArcMap 10.x.

## 1. Unduhan Resmi v1.6.4

| Edisi | Berkas Installer | Kompatibilitas |
| :--- | :--- | :--- |
| **ArcGIS Pro** | `ArcGISPro_AI_Studio_Setup.exe` | ArcGIS Pro 3.0 s/d 3.7+ (Basic, Standard, Advanced) |
| **ArcMap 10.x** | `ArcMap_AI_Studio_Setup.exe` | ArcMap 10.3 s/d 10.8.2 (Self-Contained, tanpa instal .NET) |

Keduanya otomatis mendapatkan **Free Trial 3 Hari** penuh saat pertama kali dipasang, dan pemegang lisensi Tahunan maupun Lifetime otomatis aktif di ArcGIS Pro sekaligus ArcMap pada PC yang sama.

---

## 2. Pembaruan Utama v1.6.4

- **Ekspor Multi-Layer & Pembuatan Folder/GDB Otomatis:** Konversi satu maupun banyak layer sekaligus ke `.shp`, `.geojson`, `.xlsx`, `.csv`, atau File Geodatabase kini otomatis membuat folder tujuan maupun `.gdb` baru jika belum ada — tanpa error `Cannot create output` dan tanpa perlu membuat folder manual.
- **Port MCP Permanen Anti-Bentrok (Pro `8000` & ArcMap `8001`):** ArcMap MCP Studio kini berjalan stabil di port tetap `http://127.0.0.1:8001/mcp` sehingga dapat dibuka bersamaan dengan ArcGIS Pro (`8000`) tanpa konflik port atau perubahan alamat konfigurasi.
- **Sinkronisasi & Salin JSON Kompatibel Semua Klien AI:** Tombol **Sinkronkan Klien & Skill** maupun **Salin JSON** mendukung penuh Antigravity, Cursor, Claude Desktop, Claude Code, Gemini CLI, OpenCode, dan Hermes Agent.
- **Eksekusi Skrip ArcPy Lebih Stabil & Pesan Error Jelas:** Lingkungan eksekusi otomatis mengaktifkan penimpaan output aman, menampilkan pesan error inti secara ringkas, serta menjaga stabilitas perintah beruntun pada FreeLLMAPI dan provider AI lainnya.

---

## 3. Panduan Cepat ArcGIS Pro 3.0 - 3.7+

1. Tutup seluruh jendela ArcGIS Pro.
2. Jalankan `ArcGISPro_AI_Studio_Setup.exe` dan ikuti wizard hingga selesai.
3. Buka ArcGIS Pro dan buka project `.aprx` Anda.
4. **Jika tab `AI AGENT (MCP)` atau Add-In belum muncul (khususnya ArcGIS Pro 3.3 / 3.4+):**
   - Buka menu **Project** -> **Add-In Manager** -> tab **Options**.
   - Pada bagian kebijakan keamanan di bawah, pilih **Load all Add-Ins without restrictions (Least Secure)**.
   - Tutup seluruh jendela ArcGIS Pro lalu buka kembali; tab **AI AGENT (MCP)** akan langsung tampil di Ribbon.
5. Masuk ke tab Ribbon **AI AGENT (MCP)**:
   - Klik **Panel MCP** untuk membuka panel chat AI Spatial Specialist dan pengaturan API Key (mendukung **FreeLLMAPI (Local)**, **Google Gemini 4**, tombol pintas portal API Key tiap provider, serta tombol **Deteksi Otomatis** dan **Tes Koneksi**).
   - Klik **Sinkron Klien MCP** untuk mendaftarkan 43 tool spasial beserta skill *CAT Spatial Specialist* (Topologi, Raster Calculator & Indeks Spektral, serta Replika Layout Bersih `.mxd`) ke Antigravity, Claude Desktop, Claude Code, Cursor, Gemini CLI, OpenCode, dan Hermes Agent.
   - Klik **MCP Konektor** jika ingin terhubung ke ChatGPT, Google Gemini Web, atau Claude.ai Web melalui `https://mcpro.ahzastudio.web.id/mcp`.

---

## 4. Panduan Lengkap ArcMap 10.3 - 10.8.2

### Langkah Pemasangan
1. Tutup seluruh jendela ArcMap 10.x yang sedang terbuka.
2. Jalankan `ArcMap_AI_Studio_Setup.exe` lalu klik **Pasang Sekarang**. Installer akan memasang toolbar Add-In secara otomatis ke seluruh versi ArcMap 10.3 s/d 10.8 yang terpasang.
3. Buka kembali ArcMap 10.x dan buka dokumen peta `.mxd` Anda.
4. Tampilkan toolbar **ArcMap MCP Studio** (4 tombol: *Start Bridge*, *Stop Bridge*, *Buka Studio*, *Cek Status*), lalu klik **Buka Studio**.

### Mengenal 3 Tab Utama di ArcMap Studio
- **AI Spatial Chat:** Layar percakapan langsung ke sesi `.mxd` aktif (terpisah dari Pengaturan API agar API Key selalu aman saat presentasi atau screen-share), dengan respons tabel rapi dan pengaman anti-loop.
- **Pengaturan API:** Pilihan provider AI (`Pollinations`, `Google Gemini 4 / 3.8 / 3.5` dengan penyaringan Free Tier & auto-fallback saat trafik tinggi, `FreeLLMAPI (Local)` pada `http://127.0.0.1:31415`, `Groq`, `Cerebras`, `NVIDIA NIM`, `OpenRouter`, `DeepSeek`, `9Router`, dan `Ollama`), dilengkapi masking API Key, pintasan portal masing-masing provider, dan tombol **Tes Koneksi**.
- **Server & Lisensi:**
  - **Sinkronkan Klien & Skill (1 Klik):** Mendaftarkan **27 tool ArcMap** di port tetap `http://127.0.0.1:8001/mcp` (termasuk pembuatan **tabel vektor langsung ke Page Layout**, ekspor multi-layer otomatis buat folder, label multi-baris berhalo, dan filter wilayah 1-klik + Auto Zoom) beserta skill *CAT Spatial Specialist* ke seluruh AI Agent lokal.
  - **Aktifkan Cloud Relay:** Menghubungkan sesi ArcMap Anda ke gateway `https://mcpro.ahzastudio.web.id/mcp` sehingga tetap bisa diakses dari Claude.ai Web, ChatGPT, atau AI Cloud meski komputer Anda hanya menginstal ArcMap tanpa ArcGIS Pro.

---

## 5. Fitur & Alur Kerja Siap Pakai v1.6.4

- **Ekspor Multi-Layer ke Folder Baru Otomatis (Pro & ArcMap):**
  > "Konversikan layer Batas_Polygon dan Titik_Survei ke folder baru D:\\Project\\SHP dalam format shapefile."
- **Tabel Daftar Koordinat Vektor di Layout (ArcMap 10.x & ArcGIS Pro):**
  > "Buatkan tabel daftar koordinat dari layer Titik_Koordinat dengan kolom No, Nama, X, Y lalu masukkan ke layout aktif."
- **Pelabelan Multi-Baris & Filter Wilayah 1-Klik:**
  > "Filter layer Batas_Kab ke wilayah Situbondo, zoom ke layer tersebut, lalu beri label Nama tebal di atas dan Luas (Ha) di bawah dengan halo putih."
- **Raster Calculator & Indeks Spektral (`NDVI`, `EVI`, `LST`, `NDBI`, `NDWI`, `SAVI`):**
  > "Hitung indeks NDVI dan suhu permukaan (LST °C) dari citra Landsat 8 di peta aktif lalu tampilkan statistik Min, Max, Mean, dan Std."
- **Replika Layout Bersih dari ArcMap (`.mxd`) ke ArcGIS Pro:**
  > "Tiru tata letak layout dari file D:\\Peta\\Template.mxd ke project ArcGIS Pro ini lalu hubungkan ke Map aktif."
- **Otomasi Perbaikan Topology Error (`Sliver Polygon` & `Overlap`):**
  > "Beresin semua topology error layer Hasil_Intersect: perbaiki geometri rusak, hilangkan seluruh overlap antar poligon, gabungkan sliver di bawah 50 m2 ke tetangga dengan batas terpanjang, tambahkan hasilnya ke peta, lalu tampilkan tabel perbandingan sebelum vs sesudah."

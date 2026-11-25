# Panduan Lengkap ArcGIS Pro & ArcMap AI Agent + MCP Studio v1.6.2

Selamat datang di panduan resmi **AhzaStudio AI Agent & MCP Studio v1.6.2**. Versi ini menyatukan dukungan **ArcGIS Pro 3.0 s/d 3.7+** dan **ArcMap 10.3 s/d 10.8.2** dalam **1 Lisensi Terpadu** pada perangkat yang sama.

## 1. Unduhan Resmi v1.6.2

| Edisi | Berkas Installer | Kompatibilitas |
| :--- | :--- | :--- |
| **ArcGIS Pro** | `ArcGISPro_AI_Studio_Setup.exe` | ArcGIS Pro 3.0 s/d 3.7+ (Basic, Standard, Advanced) |
| **ArcMap 10.x** | `ArcMap_AI_Studio_Setup.exe` | ArcMap 10.3 s/d 10.8.2 (Self-Contained, tanpa instal .NET) |

Keduanya otomatis mendapatkan **Free Trial 3 Hari** penuh saat pertama kali dipasang, dan pemegang lisensi Tahunan maupun Lifetime otomatis aktif di ArcGIS Pro sekaligus ArcMap pada PC yang sama.

---

## 2. Panduan Cepat ArcGIS Pro 3.0 - 3.7+

1. Tutup seluruh jendela ArcGIS Pro.
2. Jalankan `ArcGISPro_AI_Studio_Setup.exe` dan ikuti wizard hingga selesai.
3. Buka ArcGIS Pro dan buka project `.aprx` Anda.
4. Masuk ke tab Ribbon **AI AGENT (MCP)**:
   - Klik **Panel MCP** untuk membuka panel chat AI Spatial Specialist dan pengaturan API Key (dilengkapi tombol pintas portal API Key tiap provider dan tombol **Tes Koneksi**).
   - Klik **Sinkron Klien MCP** untuk mendaftarkan 43 tool spasial beserta skill *CAT Spatial Specialist* dan *GIS Topology Error Fixer* ke Antigravity, Claude Desktop, Claude Code, Cursor, Gemini CLI, OpenCode, dan Hermes Agent.
   - Klik **MCP Konektor** jika ingin terhubung ke ChatGPT, Google Gemini Web, atau Claude.ai Web melalui `https://mcpro.ahzastudio.web.id/mcp`.

---

## 3. Panduan Lengkap ArcMap 10.3 - 10.8.2

### Langkah Pemasangan
1. Tutup seluruh jendela ArcMap 10.x yang sedang terbuka.
2. Jalankan `ArcMap_AI_Studio_Setup.exe` lalu klik **Pasang Sekarang**. Installer akan memasang toolbar Add-In secara otomatis ke seluruh versi ArcMap 10.3 s/d 10.8 yang terpasang.
3. Buka kembali ArcMap 10.x dan buka dokumen peta `.mxd` Anda.
4. Tampilkan toolbar **ArcMap MCP Studio** (4 tombol: *Start Bridge*, *Stop Bridge*, *Buka Studio*, *Cek Status*), lalu klik **Buka Studio**.

### Mengenal 3 Tab Utama di ArcMap Studio
- **AI Spatial Chat:** Layar percakapan langsung ke sesi `.mxd` aktif (terpisah dari Pengaturan API agar API Key selalu aman saat presentasi atau screen-share).
- **Pengaturan API:** Pilihan provider AI (Pollinations gratis tanpa API Key, Google Gemini, Groq, Cerebras, OpenRouter, DeepSeek, 9Router, OpenAI, Ollama) dengan masking API Key, pintasan portal masing-masing provider, dan tombol **Tes Koneksi**.
- **Server & Lisensi:**
  - **Sinkronkan Klien & Skill (1 Klik):** Mendaftarkan 24 tool ArcMap beserta 2 skill (*CAT Spatial Specialist* dan *GIS Topology Error Fixer*) ke seluruh AI Agent lokal (Antigravity, Claude Desktop, Claude Code, Cursor, Gemini CLI, OpenCode, dan Hermes Agent).
  - **Aktifkan Cloud Relay:** Menghubungkan sesi ArcMap Anda ke gateway `https://mcpro.ahzastudio.web.id/mcp` sehingga tetap bisa diakses dari Claude.ai Web, ChatGPT, atau AI Cloud meski komputer Anda hanya menginstal ArcMap tanpa ArcGIS Pro.

---

## 4. Otomasi Perbaikan Topology Error (Sliver Polygon & Overlap Hasil Intersect)

Baik di **ArcGIS Pro** maupun **ArcMap 10.x**, Anda dapat langsung membersihkan kesalahan topologi lewat prompt tanpa merusak layer asli (hasil selalu disimpan sebagai layer baru `*_clean_topo.shp`) dan berjalan penuh pada lisensi **Basic, Standard, maupun Advanced**:

- **Audit Geometri, Sliver & Overlap:**
  > "Cek topology error pada layer Hasil_Intersect, deteksi overlap antar poligon dan sliver polygon di bawah 50 m2."
- **Perbaikan Otomatis Penuh:**
  > "Beresin semua topology error layer Hasil_Intersect: perbaiki geometri rusak, hilangkan seluruh overlap antar poligon, gabungkan sliver di bawah 50 m2 ke tetangga dengan batas terpanjang, tambahkan hasilnya ke peta, lalu tampilkan tabel perbandingan sebelum vs sesudah."
- **Hilangkan Overlap dengan Kolom Prioritas:**
  > "Hilangkan overlap pada layer Kawasan_Gabungan dengan prioritas field KELAS dan simpan sebagai layer baru."

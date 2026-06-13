# ELECTRASIM

Simulator sistem tenaga listrik berbasis web (HTML statis, tanpa build step).
Dibagi menjadi tiga tahap rantai pasok tenaga listrik:

| Tahap | Modul | Berkas | Status |
|-------|-------|--------|--------|
| 1 | **Pembangkit** — Konsol operator PLTGU combined-cycle (SimPLTGU), jaga frekuensi 50 Hz, kelola bahan bakar/keandalan/emisi/laba. Tampilan 3D (Three.js) & diagram satu garis (SLD). | `pembangkit.html` | ✅ Siap |
| 2 | **Transmisi** — Penjelajahan gardu induk 150/20 kV orang-pertama, misi keselamatan kerja (APD/K3). | `transmisi.html` | ✅ Siap |
| 2 | **Transmisi** — SimDispatch: konsol Pusat Pengatur Beban (P2B) Jamali, economic dispatch & merit order, kendali frekuensi/cadangan (N-1). | `dispatch.html` | ✅ Siap |
| 3 | **Distribusi** — Konstruksi SUTM 20 kV: game 3D orang-pertama — kenakan APD, panjat tiang, kuis tiap langkah, pasang travers/isolator/konduktor/proteksi/grounding hingga energize. | `distribusi.html` | ✅ Siap |
| 3 | **Distribusi** — Yantek (Pelayanan Teknik): penanganan gangguan SUTM (kabel putus akibat binatang) + inspeksi gardu zoom-in & ganti NH Fuse, lalu penormalan tegangan. | `yantek.html` | ✅ Siap |

`index.html` adalah halaman menu utama yang menautkan ketiga modul di atas.

## Menjalankan

Buka `index.html` di peramban, atau jalankan server statis lokal:

```bash
python3 -m http.server 8000
# lalu buka http://localhost:8000
```

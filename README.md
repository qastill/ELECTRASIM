# ELECTRASIM

Simulator sistem tenaga listrik berbasis web (HTML statis, tanpa build step).

**Homepage = ElectraSim VR 3D** (`index.html`) — satu app 3D berbasis misi untuk
**16 jalur spesialisasi** ketenagalistrikan (128 misi), dipandu AI instructor VOLTA.
Misi tiap jalur **berjenjang**: terkunci 🔒 sampai misi sebelumnya selesai (M1→M8),
"Misi Berikutnya" melanjutkan sampai tuntas; progres tersimpan di `localStorage`.

## Simulator 3D ElectraSim (tertanam per jalur)

Enam simulator interaktif tampil sebagai entri **3D** di dalam jalur yang sesuai pada menu VR 3D:

| Simulator | Berkas | Jalur |
|-----------|--------|-------|
| SimPLTGU — Konsol Operator PLTGU | `pembangkit.html` | 07 · Pembangkitan & Renewable |
| Gardu Induk 150/20 kV — POV & Misi K3 | `transmisi.html` | 04 · Transmisi |
| SimDispatch — Pengatur Beban (P2B) | `dispatch.html` | 04 · Transmisi |
| Konstruksi SUTM 20 kV | `distribusi.html` | 03 · Distribusi |
| Yantek — Penanganan Gangguan | `yantek.html` | 03 · Distribusi |
| Sambungan Pelanggan & Wiring APP (kWh 1-3-4-6) | `pelanggan.html` | 03 · Distribusi |

`gardu150.html` adalah jelajah bebas gardu 150/20 kV bawaan VR 3D (Jalur 04).
Misi tiap jalur dimuat dari `missions/jalur01–16.js`; gambar di `foto/`.

## Menjalankan

Buka `index.html` di peramban, atau jalankan server statis lokal:

```bash
python3 -m http.server 8000
# lalu buka http://localhost:8000
```

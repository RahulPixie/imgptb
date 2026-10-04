# imgptb — Aset Gambar PTB STMKG 2026

Repositori ini menyimpan aset gambar untuk website **Penerimaan Taruna Baru (PTB) STMKG 2026**. Semua file disajikan melalui **jsDelivr** sebagai CDN publik.

## Struktur Repositori

```
.
├── img/
│   ├── [NamaTaruna].png       # Foto taruna/taruni
│   ├── demustar.png           # Aset demustar
│   ├── poltar.png             # Aset poltar
│   └── resimen.png            # Aset resimen
└── readme.md
```

Semua gambar berada di dalam folder `img/`. Tidak ada subfolder tambahan.

## Penamaan File

| Kategori | Format | Contoh |
|---|---|---|
| Foto taruna/taruni | `NamaLengkap.ekstensi` | `ArfanyDhimasMuftareza.png` |
| Aset kegiatan | `nama-aset.ekstensi` | `demustar.png`, `poltar.png` |

Ekstensi yang digunakan: `.png`, `.jpg`, `.jpeg` (case-insensitive, tapi disarankan konsisten lowercase).

## Penggunaan via jsDelivr

Format URL:

```
https://cdn.jsdelivr.net/gh/RahulPixie/imgptb@VERSI/img/NAMA-FILE
```

### Contoh Foto Taruna

```html
<img src="https://cdn.jsdelivr.net/gh/RahulPixie/imgptb@v1.0.0/img/ArfanyDhimasMuftareza.png" alt="Arfany Dhimas Muftareza">
```

### Contoh Aset Kegiatan

```html
<img src="https://cdn.jsdelivr.net/gh/RahulPixie/imgptb@v1.0.0/img/demustar.png" alt="Demustar">
<img src="https://cdn.jsdelivr.net/gh/RahulPixie/imgptb@v1.0.0/img/poltar.png" alt="Poltar">
<img src="https://cdn.jsdelivr.net/gh/RahulPixie/imgptb@v1.0.0/img/resimen.png" alt="Resimen">
```

### CSS Background

```css
.hero {
  background-image: url('https://cdn.jsdelivr.net/gh/RahulPixie/imgptb@v1.0.0/img/resimen.png');
  background-size: cover;
  background-position: center;
}
```

## Versioning

Kunci versi aset dengan **tag Git** supaya perubahan gambar tidak merusak tampilan website secara tiba-tiba.

```bash
git tag v1.0.0
git push origin v1.0.0
```

| Skema URL | Perilaku |
|---|---|
| `@latest` | Selalu ikuti commit terbaru di branch `main` |
| `@v1.0.0` | Terkunci pada tag tersebut |
| `@main` | Ikuti branch `main` (tidak disarankan untuk produksi) |

## Catatan Cache

jsDelivr melakukan cache agresif (hingga 7 hari untuk URL non-versi). Jika gambar diperbarui tetapi URL masih sama, perubahan tidak langsung terlihat.

Solusi:
1. Buat tag versi baru setiap kali ada perubahan gambar, **atau**
2. Tambahkan query string: `?v=2` di akhir URL

## Aturan Upload

- Upload gambar melalui **PicGo** (sudah terkonfigurasi ke repo ini)
- Maksimal ukuran file: **500 KB** per gambar
- Resolusi maksimal: **2000 px** di sisi terpanjang
- Gunakan nama file yang deskriptif tanpa spasi
- Sertakan `alt` text yang jelas saat memakai gambar di HTML

## Lisensi

Aset visual di repositori ini adalah milik **STMKG** dan **BMKG**. Penggunaan di luar keperluan website resmi PTB STMKG 2026 memerlukan izin tertulis.

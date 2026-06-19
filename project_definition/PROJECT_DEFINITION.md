# Project Definition
**WebGIS Development Bootcamp Batch 3**

## Informasi Project
**Nama Project WebGIS:**
Pemetaan Potensi Pertanian, Irigasi, dan Produktivitas Lahan Kabupaten Sumbawa

**Nama Peserta:**
Titanio Yudista - Universitas Cakrawala

## 1. Ide Project
WebGIS ini dibuat untuk menampilkan dan mengelola data spasial pertanian di wilayah Kabupaten Sumbawa. Informasi yang ditampilkan meliputi Lahan Baku Sawah, Lahan Sawah Dilindungi, Lahan Pertanian Pangan Berkelanjutan (LP2B), daerah dan jaringan irigasi, pola dan intensitas tanam, tingkat produktivitas lahan, komoditas pertanian, serta sebaran alat dan mesin pertanian (Alsintan).

Data spasial akan disimpan dalam format GeoJSON dan dikelola melalui GEO MAPID sebagai database utama. Data tersebut kemudian akan dipanggil dan ditampilkan kembali pada WebGIS interaktif untuk memudahkan pemantauan dan analisis potensi pertanian daerah.

## 2. Permasalahan yang Diangkat
Kabupaten Sumbawa memiliki potensi pertanian yang besar, namun informasi mengenai sebaran lahan pertanian, kondisi irigasi, pola tanam, ketersediaan alat dan mesin pertanian (Alsintan), serta tingkat produktivitas komoditas belum terpetakan dan terintegrasi secara digital dengan baik. Data yang masih tersebar menyulitkan pemerintah daerah, penyuluh pertanian, dan masyarakat dalam memantau kondisi lahan maupun sarana prasarana pertanian secara real-time. Hal ini berdampak pada kurang optimalnya pengambilan keputusan terkait ketahanan pangan, distribusi sumber daya air, manajemen peralatan pertanian, dan pengembangan komoditas unggulan di Kabupaten Sumbawa.

## 3. Target Pengguna
- **Pemerintah Daerah (Dinas Pertanian):** Untuk keperluan perencanaan, monitoring, dan evaluasi kebijakan ketahanan pangan serta pengelolaan lahan pertanian.
- **Penyuluh Pertanian:** Untuk memberikan rekomendasi pola tanam dan strategi peningkatan produktivitas kepada petani.
- **Masyarakat dan Petani:** Untuk mendapatkan informasi mengenai potensi lahan, ketersediaan irigasi, komoditas, serta keberadaan alat dan mesin pertanian di wilayahnya.
- **Akademisi dan Peneliti:** Sebagai data pendukung dalam riset pengembangan sektor pertanian di Kabupaten Sumbawa.

## 4. Data yang Digunakan
Data spasial yang digunakan dalam perancangan WebGIS ini terdiri dari:

- **Lahan Baku Sawah (LBS) dan Lahan Sawah Dilindungi (LSD):**
  Sumber: Dinas Pertanian Kabupaten Sumbawa / Kementerian ATR/BPN.
- **Lahan Pertanian Pangan Berkelanjutan (LP2B):**
  Sumber: Bappeda / Dinas Pertanian Kabupaten Sumbawa.
- **Infrastruktur Irigasi (Daerah Irigasi, Jaringan, dan Bangunan Irigasi):**
  Sumber: Dinas PUPR / Balai Wilayah Sungai terkait.
- **Pola dan Intensitas Tanam & Komoditas Pertanian:**
  Sumber: Data Statistik Pertanian Daerah / BPS Kabupaten Sumbawa.
- **Tingkat Produktivitas Lahan:**
  Sumber: Data Panen dan Hasil Pertanian Dinas Pertanian Kabupaten Sumbawa.
- **Alat dan Mesin Pertanian (Alsintan):**
  Sumber: Data Catalog GEO MAPID atau Dinas Pertanian Kabupaten Sumbawa.
- **Batas Administrasi Kecamatan/Desa Kabupaten Sumbawa:**
  Sumber: Data Catalog GEO MAPID atau portal data pemerintah (BIG).

Seluruh data akan diolah menggunakan format GeoJSON dan disimpan sebagai layer terpisah di GEO MAPID. Layer dari GEO MAPID kemudian akan diakses untuk ditampilkan pada WebGIS.

## 5. Fitur yang Ingin Dibuat
Referensi tampilan dan fitur yang digunakan dalam perancangan WebGIS ini meliputi:
- **Landing page:** Halaman utama yang menjelaskan tujuan WebGIS.
- **Peta Interaktif:** Tampilan peta utama yang menampilkan layer spasial pertanian.
- **Panel Layer dan Filter:** Fitur untuk mengaktifkan/menonaktifkan layer dan memfilter data fasilitas/komoditas/Alsintan.
- **Popup Informasi:** Menampilkan detail atribut ketika poligon lahan, titik fasilitas, atau lokasi Alsintan dipilih.
- **Legenda:** Keterangan visual untuk area jangkauan dan tipe lahan yang ditampilkan.
- **Ringkasan Data:** Menampilkan grafik atau angka ringkasan terkait produktivitas dan luas lahan.

Tampilan WebGIS akan dibuat sederhana agar informasi mudah dipahami oleh pengguna.

## 6. Referensi Tampilan / Inspirasi
https://gispaperta.web.id/ (WebGIS Pertanian Kabupaten Batang)

## 7. Output Akhir yang Diharapkan
Output akhir yang diharapkan adalah WebGIS interaktif yang dapat memberikan informasi terintegrasi mengenai potensi lahan, irigasi, alat dan mesin pertanian (Alsintan), komoditas, dan produktivitas pertanian di Kabupaten Sumbawa.

Project ini akan menghasilkan:
- Project GEO MAPID yang berisi layer data pertanian dalam format GeoJSON.
- WebGIS dengan peta interaktif, filter layer komoditas/produktivitas/Alsintan, popup, dan legenda.
- Repository GitHub yang berisi source code project.
- WebGIS yang dapat diakses secara publik melalui link deployment.
- Portfolio WebGIS yang dapat menunjukkan kemampuan peserta dalam mengelola data spasial pertanian menggunakan GEO MAPID dan menampilkannya pada aplikasi WebGIS.

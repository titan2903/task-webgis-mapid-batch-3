# Task Day 3: GIS Fundamental - Bootcamp WebGIS MAPID

Repository ini berisi hasil pengerjaan **Task Day 3: GIS Fundamental** dalam rangkaian Bootcamp WebGIS MAPID. Proyek ini berfokus pada eksplorasi, pengolahan, analisis spasial sederhana, dan visualisasi data menggunakan perangkat lunak **QGIS** serta pengujian web map menggunakan **Geo MAPID Online Tools**.

## Identifikasi Proyek
* **Nama Peserta:** Titanio Yudista
* **Wilayah Studi:** Jakarta Selatan, DKI Jakarta, Indonesia
* **Tema Analisis:** Aksesibilitas Cafe Terhadap Layanan Transportasi Massal (Halte Transjakarta)

---

## Folder dan Struktur File
Proyek ini diorganisasikan dengan struktur folder sebagai berikut:
```text
task_gis_fundamental/
├── data/                      # Dataset spasial hasil akuisisi dan pengolahan
│   ├── buffer_transjakarta_500m.geojson   # Area jangkauan halte 500m (Buffer)
│   ├── cafe_akses_brt.geojson             # Cafe yang berada di dalam radius buffer 500m
│   ├── sample_cafe.geojson                # Sampel layer titik cafe hasil digitasi/copy-paste
│   ├── sample_highway.geojson             # Sampel layer garis jalan hasil digitasi/copy-paste
│   └── (file lainnya...)
├── images/                    # Screenshot hasil visualisasi
│   ├── qgis.png               # Tampilan layout / styling di QGIS (1)
│   ├── qgis2.png              # Tampilan layout / styling di QGIS (2)
│   └── isochrone_geo_mapid.png# Peta analisis isochrone di platform Geo MAPID
├── LAPORAN.md                 # Laporan ringkas dalam format Markdown
├── LAPORAN.docx               # Laporan ringkas dalam format Microsoft Word (.docx)
├── query.txt                  # Query Overpass API yang digunakan untuk download data
├── hands_on.md                # Panduan teknis langkah-langkah pengerjaan
└── README.md                  # Dokumentasi proyek (file ini)
```

---

## Analisis Spasial & Metodologi
1. **Akuisisi Data:** Data diperoleh dari OpenStreetMap menggunakan Overpass Turbo (`query.txt`) untuk mengambil data Cafe (`amenity=cafe`), Halte Transjakarta (`network=Transjakarta`), dan Jaringan Jalan (`highway=primary|secondary|tertiary`).
2. **Transformasi Koordinat:** Reprojeksi dari koordinat geografis **WGS 84 (EPSG:4326)** ke koordinat terproyeksi **WGS 84 / UTM Zone 48S (EPSG:32748)** untuk melakukan analisis jarak (*buffer*) secara akurat dalam satuan meter.
3. **Analisis Buffer (Jangkauan Halte):** Membuat area penyangga (*buffer*) sejauh 500 meter di sekitar halte Transjakarta untuk merepresentasikan jarak jalan kaki ideal (aksesibel).
4. **Analisis Aksesibilitas (Spatial Join):** Mengidentifikasi cafe-cafe yang berada di dalam radius buffer 500 meter (diberi status `"Mudah Diakses"`) dan di luar radius buffer (diberi status `"Sulit Diakses"`).
5. **Digitasi Layer Sampel:** Membuat layer titik `sample_cafe` dan layer garis `sample_highway` dari hasil seleksi fitur secara manual guna kebutuhan analisis WebGIS terfokus.
6. **Ekspor & Publikasi:** Seluruh layer di-export kembali ke format **GeoJSON** dengan CRS **WGS 84 (EPSG:4326)** dan diunggah ke portal **Geo MAPID** untuk uji coba visualisasi berbasis web.

---

## Potensi Pemanfaatan untuk WebGIS
Data dan hasil pengolahan ini siap diintegrasikan ke tahap pengembangan WebGIS tingkat lanjut untuk:
* **Peta Interaktif Lokasi Bisnis:** Membantu pengguna mencari cafe terdekat yang memiliki akses transportasi publik yang mudah.
* **Analisis Wilayah (TOD - Transit Oriented Development):** Memvisualisasikan hubungan antara titik transit transportasi massal dengan pertumbuhan sektor komersil di sekitarnya.
* **Dashboard Analitik:** Menyajikan persentase cafe ramah pedestrian berbasis grafik interaktif pada peta WebGIS.

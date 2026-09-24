# RENCANA PEMBELAJARAN SEMESTER (RPS) BERBASIS OBE

**Mata Kuliah:** *Internet of Things* (IoT)  
**Bobot SKS:** 3 SKS (1 Teori, 2 Praktikum)  
**Semester:** Ganjil / Genap  
**Prasyarat:** Algoritma dan Pemrograman Dasar, Jaringan Komputer dan Komunikasi Data

---

## 1. Deskripsi Mata Kuliah
Mata kuliah ini dirancang dengan pendekatan *Hands-on* dan *Project-Based Learning* (PjBL) untuk membekali mahasiswa dengan keterampilan praktis membangun ekosistem *Internet of Things* (IoT) secara *end-to-end*. Fokus utama meliputi perakitan perangkat keras berbasis ESP32, akuisisi data sensor (khususnya sensor lingkungan/pertanian), penggunaan protokol komunikasi MQTT, hingga integrasi dengan *backend* web (Firebase/Laravel). Sebagai pengayaan, mata kuliah ini memperkenalkan penerapan algoritma *Machine Learning* sederhana untuk analisis data sensor, memungkinkan sistem IoT tidak hanya mengumpulkan data, tetapi juga menghasilkan keputusan yang cerdas.

## 2. Capaian Pembelajaran Lulusan (CPL) yang Dibebankan
*   **CPL-1 (Sikap):** Menunjukkan sikap bertanggung jawab, disiplin, dan inovatif dalam menyelesaikan proyek teknologi informasi secara mandiri maupun dalam tim.
*   **CPL-2 (Pengetahuan):** Menguasai konsep dasar elektronika, mikrokontroler, protokol jaringan komputer, dan fundamental *Machine Learning* untuk pemrosesan data.
*   **CPL-3 (Keterampilan Umum):** Mampu mendokumentasikan, merancang, dan menyajikan hasil integrasi sistem perangkat keras dan lunak secara terstruktur.
*   **CPL-4 (Keterampilan Khusus):** Mampu merakit perangkat IoT, memprogram mikrokontroler untuk akuisisi dan transmisi data ke *cloud*, serta mengimplementasikan model prediksi berbasis data sensor.

## 3. Capaian Pembelajaran Mata Kuliah (CPMK)
*   **CPMK-1:** Mahasiswa mampu merangkai dan memprogram ESP32 beserta komponen I/O (sensor dan aktuator) secara mandiri.
*   **CPMK-2:** Mahasiswa mampu mengimplementasikan protokol komunikasi IoT (HTTP/REST API dan MQTT) untuk transmisi data dari perangkat *edge* ke *server*.
*   **CPMK-3:** Mahasiswa mampu membangun jembatan data (*data pipeline*) dari perangkat IoT ke platform *cloud*, *database* NoSQL (Firebase), atau sistem web kustom (PHP/Laravel).
*   **CPMK-4:** Mahasiswa mampu memahami dan mengintegrasikan model *Machine Learning* dasar (klasifikasi/prediksi) ke dalam ekosistem IoT sebagai bentuk pengayaan analitik.
*   **CPMK-5:** Mahasiswa mampu merancang, merakit, menguji, dan mendemonstrasikan purwarupa sistem IoT fungsional berbasis studi kasus nyata.

---

## 4. Rencana Kegiatan Pembelajaran Mingguan (16 Pertemuan)

| Minggu | Kemampuan Akhir yang Diharapkan (Sub-CPMK) | Materi Pembelajaran | Bentuk & Metode Pembelajaran | Penilaian (Indikator & Kriteria) | Bobot | Materi |
| :--- | :--- | :--- | :--- | :--- | :--- |:--- |
| **1** | Mampu memahami anatomi sistem IoT secara keseluruhan. | 1. Arsitektur IoT (*Perception, Network, Application*)<br>2. Pengenalan ESP32 vs mikrokontroler lain | Kuliah Interaktif, Diskusi<br>*(TM: 1x50", BM: 2x60")* | Ketepatan menjelaskan lapisan arsitektur sistem IoT. | 2% | [Week_1](./Week_1/)
| **2** | Mampu mengatur lingkungan kerja dan memprogram I/O digital dasar. | 1. Instalasi Arduino IDE / PlatformIO<br>2. *Wiring* komponen di *Breadboard*<br>3. Pemrograman GPIO (LED, *Push Button*) | Praktikum, *Hands-on*<br>*(TM: 1x50", P: 2x170")* | Keberhasilan *upload program* dan manipulasi I/O digital. | 5% |
| **3** | Mampu melakukan akuisisi data menggunakan sensor. | 1. Pembacaan Sensor Analog vs Digital<br>2. Praktik Sensor Lingkungan (Suhu/Kelembaban DHT22, Kelembaban Tanah/NDVI) | Praktikum, *Hands-on*<br>*(TM: 1x50", P: 2x170")* | Akurasi konversi nilai raw sensor menjadi satuan standar (Celcius, %RH). | 7% |
| **4** | Mampu mengontrol perangkat eksternal melalui aktuator. | 1. Konsep *Relay* (AC/DC Load)<br>2. Kontrol *Servo* dan Motor DC<br>3. Logika kontrol berbasis *threshold* sensor | Praktikum, *Problem-based*<br>*(TM: 1x50", P: 2x170")* | Sistem mampu menggerakkan aktuator berdasarkan batas nilai sensor tertentu. | 7% |
| **5** | Mampu mengkoneksikan perangkat ke jaringan Internet. | 1. Konfigurasi WiFi pada ESP32<br>2. Komunikasi HTTP GET/POST<br>3. Memanggil API eksternal (BMKG/Cuaca) | Praktikum<br>*(TM: 1x50", P: 2x170")* | Modul terhubung ke AP lokal dan berhasil melakukan HTTP Request. | 5% |
| **6** | Mampu mengimplementasikan protokol MQTT untuk efisiensi *bandwidth*. | 1. Konsep *Publish/Subscribe*<br>2. Setup *Broker* MQTT (Mosquitto/HiveMQ)<br>3. Mengirim dan menerima data via MQTT | Praktikum<br>*(TM: 1x50", P: 2x170")* | Data terkirim secara *real-time* ke broker MQTT tanpa *delay* berlebih. | 7% |
| **7** | Mampu mengintegrasikan *hardware* IoT dengan ekosistem Web. | 1. Menyimpan data ke Firebase Realtime Database<br>2. Membuat API sederhana (*Endpoint* web PHP/Laravel) untuk menerima data | Praktikum, *Project-based*<br>*(TM: 1x50", P: 2x170")* | Data terekam di *database* cloud dan dapat dipanggil melalui web. | 7% |
| **8** | **Evaluasi Tengah Semester (UTS)** | **Review Materi & Pengajuan Proposal Proyek Akhir** | **Presentasi Ide Proyek** | **Kelayakan teknis dari skema *hardware*, komunikasi data, dan studi kasus.** | **15%** |
| **9** | Mampu memvisualisasikan data IoT ke dalam bentuk *Dashboard*. | 1. Menampilkan data di Grafana / ThingsBoard<br>2. Membuat UI *dashboard* responsif (TailwindCSS/JS sederhana) | Praktikum<br>*(TM: 1x50", P: 2x170")* | Kejelasan grafik dan latensi pembaruan antarmuka *dashboard*. | 5% |
| **10** | **[Pengayaan ML 1]** Mampu merancang alur pengumpulan dataset untuk model ML. | 1. Menyimpan log data runtun waktu (*time-series log*) ke CSV/Database<br>2. Pelabelan data (*Data Labeling*) kondisi normal vs anomali (misal: tanah kering vs subur) | Kuliah Interaktif, Praktikum<br>*(TM: 1x50", P: 2x170")* | Mahasiswa menghasilkan 1 *dataset* valid dari sensor fisik. | 5% |
| **11** | **[Pengayaan ML 2]** Mampu melatih dan menanamkan ML klasifikasi dasar. | 1. Pengenalan platform *Edge Impulse* / Weka<br>2. *Training* model *Decision Tree*/*Random Forest* sederhana<br>3. Menarik API inferensi / *Library* statis ke ESP32 | Praktikum, Demonstrasi<br>*(TM: 1x50", P: 2x170")* | Akurasi *training* model mencapai standar minimum untuk klasifikasi. | 10% |
| **12** | Mampu melakukan inferensi lokal (*Edge*) atau via *Cloud API*. | 1. Mengirim data *live* sensor ke model untuk diprediksi<br>2. Memicu aktuator berdasarkan hasil inferensi ML | Praktikum, *Problem-based*<br>*(TM: 1x50", P: 2x170")* | Sistem bereaksi (aktuasi) berdasarkan prediksi model, bukan sekadar *threshold* statis. | 10% |
| **13** | Mampu merancang Node IoT hemat energi untuk implementasi lapangan. | 1. Mode *Deep Sleep* ESP32<br>2. Transmisi periodik (Bangun -> Baca Sensor -> Kirim MQTT -> Tidur) | Praktikum<br>*(TM: 1x50", P: 2x170")* | Pengurangan konsumsi arus (dapat didemonstrasikan/diukur). | 5% |
| **14** | Pengembangan Proyek Akhir Terintegrasi (Tahap Perakitan & *Coding*). | *Mentoring* dan perakitan purwarupa Node IoT (Sensor, ESP32, Casing, Catu Daya). | Pembelajaran Berbasis Proyek (PjBL)<br>*(P: 3x170")* | Progres alat fisik siap uji dan *source code* bebas *error*. | - |
| **15** | Pengembangan Proyek Akhir Terintegrasi (Tahap Pengujian Lapangan). | Kalibrasi pembacaan sensor di lingkungan nyata, pengujian stabilitas koneksi, dan penulisan laporan akhir. | Pembelajaran Berbasis Proyek (PjBL)<br>*(P: 3x170")* | Kesesuaian sistem dengan spesifikasi rancangan awal. | - |
| **16** | **Evaluasi Akhir Semester (UAS)** | **Demonstrasi Proyek Akhir & Pameran (Studi Kasus Implementatif)** | **Presentasi & Ujian Lisan** | **Fungsi sistem, keandalan pengiriman data, ketepatan analisis ML, dan kerapian *hardware*.** | **10%** |

---

## 5. Sistem Penilaian (OBE Assessment)

| Komponen Penilaian | Terkait dengan CPMK | Persentase Bobot | Keterangan |
| :--- | :--- | :--- | :--- |
| **Tugas & Laporan Praktikum (Mingguan)** | CPMK-1, CPMK-2 | 25% | Menilai kedisiplinan dan keberhasilan *hands-on* modul mingguan. |
| **Tugas Pengayaan (ML & Cloud Web)** | CPMK-3, CPMK-4 | 20% | Menilai implementasi MQTT, integrasi Firebase/Laravel, dan *training* dataset ML. |
| **Ujian Tengah Semester (UTS)** | CPMK-1, CPMK-2 | 15% | Evaluasi konsep, arsitektur, dan proposal proyek alat IoT. |
| **Proyek Akhir Purwarupa IoT (UAS)** | CPMK-5 | 40% | Demo fisik perangkat terintegrasi, laporan teknis lapangan, dan presentasi tim. |
| **TOTAL** | | **100%** | |

## 6. Referensi & Daftar Pustaka

**Buku Utama:**
1. Kurniawan, A. (2019). *Smart Internet of Things Projects*. Packt Publishing.
2. Warden, P., & Situnayake, D. (2019). *TinyML: Machine Learning with TensorFlow Lite on Arduino and Ultra-Low-Power Microcontrollers*. O'Reilly Media. *(Sebagai modul pengayaan)*

**Referensi Pendukung / Perangkat Lunak:**
1. Dokumentasi Resmi Espressif ESP32.
2. Dokumentasi protokol MQTT (Mosquitto/HiveMQ).
3. Dokumentasi Integrasi Web API (*Laravel API Documentation* / *Firebase Docs*).
4. Platform *Edge AI*: Edge Impulse (*docs.edgeimpulse.com*).

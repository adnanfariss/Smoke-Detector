![alt text](https://github.com/adnanfariss/Smoke-Detector/blob/main/assets/project-2.1.jpg?raw=true)

**Kata Pengantar**

Tempat umum adalah ruang yang seharusnya aman dan nyaman bagi semua orang. Namun, seringkali kita menemui masalah yang mengganggu ketertiban dan kesehatan, seperti kebiasaan merokok di area yang seharusnya bebas rokok. Sekolah, sebagai salah satu tempat umum yang seharusnya menjadi zona aman bagi siswa, justru sering menjadi tempat pelanggaran aturan ini. Meskipun sudah ada peraturan Kawasan Tanpa Rokok (KTR), masih banyak siswa, guru, bahkan petugas sekolah yang merokok di area tersembunyi seperti toilet.

Masalah ini tidak hanya melanggar aturan, tetapi juga membahayakan kesehatan siswa lain yang menjadi perokok pasif. Untuk mengatasi hal ini, kami menciptakan **Asmo (Anti-Smoking Detector)**, sebuah alat inovatif yang dirancang untuk mendeteksi dan mencegah aktivitas merokok di area sekolah, terutama di toilet. Alat ini akan kami perkenalkan dalam pameran Inovasi Teknologi pada Pekan P5 di sekolah kami pada Oktober 2024.

---

**Rumusan Masalah**

1. **Toilet sebagai Lokasi Rahasia Merokok**: Toilet sering menjadi tempat favorit siswa untuk merokok karena sulit diawasi.
2. **Pelanggaran yang Tidak Terdeteksi**: Banyak kasus merokok di sekolah yang tidak terdeteksi oleh guru atau staf.
3. **Dampak Kesehatan**: Asap rokok di toilet tidak hanya mengganggu kenyamanan, tetapi juga membahayakan kesehatan siswa lain, terutama yang menjadi perokok pasif.

---

**Tujuan Penelitian**

Tujuan utama proyek ini adalah **mengurangi kasus merokok di sekolah**, khususnya di toilet, dengan cara:
- Mendeteksi aktivitas merokok secara otomatis.
- Memberikan respons cepat seperti mengunci pintu toilet untuk mencegah pelaku kabur.
- Memberikan efek jera kepada pelanggar aturan KTR.

---

**Manfaat Penelitian**

1. **Mendukung Program Pemerintah**: Alat ini mendukung program pemerintah dalam menciptakan Kawasan Tanpa Rokok di satuan pendidikan.
2. **Meningkatkan Disiplin Siswa**: Dengan adanya alat ini, diharapkan siswa lebih disiplin dan tidak melanggar aturan merokok di sekolah.
3. **Melindungi Kesehatan Siswa**: Mengurangi paparan asap rokok bagi siswa lain, terutama yang menjadi perokok pasif.

---

**Tinjauan Pustaka**

**1. ESP32: Otak dari Sistem**
ESP32 adalah mikrokontroler canggih yang dilengkapi dengan modul Wi-Fi dan Bluetooth. Kemampuannya dalam mengolah data dan terhubung ke internet membuatnya ideal untuk proyek IoT seperti Asmo. Dengan 17 pin GPIO, ESP32 dapat mengontrol berbagai komponen seperti sensor dan aktuator.

**2. Sensor MQ2: Detektor Asap**
Sensor MQ2 adalah komponen kunci dalam proyek ini. Sensor ini mampu mendeteksi gas yang mudah terbakar, termasuk asap rokok. Sensitivitasnya yang tinggi membuatnya efektif untuk mendeteksi aktivitas merokok di ruang tertutup seperti toilet.

**3. Kunci Pintu Solenoid: Pengunci Otomatis**
Kunci solenoid adalah mekanisme penguncian yang digerakkan oleh elektromagnet. Dalam proyek ini, kunci solenoid digunakan untuk mengunci pintu toilet secara otomatis saat terdeteksi aktivitas merokok.

**4. Relay: Pengontrol Arus Tinggi**
Relay berfungsi sebagai sakelar yang memungkinkan ESP32 mengontrol perangkat bertegangan tinggi seperti kunci solenoid. Dengan relay, ESP32 dapat mengaktifkan atau menonaktifkan kunci solenoid dengan aman.

**5. Catu Daya Step Down 2,5 DC: Penstabil Tegangan**
Modul step-down digunakan untuk menurunkan tegangan dari 12V (dari catu daya eksternal) menjadi 3.3V yang dibutuhkan oleh ESP32. Ini memastikan bahwa semua komponen bekerja dengan tegangan yang sesuai.

---

**Prosedur Pengembangan Alat**

**Desain Sistem**
Kami menggunakan aplikasi **Fritzing** untuk merancang sistem secara visual. Rangkaian ini terdiri dari ESP32 sebagai pusat kendali, sensor MQ2 untuk mendeteksi asap, relay untuk mengontrol kunci solenoid, dan modul step-down untuk menstabilkan tegangan.

**Bahan yang Digunakan**
- **ESP32**: Mikrokontroler utama.
- **Sensor MQ2**: Untuk mendeteksi asap rokok.
- **Kunci Solenoid**: Untuk mengunci pintu toilet.
- **Relay**: Untuk menghubungkan ESP32 dengan kunci solenoid.
- **Catu Daya Step Down**: Untuk menurunkan tegangan dari 12V ke 3.3V.

**Langkah-Langkah Perakitan**
1. **Hubungkan Sensor MQ2 ke ESP32**:
   - VCC sensor ke pin 3.3V ESP32.
   - GND sensor ke GND ESP32.
   - Pin A0 sensor ke pin A0 ESP32.
2. **Hubungkan Relay ke ESP32**:
   - VCC relay ke pin 3.3V ESP32.
   - GND relay ke GND ESP32.
   - Pin IN relay ke pin D1 ESP32.
3. **Hubungkan Kunci Solenoid ke Relay**:
   - NO (Normally Open) relay ke positif solenoid.
   - GND solenoid ke catu daya eksternal.
4. **Pasang Catu Daya Step Down**:
   - Input 12V dari power supply ke modul step-down.
   - Output 3.3V ke ESP32.

**Cara Kerja Alat**
1. Sensor MQ2 mendeteksi asap rokok di toilet.
2. ESP32 menerima sinyal dari sensor dan mengaktifkan relay.
3. Relay mengaktifkan kunci solenoid, mengunci pintu toilet.
4. Sistem mengirim notifikasi ke guru atau staf melalui Wi-Fi.

---

**Kesimpulan**

Asmo adalah solusi inovatif untuk mengatasi masalah merokok di sekolah, terutama di toilet. Dengan menggabungkan teknologi IoT dan komponen elektronik yang terjangkau, alat ini dapat mendeteksi dan mencegah aktivitas merokok secara efektif. Kami berharap alat ini dapat membantu menciptakan lingkungan sekolah yang lebih sehat dan tertib, serta mendukung program pemerintah dalam menciptakan Kawasan Tanpa Rokok.

---

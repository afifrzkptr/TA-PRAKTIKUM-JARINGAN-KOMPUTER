# TA-PRAKTIKUM-JARINGAN-KOMPUTER
Repository ini dibuat sebagai bukti pengumpulan untuk perngerjaan TA pada mata kuliah Praktikum Jaringan Komputer

# TA Percobaan  2: Build a Switch and Router Network
<img width="734" height="202" alt="image" src="https://github.com/user-attachments/assets/e097eec9-26a2-4236-8b5c-fb00d9560fec" />

# 📝 Analisis Hasil Ping Jaringan

Hasil percobaan *ping* dari Lab Jaringan menunjukkan pentingnya konfigurasi **Default Gateway** pada perangkat *end-device* untuk memungkinkan komunikasi antar jaringan (dirutekan oleh *Router*).

| Skenario Ping | Hasil | Penjelasan Singkat |
| :--- | :--- | :--- |
| **PC A** ke **PC B** | **Gagal/Error** | Kedua PC berada di **subnet berbeda** (PC A: 192.168.1.x; PC B: 192.168.0.x). Jika salah satu PC (misalnya PC B) **belum diberikan Default Gateway (192.168.0.1)** atau **memiliki Default Gateway yang salah (misalnya 192.168.1.2)**, *traffic* tidak tahu harus dikirim ke mana di luar jaringan lokalnya, sehingga *ping* gagal. |
<img width="642" height="125" alt="image" src="https://github.com/user-attachments/assets/20edc632-bfbb-41ec-aefb-d39e22bccf9a" />

| **PC A** ke **Default Gateway** Router (192.168.1.1) | **Berhasil** | *Ping* berhasil karena **192.168.1.1** adalah alamat *interface* Router R1 yang terhubung langsung ke subnet PC A. Ini membuktikan koneksi lokal PC A ke *Router* sudah benar. |
<img width="697" height="327" alt="image" src="https://github.com/user-attachments/assets/5247bb74-fe8b-4021-b2c5-5b149e3b226a" />


* **Tautan Video YouTube: https://youtu.be/szYmo5HQtBo

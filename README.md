# TA-PRAKTIKUM-JARINGAN-KOMPUTER
Repository ini dibuat sebagai bukti pengumpulan untuk perngerjaan TA pada mata kuliah Praktikum Jaringan Komputer

# ❗TA Percobaan  3: VLAN❗
<img width="572" height="320" alt="image" src="https://github.com/user-attachments/assets/3ea6b2d2-4673-40d7-a0d2-849f330214c0" />

    "1. Tambahkan PC baru (mis. PC-C) ke workspace dan hubungkan ke Switch S1 menggunakan kabel straight-through (port: Fa0/11).",
    "2. Masuk ke CLI Switch S1 dan konfigurasikan port:\n"
    "   enable\n   configure terminal\n   interface fa0/11\n   switchport mode access\n   switchport access vlan 10\n   end",
    "3. Atur IP Address di PC-C (Desktop → IP Configuration):\n"
    "   IP Address: 192.168.10.5\n   Subnet Mask: 255.255.255.0",
    "4. Verifikasi VLAN di Switch:\n   show vlan brief",
    "5. Tes koneksi dari PC-C ke PC lain di VLAN 10:\n   ping 192.168.10.3"
* Tautan Video YouTube TA Percobaan 3: https://youtu.be/ZB0ViQE5ZTo
    


# ❗TA Percobaan  2: Build a Switch and Router Network❗
<img width="734" height="202" alt="image" src="https://github.com/user-attachments/assets/e097eec9-26a2-4236-8b5c-fb00d9560fec" />

# 📝 Analisis Hasil Ping Jaringan

Hasil percobaan *ping* dari Lab Jaringan menunjukkan pentingnya konfigurasi **Default Gateway** pada perangkat *end-device* untuk memungkinkan komunikasi antar jaringan (dirutekan oleh *Router*).

| Skenario Ping | Hasil | Penjelasan Singkat |
| :--- | :--- | :--- |
| **PC A** ke **PC B** | **Gagal/Error** | Kedua PC berada di **subnet berbeda** (PC A: 192.168.1.x; PC B: 192.168.0.x). Jika salah satu PC (misalnya PC B) **belum diberikan Default Gateway (192.168.0.1)** atau **memiliki Default Gateway yang salah (misalnya 192.168.1.2)**, *traffic* tidak tahu harus dikirim ke mana di luar jaringan lokalnya, sehingga *ping* gagal. |

<img width="642" height="125" alt="image" src="https://github.com/user-attachments/assets/20edc632-bfbb-41ec-aefb-d39e22bccf9a" />

| Skenario Ping | Hasil | Penjelasan Singkat |
| :--- | :--- | :--- |
| **PC A** ke **Default Gateway** Router (192.168.1.1) | **Berhasil** | *Ping* berhasil karena **192.168.1.1** adalah alamat *interface* Router R1 yang terhubung langsung ke subnet PC A. Ini membuktikan koneksi lokal PC A ke *Router* sudah benar. |

<img width="697" height="327" alt="image" src="https://github.com/user-attachments/assets/5247bb74-fe8b-4021-b2c5-5b149e3b226a" />

* Tautan Video YouTube TA Percobaan 2: https://youtu.be/szYmo5HQtBo

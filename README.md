# 🏎️ Karting Deng

![Unity](https://img.shields.io/badge/Unity-2021.3%2B-black?style=flat&logo=unity)
![Language](https://img.shields.io/badge/Language-C%23-blue?style=flat&logo=csharp)
![Status](https://img.shields.io/badge/Status-Prototype-orange)

---

## 1. Executive Summary

### 1.1 Konsep Game
**Karting Deng** adalah sebuah game balap arcade *fast-paced* yang dikembangkan menggunakan **Unity Engine**. Proyek ini merupakan kustomisasi dan pengembangan lebih lanjut dari *Unity Karting Microgame*, menampilkan desain sirkuit orisinil (custom map), visual low-poly yang unik, dan implementasi logika AI berbasis checkpoint.

### 1.2 Target Audiens
* Penggemar game balap kasual (seperti Mario Kart atau Crash Team Racing).
* Pengguna yang menyukai estetika visual *Synthwave/Vaporwave*.
* Developer/Pelajar yang ingin mempelajari implementasi AI Pathfinding di Unity.

### 1.3 Unique Selling Points (USP)
* **Custom Track Design**: Sirkuit tidak menggunakan template, melainkan dibangun manual (*hand-crafted*) dengan rute yang menantang.
* **Dual-Environment**: Menampilkan dua biome berbeda (Kota Neon & Gurun Tandus).
* **Checkpoint AI System**: Lawan menggunakan sistem navigasi berbasis checkpoint yang dinamis, bukan sekadar *waypoints* statis.

---

## 📸 Galeri / Screenshot

| Main Menu | Gameplay |
| :---: | :---: |
| <img width="958" height="538" alt="image" src="https://github.com/user-attachments/assets/7a9b4c02-5358-412f-a88c-908c4d3b6a84" /> | <img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/84a9fcc9-7807-4648-b765-e2d91cb3d401" /> |

| Map Overview | Environment |
| :---: | :---: |
| <img width="686" height="526" alt="image" src="https://github.com/user-attachments/assets/dd4ca139-f0d6-4c7b-b9b4-676456dbb432" /> | <img width="1036" height="533" alt="image" src="https://github.com/user-attachments/assets/b6d6f081-ff8c-483b-a083-bc5075a94b81" /> |

> *Visual game menampilkan estetika low-poly dengan pencahayaan bergaya synthwave/sunset.*

---

## 2. Gameplay Mechanics

### 2.1 Core Loop (Alur Utama)
1.  **Main Menu**: Pemain memilih opsi "Play".
2.  **Level Select**: Pemain memilih satu dari dua sirkuit yang tersedia (City atau Desert).
3.  **Race**: Balapan dimulai. Pemain harus menyelesaikan jumlah lap yang ditentukan (Default: 1 Lap) lebih cepat dari AI.
4.  **Win/Loss**:
    * **Menang**: Pemain menyentuh garis finis urutan pertama.
    * **Kalah**: AI menyentuh garis finis sebelum pemain.

### 2.2 Kontrol (Input)
Game menggunakan skema kontrol Keyboard standar:

| Tombol | Aksi |
| :---: | :--- |
| **W / ↑** | Akselerasi (Gas) |
| **S / ↓** | Rem / Mundur |
| **A / ←** | Belok Kiri |
| **D / →** | Belok Kanan |
| **Tab** | Menu Pause |

### 2.3 Mekanisme AI (Kecerdasan Buatan)
* **Navigasi**: AI menggunakan *Unity NavMesh Agent* yang dimodifikasi.
* **Targeting**: AI tidak langsung menuju garis finis. Mereka diprogram untuk mengejar serangkaian *Invisible Collider Checkpoints* yang disebar di lintasan. Hal ini memungkinkan AI menavigasi tikungan tajam dan rute kompleks buatan tangan (custom map) dengan mulus.

---

## 3. Game World & Level Design

Game ini memiliki dua level utama dengan karakteristik visual dan tantangan yang berbeda.

### 3.1 Map 1: Neon City (Kota)
* **Tema Visual**: Perkotaan futuristik saat matahari terbenam (*Sunset*). Didominasi warna ungu, pink, dan oranye.
* **Karakteristik Trek**:
    * Jalan aspal mulus.
    * Tikungan 90 derajat yang tajam (membutuhkan *drift*).
    * Terdapat jembatan layang (*overpass*) dan terowongan gedung.
    * Rintangan berupa trotoar dan bangunan tinggi.

### 3.2 Map 2: Desert Canyon (Gurun)
* **Tema Visual**: Gurun tandus dengan tebing batu merah dan langit biru cerah/terik.
* **Karakteristik Trek**:
    * Jalan berdebu dan sedikit licin.
    * Kontur tanah yang tidak rata (naik-turun).
    * Lintasan lebih lebar namun minim pembatas jalan (risiko terlempar keluar jalur).
    * Pemandangan piramida dan kaktus sebagai *landmark*.

---

## 4. Technical Specifications

### 4.1 Tools & Aset
* **Game Engine**: Unity 2021.3 LTS (atau lebih baru).
* **Bahasa**: C# Scripting.
* **3D Models**: Modifikasi dari *Unity Karting Microgame* + Aset *Low Poly Environment* tambahan.
* **Physics**: Unity Rigidbody Physics untuk pergerakan kendaraan.

### 4.2 Struktur Scene
Proyek menggunakan arsitektur *Multi-Scene*:
1.  `IntroMenu`: Scene khusus untuk UI dan pemilihan level.
2.  `Map_City`: Scene gameplay untuk trek kota.
3.  `Map_Desert`: Scene gameplay untuk trek gurun.
4.  Data lap dan pemilihan level dikirim antar scene menggunakan `PlayerPrefs`.

---

## 6. Future Roadmap (Rencana Pengembangan)
* [ ] Menambahkan sistem *Power-ups* (Boost, Trap).
* [ ] Menambahkan variasi Karakter/Mobil dengan statistik berbeda.
* [ ] Implementasi *Local Multiplayer* (Split-screen).
* [ ] Leaderboard waktu tercepat (High Score).

---

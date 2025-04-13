# 🐦 Flappy Bird (Java Version)

## 📌 Deskripsi
Proyek ini adalah implementasi sederhana game **Flappy Bird** menggunakan **Java Swing**. Pemain mengontrol seekor burung untuk terbang melewati celah antar pipa tanpa menabrak. Skor bertambah setiap kali pemain berhasil melewati satu set pipa.

## 📐 Desain Program

### Struktur Kelas
- **`App.java`**: Entry point program. Membuka JFrame dan menambahkan panel game `FlappyBird`.
- **`FlappyBird.java`**: Panel utama game. Mengatur logika permainan, render grafis, pergerakan objek, tabrakan, dan skor.
- **`Player.java`**: Menyimpan informasi dan perilaku objek burung.
- **`Pipe.java`**: Menyimpan informasi dan perilaku objek pipa.

### Komponen Grafis
- Gambar latar (`background.png`)
- Gambar burung (`bird.png`)
- Gambar pipa atas dan bawah (`upperPipe.png`, `lowerPipe.png`)

> Semua gambar disimpan di folder `assets/` dan diakses melalui `getResource()`.

## 🔄 Alur Program

### 1. Inisialisasi
Saat program dijalankan melalui `App.java`, frame dibuat dan objek `FlappyBird` ditambahkan sebagai panel utama.

### 2. Gameplay Loop
`Timer` memicu method `actionPerformed()` sebanyak ~60 FPS:
- Memanggil `move()` untuk memperbarui posisi burung dan pipa
- Memanggil `repaint()` untuk menggambar ulang panel

### 3. Kontrol Pemain
- Tombol **Spasi (SPACE)**: Burung meloncat ke atas
- Tombol **R**: Mereset permainan saat game over

### 4. Skoring
- Skor bertambah **+1 setiap kali burung melewati pipa atas**
- Skor ditampilkan menggunakan `JLabel` di pojok kiri atas

### 5. Game Over
- Terjadi jika:
  - Burung menabrak pipa
  - Burung jatuh ke bawah layar
- Pesan **“Game Over”** ditampilkan di tengah layar

## 🖥️ Dokumentasi Program Saat Dijalankan

### Tampilan Awal:
- Latar belakang dan burung muncul
- Pipa akan muncul secara berkala

### Saat Bermain:
- Burung terbang dengan menekan spasi
- Setiap kali melewati celah pipa, skor bertambah

### Saat Game Over:
- Burung berhenti bergerak
- Teks “Game Over” muncul di tengah layar
- Tekan **R** untuk memulai ulang

## 🗂️ Struktur Folder Disarankan

```
FlappyBirdGame/
├── src/
│   ├── App.java
│   ├── FlappyBird.java
│   ├── Pipe.java
│   ├── Player.java
├── assets/
│   ├── background.png
│   ├── bird.png
│   ├── lowerPipe.png
│   ├── upperPipe.png
```

## 🚀 Cara Menjalankan

1. Pastikan semua file `.java` dan folder `assets/` sudah berada di direktori proyek.
2. Compile dan jalankan `App.java` dari IDE atau terminal.
3. Nikmati permainan dan pecahkan skor tertinggi!
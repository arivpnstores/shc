
# 🔐 Script Encrypt Premium (Bash Obfuscator & SHC)

Script ini digunakan untuk **mengamankan file shell script (.sh)** dengan metode:
- **Obfuscate Bash**
- **Compile SHC**
- **Combine Obfuscate + SHC**

Dilengkapi dengan **sistem lisensi offline** (password sekali input, auto save).

---

## ✨ Fitur Utama
- 🔑 **Lisensi Offline**
  - User input password **1x saja**
  - Lisensi disimpan otomatis
  - Run berikutnya **tidak perlu input ulang**
- 🔒 **Proteksi Script**
  - Obfuscate bash (`bash-obfuscate`)
  - Compile ke binary (`shc`)
  - Combine (lebih sulit dibaca & dibongkar)
- 🗑️ **Auto hapus file asli**
  - File `.sh` asli dihapus setelah sukses diproses
- 📂 **Manajemen Folder Otomatis**
  - Folder input & output dibuat otomatis
- 🧩 **Full CLI (tanpa bot Telegram, tanpa internet runtime)**

---

## 📁 Struktur Folder
```

/root/shc/
├── script1.sh
├── script2.sh
└── obfuscated/
├── script1.sh
└── script2.sh

````

---

## 🛠️ Dependensi
Script akan otomatis meng-install jika belum ada:
- `curl`
- `git`
- `build-essential`
- `dos2unix`
- `zip`
- `coreutils`
- `gcc`
- `make`

Tambahan sesuai metode:
- **bash-obfuscate** → butuh Node.js (via NVM)
- **shc** → compile dari source

---

## 🚀 Cara Pakai

### 1️⃣ Jalankan Script
```bash
wget -q https://raw.githubusercontent.com/arivpnstores/shc/main//menuenc -O /usr/local/bin/menuenc && chmod +x /usr/local/bin/menuenc && menuenc
````

### 2️⃣ Masukkan Password Lisensi

* Hanya diminta **satu kali**
* Disimpan di:

```
/etc/.encrypt_license
```

### 3️⃣ Siapkan File

Upload semua file `.sh` ke:

```
/root/shc
```

### 4️⃣ Pilih Metode

```
1) bash-obfuscate
2) SHC + GNU compile (portable)
3) Combine (bash-obfuscate + SHC)
```

### 5️⃣ Proses Berjalan

* File terenkripsi akan masuk ke:

```
/root/shc/obfuscated
```

* File `.sh` asli **dihapus otomatis**

---

## 🔐 Sistem Lisensi

* Lisensi **offline**
* Disimpan secara lokal
* Permission file:

```
chmod 600 /etc/.encrypt_license
```

Contoh konfigurasi di script:

```bash
ALLOWED_KEYS=("Ari123Ok")
```

---

## ⚠️ Catatan Penting

* Jalankan sebagai **root**
* Pastikan file `.sh` sudah benar sebelum proses
* File asli akan **dihapus permanen**
* Untuk keamanan maksimal, gunakan **Combine (3)**

---

## 🧪 Distro Tested

* Debian 11 / 12
* Ubuntu 20.04 / 22.04

---

## 📌 Tips Keamanan Tambahan

* Compile hasil akhir dengan `strip`
* Jalankan di VPS build khusus
* Backup file `.sh` sebelum diproses

---

## 🧑‍💻 Author
ORDER PASSWORD : https;//t.me/ARI_VPN_STORE


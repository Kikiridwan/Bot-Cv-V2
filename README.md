# Telegram Bot Node.js

Bot Converter File Telegram ini berbasis **Node.js** menggunakan **node-telegram-bot-api** dengan sistem **plugin modular**, manajemen role, logging, dan validasi terenkripsi sebelum bot dijalankan.

---

## Fitur

Bot menggunakan sistem **plugin modular**, berikut daftar plugin yang tersedia:

### Owner
- `owner-setrole.js` → Mengatur role pengguna (user, VIP, owner).

### User
- `user-me.js` → Menampilkan info pengguna.
- `user-start.js` → Memulai interaksi dengan bot (/start).
- `user-stats.js` → Menampilkan statistik pengguna.

### VIP
- `vip-bagilanjutan.js` → Membagi file lanjutan.
- `vip-bagivcf.js` → Membagi file VCF.
- `vip-cekkontak.js` → Mengecek kontak.
- `vip-createadmin.js` → Membuat admin baru.
- `vip-gabungtxt.js` → Menggabungkan file TXT.
- `vip-gabungvcf.js` → Menggabungkan file VCF.
- `vip-msgtotxt.js` → Mengubah pesan menjadi TXT.
- `vip-potonglanjutan.js` → Memotong file lanjutan.
- `vip-potongvcf.js` → Memotong file VCF.
- `vip-txttovcf.js` → Mengubah file TXT menjadi VCF.
- `vip-vcftotxt.js` → Mengubah file VCF menjadi TXT.

---

# Struktur Folder Bot

```
├─ .env
├─ .gitignore
├─ commands              # Folder command bot
│  ├─ owner-setrole.js
│  ├─ user-me.js
│  ├─ user-start.js
│  ├─ user-stats.js
│  ├─ vip-bagilanjutan.js
│  ├─ vip-bagivcf.js
│  ├─ vip-cekkontak.js
│  ├─ vip-createadmin.js
│  ├─ vip-gabungtxt.js
│  ├─ vip-gabungvcf.js
│  ├─ vip-msgtotxt.js
│  ├─ vip-potonglanjutan.js
│  ├─ vip-potongvcf.js
│  ├─ vip-txttovcf.js
│  └─ vip-vcftotxt.js
├─ config.js             # Konfigurasi 
├─ database.json         # Database user
├─ index.js              # Entry point utama bot
├─ main.js               # Setup dan validasi
├─ package-lock.json
└─ package.json
```

---

## Instalasi

1. Clone repository:
```
$ git clone https://github.com/syawaloktasyahputra/BOT-CV
$ cd BOT-CV
```

2. Install dependencies:
```
$ npm install
```

3. Create file config.js in root:
```
export default {
  token: "YOUR_TELEGRAM_BOT_TOKEN",
  owner: [123456789], // ID Telegram owner
};
```

4. Run the bot
```
npm start
```

## DATABASE STRUCTURE
```
{
  "123456789": {
    "id": 123456789,
    "username": "user123",
    "first_name": "User",
    "last_name": "Example",
    "role": "user",
    "role_expire": 0
  }
}
```
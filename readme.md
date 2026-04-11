# 📘 Product Requirements Document (PRD)

## Website Al-Qur'an (Vue.js + .NET)

---

## 1. 📌 Overview

Website Al-Qur'an adalah platform berbasis web yang memungkinkan pengguna membaca, mencari, dan memahami Al-Qur'an secara digital. Aplikasi ini dibangun menggunakan:

* **Frontend:** Vue.js
* **Backend:** .NET (Web API)
* **Hosting:** Platform gratis (contoh: Vercel, Netlify, atau Azure Free Tier)

---

## 2. 🎯 Objectives

### Tujuan Utama:

* Menyediakan akses mudah untuk membaca Al-Qur'an secara online
* Menyediakan fitur pencarian ayat dan surat
* Menyediakan terjemahan dan tafsir sederhana
* Responsif dan ringan untuk semua perangkat

### Success Metrics:

* Waktu loading < 3 detik
* Minimal 100 pengguna aktif/bulan
* Bounce rate < 50%

---

## 3. 👥 Target Users

* Muslim umum (pelajar, pekerja, dll)
* Pengguna yang ingin membaca Al-Qur'an secara digital
* Pengguna yang ingin mencari ayat tertentu dengan cepat

---

## 4. 🧩 Features & Requirements

### 4.1 Core Features

#### 📖 1. Baca Al-Qur'an

* Menampilkan daftar surat (114 surat)
* Menampilkan ayat per surat
* Navigasi antar surat dan ayat

#### 🔍 2. Pencarian Ayat

* Cari berdasarkan:

  * Kata kunci
  * Nomor surat & ayat
* Highlight hasil pencarian

#### 🌐 3. Terjemahan

* Bahasa Indonesia
* Toggle tampil/sembunyi terjemahan

#### 📚 4. Tafsir (Opsional MVP+)

* Tafsir singkat per ayat
* Expand/collapse view

#### 🔊 5. Audio (Optional)

* Play audio per ayat
* Streaming ringan

---

### 4.2 Additional Features (Future)

* Bookmark ayat
* Mode gelap (dark mode)
* Riwayat bacaan terakhir
* Multi-language

---

## 5. 🧱 Technical Architecture

### 5.1 Frontend (Vue.js)

* Framework: Vue 3 + Composition API
* Routing: Vue Router
* State Management: Pinia / Vuex
* UI: Tailwind CSS / Vuetify

### 5.2 Backend (.NET)

* Framework: ASP.NET Core Web API
* Database:

  * SQLite (untuk hosting gratis & ringan)
* API Endpoints:

  * `/surah`
  * `/surah/{id}`
  * `/search?q=`
  * `/ayah/{id}`

### 5.3 Data Source

* Dataset Al-Qur'an (JSON / API publik seperti:

  * https://api.quran.com
  * https://alquran.cloud)

---

## 6. ☁️ Hosting Strategy (Free)

### Frontend Hosting:

* Vercel / Netlify

### Backend Hosting:

* Railway / Render / Azure Free Tier

### Database:

* SQLite (embedded)
* atau PostgreSQL (free tier jika perlu)

---

## 7. 🔄 User Flow

1. User membuka website
2. Melihat daftar surat
3. Memilih surat
4. Membaca ayat + terjemahan
5. (Opsional) menggunakan search untuk mencari ayat tertentu

---

## 8. 🧪 Non-Functional Requirements

* ⚡ Performance: cepat dan ringan
* 📱 Responsive: mobile-friendly
* 🔒 Security: sanitasi input search
* 🌍 Accessibility: readable font arab & latin

---

## 9. 🎨 UI/UX Guidelines

* Font Arab jelas (contoh: Amiri, Scheherazade)
* Layout clean & minimal
* Dark mode optional
* Highlight ayat aktif

---

## 10. 🚧 Development Milestones

### Phase 1 (MVP - 2 minggu)

* Setup project (Vue + .NET)
* API basic (list surah & ayat)
* UI baca Al-Qur'an

### Phase 2 (1-2 minggu)

* Search feature
* Terjemahan
* Deployment ke hosting gratis

### Phase 3 (Future)

* Audio
* Bookmark
* Tafsir

---

## 11. ⚠️ Risks & Mitigation

| Risk               | Mitigation                     |
| ------------------ | ------------------------------ |
| Hosting free limit | Gunakan caching & optimasi API |
| Data besar         | Lazy loading ayat              |
| Performance lambat | CDN & optimize assets          |

---

## 12. 📦 Deployment Plan

1. Push code ke GitHub
2. Deploy frontend ke Vercel/Netlify
3. Deploy backend ke Render/Azure
4. Integrasikan API endpoint
5. Testing end-to-end

---

## 13. 📎 Appendix

### Suggested Folder Structure

```
/frontend (Vue)
  /components
  /views
  /services

/backend (.NET)
  /Controllers
  /Models
  /Services
```

---

## 14. ✅ Conclusion

Project ini bertujuan membuat platform Al-Qur'an digital yang sederhana, cepat, dan mudah diakses. Dengan stack Vue.js dan .NET, serta deployment di layanan gratis, project ini cocok sebagai:

* Portfolio project
* Produk edukasi
* Aplikasi ibadah digital

---

**End of PRD**

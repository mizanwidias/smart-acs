# ⚡ Smart-ACS — Next Generation GenieACS Override Platform 🚀

> **Empowering Network Intelligence Beyond TR-069**

Smart-ACS adalah versi _re-engineered_ dari **GenieACS**, dirancang untuk menjadi _All-in-One Network Automation Platform_ yang tidak hanya melakukan provisioning, tetapi juga **melakukan observasi, analisis, dan otomasi tingkat lanjut** terhadap perangkat CPE (Customer Premises Equipment).

---

## 🧠 Konsep Utama

Smart-ACS bukan sekadar ACS biasa.  
Ia adalah **jembatan antara TR-069, event stream processing, dan real-time insight**.

### ✨ Fitur Unggulan
| Fitur | Deskripsi |
|:------|:-----------|
| ⚙️ **One Click Provisioning** | CPE baru langsung dikonfigurasi otomatis tanpa login manual |
| 📡 **Real-Time Monitoring** | Tracking status perangkat aktif, trafik, dan parameter penting |
| 🚨 **Smart Alerting Engine** | Terintegrasi dengan **Kafka** & **Telegram Bot** untuk notifikasi langsung ke engineer |
| 🧩 **Event-driven Architecture** | Semua perubahan CPE, log error, atau disconnect dikirim ke event bus (Kafka) |
| 🧠 **AI/Anomaly Detection (Planned)** | Mendeteksi perilaku abnormal pada perangkat jaringan |
| 🌐 **Topology Visualization** | Dashboard interaktif untuk melihat hubungan antar perangkat |
| 📊 **Custom Dashboard** | Statistik performa jaringan dengan grafis real-time menggunakan chart library modern |

---

## 🏗️ Arsitektur Sistem (Developer View)



               ┌───────────────────────────────┐
               │         Web Dashboard          │
               │  (Next.js / React + Tailwind)  │
               └──────────────┬────────────────┘
                              │
                              ▼
                 ┌────────────────────────┐
                 │  Smart-ACS Core (API)  │
                 │  Node.js / Express.js  │
                 └────────────┬───────────┘
                              │
                              ▼
                ┌────────────────────────────┐
                │        Apache Kafka        │
                │  (Event & Alert Streamer)  │
                └────────────┬───────────────┘
                              │
            ┌─────────────────┴──────────────────┐
            │                                    │
            ▼                                    ▼
  ┌────────────────────┐             ┌──────────────────────┐
  │   GenieACS Engine  │             │   Alert Processor     │
  │   (TR-069 Server)  │             │ (Telegram, Email, etc)│
  └─────────┬──────────┘             └────────────┬─────────┘
            │                                     │
            ▼                                     ▼
    ┌──────────────┐                     ┌──────────────────┐
    │   MongoDB    │                     │   InfluxDB (opt) │
    │ CPE Metadata │                     │  Time-Series Data│
    └──────────────┘                     └──────────────────┘


---

## ⚙️ Setup & Installation

1️⃣ Clone Repo
```bash
git clone https://github.com/mizanwidias/smart-acs.git
cd smart-acs

2️⃣ Jalankan Infrastruktur
cd infra
docker-compose up -d






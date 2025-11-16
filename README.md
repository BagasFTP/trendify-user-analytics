# Trendify -- User Behavior & Feature Usage Analytics

### Power BI • Python • E-Commerce Analytics • Funnel • Retention • Cohort

Project ini menganalisis perilaku pengguna pada aplikasi e-commerce
**Trendify** menggunakan kombinasi **Python (pandas)** untuk data
preparation & EDA, serta **Power BI** untuk dashboard final, funnel
analysis, dan retention cohort.

------------------------------------------------------------------------

## 📌 1. Latar Belakang

Trendify sebagai aplikasi e-commerce baru menghadapi beberapa masalah
setelah 3 bulan rilis:

-   Checkout completion rendah\
-   Banyak user AddToCart namun tidak sampai pembayaran\
-   Fitur tertentu jarang digunakan\
-   Retention rendah (churn tinggi)\
-   Tidak ada dashboard monitoring analytics

Project ini dibuat untuk memberikan **insight berbasis data** dan
**dashboard profesional** bagi klien.

------------------------------------------------------------------------

## 🎯 2. Tujuan Project

1.  Menganalisis perilaku pengguna\
2.  Mengetahui fitur yang paling/kurang dipakai\
3.  Menganalisis checkout funnel & titik drop-off\
4.  Menghitung retensi user (D1, D7, D30)\
5.  Membuat dashboard Power BI lengkap\
6.  Memberikan rekomendasi untuk meningkatkan conversion & retention

------------------------------------------------------------------------

## 👥 3. Pembagian Tugas (3 Orang)

### 👤 Peran 1 -- Data Cleaning & Preparation (Ferdi)

-   Cleaning dataset\
-   Handling missing value & duplicate\
-   Normalisasi event\
-   Ekstraksi timestamp\
-   Output: `event_log_trendify_clean.csv`

### 👤 Peran 2 -- Exploratory Data Analyst (Hardy)

-   DAU/WAU/MAU\
-   Feature usage\
-   Device usage\
-   Heatmap (Day vs Hour)\
-   Insight EDA\
-   Output: `EDA_APP.ipynb`, `READMEeda.md`

### 👤 Peran 3 -- Funnel, Retention & Dashboard Developer (Bagas)

*(Funnel & retention dibuat langsung di Power BI)*\
- Checkout funnel: conversion & drop-off\
- Funnel per device\
- Funnel per kategori\
- Retention analysis (D1/D7/D30)\
- Cohort table\
- Dashboard Power BI final\
- Output: Dashboard PBIX + screenshot pages

------------------------------------------------------------------------

## 🗂 4. Struktur Folder

``` bash
Trendify-User-Analytics/
│
├── data/
│   ├── event_log_trendify_50k.csv           
│   ├── event_log_trendify_clean.csv          
│
├── notebooks/
│   ├── EDA_APP.ipynb                      
│   ├── 01_data_cleaning.ipynb (optional)   
│
├── analysis/
│   ├── READMEeda.md                          
│   ├── funnel_retention_notes.md (optional)  
│
├── dashboard/
│   ├── Trendify-User-Behavior-Analytics-Dashboard.pbix
│   ├── Overview.png
│   ├── Feature Usage.png
│   ├── Funnel.png
│   ├── Device-based Funnel.png
│   ├── Retention & Cohort.png
│
└── README.md
```

------------------------------------------------------------------------

## 📊 5. Ringkasan Dashboard Power BI

Dashboard terdiri dari **5 halaman utama**, lengkap dengan visualisasi interaktif untuk menganalisis perilaku user Trendify.

---

### **1. Overview – User & Traffic Summary**

![Overview](dashboard/Overview.png)

Menampilkan:
- Total Unique Users  
- DAU / WAU / MAU  
- Event Volume  
- Device Distribution  
- Daily Traffic Trends  

---

### **2. Feature Usage Dashboard**

![Feature Usage](dashboard/Feature%20Usage.png)

Menampilkan:
- Event volume per fitur  
- Penggunaan fitur per device  
- Heatmap aktivitas (Day vs Hour)  

---

### **3. Checkout Funnel**

![Funnel](dashboard/Funnel.png)

Alur utama:  
`view_product → app_open → add_to_cart → start_checkout → payment_success`

Dashboard ini menampilkan:
- Conversion rate tiap tahap  
- Drop-off terbesar  
- Perbandingan funnel per kategori  
- Funnel berdasarkan device  

---

### **4. Device-Based Funnel**

![Device Funnel](dashboard/Device-based%20Funnel.png)

Menampilkan:
- Funnel Android  
- Funnel iOS  
- Funnel Web  
- Perbandingan conversion rate antar device  

---

### **5. Retention & Cohort Dashboard**

![Retention](dashboard/Retention%20&%20Cohort.png)

Menampilkan:
- Retention D1 / D7 / D30  
- Tabel cohort berdasarkan first_seen_date  
- Retention dynamic per device  


------------------------------------------------------------------------

## 🧠 6. Insight Utama

### 🔥 A. User Behavior

-   5.000 total unique users\
-   DAU stabil di **450--500 user/hari**\
-   Device distribution:
    -   Android: **38.8%**
    -   iOS: **36.9%**
    -   Web: **24.3%**
-   Peak time: **18:00--22:00**, terutama Friday & Sunday

------------------------------------------------------------------------

### 🔥 B. Feature Usage

Fitur paling sering dipakai: - view_product (\~10K) - app_open (\~9K) -
view_home (\~8K)

Fitur paling jarang: - payment_success (\~2K) - logout (\~1K)

→ banyak user **sekedar lihat produk** tanpa menyelesaikan transaksi.

------------------------------------------------------------------------

### 🔥 C. Checkout Funnel Analysis

Funnel (All Devices): - ViewProduct: 10K\
- AppOpen: 9K\
- AddToCart: 6K\
- StartCheckout: 5K\
- PaymentSuccess: 2K

Drop-off terbesar: - **StartCheckout → PaymentSuccess (60%)**

Conversion keseluruhan: - **26.8%**

------------------------------------------------------------------------

### 🔥 D. Device Conversion

-   Android: **27%**
-   iOS: **27%**
-   Web: **28%** (tapi volume event kecil)

→ Website memiliki engagement & conversion terendah.

------------------------------------------------------------------------

### 🔥 E. Retention & Cohort

-   D1 Retention = **11%**
-   D7 Retention = **10%**
-   D30 Retention = **10%**

Retention stagnan → engagement perlu ditingkatkan.

------------------------------------------------------------------------

## 👥 7. Contributors & Roles

  | Nama                        | Role                                               | Tanggung Jawab                                                                                                       |
| --------------------------- | -------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| **Hardy Gustino**           | **Exploratory Data Analyst (EDA & Feature Usage)** | Analisis DAU/WAU, feature usage, device analysis, heatmap, dan insight awal dari data.                               |
| **Bagas Firdaus Tri Putra** | **Funnel, Retention & Dashboard Developer**        | Checkout funnel, conversion analysis, retention & cohort analysis, desain dashboard Power BI, dan dokumentasi akhir. |
| **Ferdi Endahas**           | **Data Engineer & Data Cleaning**                  | Membersihkan data, menangani missing/duplicate, normalisasi event, dan menyiapkan dataset siap analisis.             |

------------------------------------------------------------------------

## 🛠 8. Tools yang Digunakan

-   Python (pandas, numpy, matplotlib)
-   Jupyter Notebook
-   Power BI Desktop
-   DAX
-   VS Code

------------------------------------------------------------------------

## ▶️ 9. Cara Menjalankan Project

1.  Clone repository:\

``` bash
git clone https://github.com/BagasFTP/trendify-user-analytics.git
```

2.  Jalankan notebook EDA:\

```{=html}
<!-- -->
```
    notebooks/EDA_APP.ipynb

3.  Buka dashboard Power BI:\

```{=html}
<!-- -->
```
    dashboard/Trendify-User-Behavior-Analytics-Dashboard.pbix

------------------------------------------------------------------------



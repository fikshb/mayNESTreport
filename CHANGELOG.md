# Changelog — NEST Living Board Reports

Catatan revisi deck laporan operasional NEST Living (April & Mei 2026).
Format tanggal: YYYY-MM-DD. Angka revenue: **single Total Revenue**, lingkup **PT Nest Kelola Hunian**, **incl. PPN (gross)** kecuali dinyatakan lain.

---

## 2026-07-05 (Report 03 — Q2 2026 kuartalan)

- Deck baru **`NEST_Living_Slide_Report_Q2_2026.html`** (12 slide) — rollup April–Juni 2026, mengikuti struktur 8-section dokumen sumber `Nest_Living_Q2_2026_Board_Report_Complete.docx`.
- Slide: Cover · Executive Summary · Executive Dashboard (+bar chart revenue) · Revenue Capacity & Growth (+gauge 81%) · Business Transformation Journey (timeline April/Mei/Juni) · Key Achievements · Operational Work Log · Digital Distribution · Financial Impact · Operational Risk Assessment · Strategic Investment Recommendation · Closing.
- **Angka Q2 (dibulatkan, incl. PPN):** Revenue April Rp191jt · Mei Rp233jt · Juni **Rp318jt** (+66,5% dlm 2 bln) · Total Q2 **Rp742jt**. Unit aktif **22→26→28** (+27%). Revenue capacity 49%→59%→**81%** dari potensi maks Rp392jt/bln (sisa peluang Rp74jt). 3 konversi short→long stay.
- **Keputusan data (atas instruksi user):** (1) revenue Juni ditampilkan **total saja** tanpa breakdown stream; (2) **Daya Mitra Rp127,78jt incl. PPN** (bukan Rp115jt yang tertulis di docx) agar konsisten dgn deck April/Mei; (3) Digital Distribution **tanpa embed/link** — hanya note bahwa detail channel ada di Laporan Mei 2026.
- ⚠️ Angka Q2 pakai versi **dibulatkan** dari docx (mis. Mei Rp233jt) — beda dgn deck Mei yang presisi Rp233.361.397. Konsisten internal di deck Q2 saja.
- `index.html`: tambah card **Report 03 — Q2 2026** (label "Latest" pindah dari Mei ke Q2); **koreksi unit aktif Mei 24→26** (card Report 02) agar nyambung dgn dashboard docx.
- **Deploy:** di-commit & push ke `origin/main` (commit `bfb019e`) → auto-deploy Vercel ke https://may-nes-treport.vercel.app/. File `.docx`/`.xlsx` sumber ditambahkan ke `.gitignore` & `.vercelignore` (tidak ikut publish).
- **Open item:** angka unit di dalam deck **Mei** masih "22→24 (+9,1%)" — belum disinkronkan ke 26; menunggu keputusan user.

---

## 2026-06-15 (reframe periode Report Mei → Mei saja)

- Semua label periode **"April–Mei 2026" → "Mei 2026"** di report Mei (cover, title tag, exec intro, KPI sub, Financial Impact, slide marketing/CRM, closing, footer) + card index Report 02.
- Paralel dgn Report 01 yang sudah jadi "April saja". ⚠️ Catatan: label periode di slide marketing (Airbnb/Agoda/Meta/CRM) ikut jadi "Mei 2026" — jika data channel tsebenarnya mencakup 2 bulan, perlu dikonfirmasi terpisah.

---

## 2026-06-15 (infografis Exec Summary Mei)

- Ditambah **"Executive Snapshot"** band di Exec Summary report Mei (di bawah 3 KPI card): (1) momentum revenue April→Mei +21,7%, (2) stacked bar komposisi revenue (hunian 95,6% · telco 3,2% · lelang 1,3%).
- Pure HTML/CSS inline, palette NEST (deep-blue/gold), offline-safe, tanpa dependency chart. Slide aman karena `.slide` sudah `overflow-y:auto`.

---

## 2026-06-15 (revisi Report April + koreksi unit aktif lintas-report)

### Report 01 (April) — revenue single-month & restructure
- Slide revenue diubah dari basis akrual 3-bulan (Feb–Apr, total Rp 384.178.888) menjadi **single-month April**, format "Revenue Detail" seperti report Mei (istilah akrual/unearned dibuang).
- **Total Revenue April = Rp 191.741.881** (operasional Rp 176.191.881 + lelang Arkadia Rp 15.550.000).
  - Stream: hunian & short-stay Rp 168.781.881 + infrastruktur telco Rp 7.410.000 + lelang Rp 15.550.000.
- Exec Summary: card "Revenue Lelang" dilebur jadi satu card **"Total Revenue April" Rp 191.741.881**.
- Report direframe penuh jadi **"April 2026"** (cover, title tag, judul index, insight, closing, footer) — dari sebelumnya "Februari–April" / "Maret–Mei".
- Tanggal lelang Arkadia 11 & 16 Maret **diasumsikan dana masuk April** (atas keputusan user) dan diubah ke April + diurutkan kronologis; total Rp 15.550.000 tidak berubah.

### Koreksi baseline unit aktif (lintas-report)
- Unit aktif **April: 2→8 dikoreksi jadi 16→22** (delta tetap +6 unit; +300% → +37,5%).
- Unit aktif **Mei: 8→10 dikoreksi jadi 22→24** (+25% → +9,1%) agar nyambung dgn April yang ditutup di 22.
- `index.html`: kedua card (Report 01 & 02) disesuaikan.

---

## 2026-06-15 (revisi lanjutan — single Total Revenue)

### Penyederhanaan basis & penyajian revenue
- Istilah **akrual / earned revenue / unearned (amortisasi)** **dihapus seluruhnya** dari deck Mei — diganti bahasa lugas.
- Pemasukan tidak lagi dipecah dua (earned vs total); deck kini menyajikan **satu angka Total Revenue** saja.
- **Total Revenue Mei 2026: Rp 233.361.397** (incl. PPN).

### Komposisi Total Revenue (perhitungan — TIDAK ditampilkan di slide, BOD-friendly)
```
  OTA / short-stay (dilaporkan terpisah, tidak diverifikasi ulang) ...  107.174.823
+ Income Monthly (Finance) .........................................  157.574.074
− Double-count booking (tercatat ganda di OTA & income monthly) ....  (34.350.000)
+ Lelang aset idle (one-off) .......................................    2.962.500
= TOTAL REVENUE ....................................................  233.361.397
```
- **Pendapatan Operasional (bersih) = Rp 230.398.897** (= 107.174.823 + 157.574.074 − 34.350.000); inilah angka yang tampil di slide, dipecah per stream: hunian & short-stay Rp 222.988.897 + infrastruktur telco Rp 7.410.000.

### Detail double-count (Rp 34.350.000 — 10 invoice INV-SC, booking dobel di finance)
| Invoice | Nama | Nominal |
|---|---|---:|
| INV-SC/0526/0005 | Andara Dhimas | 1.100.000 |
| INV-SC/0526/0007 | Maulidan Isbar | 6.300.000 |
| INV-SC/0526/0008 | Anis Mulachela | 6.500.000 |
| INV-SC/0526/0009 | Sidah Husein | 750.000 |
| INV-SC/0526/0012 | Maulidan Isbar | 6.300.000 |
| INV-SC/0526/0015 | Maulidan Isbar | 6.300.000 |
| INV-SC/0526/0019 | David Figueroa Cicaedo | 1.550.000 |
| INV-SC/0526/0020 | Andara Dhimas | 2.200.000 |
| INV-SC/0526/0021 | Andara Dhimas | 2.200.000 |
| INV-SC/0526/0022 | Billy Rayn Pelupessy | 1.150.000 |
| **Total** | | **34.350.000** |

- **PT Cemani Toka** (2 debit note, ~Rp 7 jt/baris) **diabaikan** atas instruksi — tidak dijadikan pengurang maupun penambah; dianggap tidak ada.
- Detail double-count & rekonsiliasi **sengaja tidak dimuat di slide** agar tidak memancing pertanyaan di forum BOD; dicatat di log ini saja sebagai audit trail.
- Sumber data: `Income monthly.xls` + rekap OTA (tidak di-commit — confidential).

---

## 2026-06-15

### Penyesuaian Daya Mitra ke incl. PPN
- Nilai kontrak sewa lahan tower **Daya Mitra** diubah dari **Rp 115.000.000** (DPP, sebelum PPN) menjadi **Rp 127.777.778** (incl. PPN, 2 tahun).
- Konsisten dengan ledger: porsi bulanan Rp 5.324.074 × 24 bulan = Rp 127.777.778.
- Diterapkan di 4 titik (Key Achievements, Financial Impact, slide 2.7 Mei, slide 2.9 April).

### Penanda
- **PPN**: seluruh angka revenue ditandai **incl. PPN (gross)** di KPI Executive Summary, total Financial Impact, dan footnote (revenue bersih ≈ angka ÷ 1,11).
- **OTA**: footnote dipertegas — revenue OTA/short-stay (Airbnb, Agoda) **sudah tercakup sebagian** pada komponen service charge ledger ini.

### Reklasifikasi pendapatan infrastruktur telekomunikasi
- **Daya Mitra** (PT Dayamitra Telekomunikasi) dan **Dhost** (PT Dhost Telekomunikasi) dikoreksi dari "vendor/biaya" menjadi **tenant infrastruktur telco = pendapatan**.
  - Daya Mitra: sewa lahan tower, Rp 5,32 jt/bln.
  - Dhost: in-building antenna (IOH operator), Rp 2,08 jt/bln (Rp 25 jt/tahun).
  - Pendapatan pasif gabungan **Rp 7,41 jt/bln**, kontrak terkunci 2 tahun.
- Slide "Strategic Vendor Partnership" (Mei 2.7) & "Perpanjangan Kontrak Vendor Strategis" (April 2.9) dibingkai ulang jadi "Kontrak Sewa Infrastruktur Telekomunikasi".

### Peralihan ke basis akrual
- Pelaporan revenue dialihkan dari **basis kas (tanggal invoice)** ke **basis akrual (earned revenue)** = Monthly Payment + pelepasan Unearned (amortisasi kontrak prabayar).
- Headline lama "Revenue Mei Rp 107.174.823" (short-stay, definisi tak jelas) dihapus, digantikan earned revenue akrual.
- Angka final:
  - **Earned Revenue Mei 2026: Rp 157.574.074** (Monthly Rp 98.757.407 + Unearned Rp 58.816.667).
  - **Total Revenue Mei 2026: Rp 160.536.574** (earned + lelang aset idle Rp 2.962.500).
  - **Earned Revenue Feb–Apr 2026: Rp 384.178.888** (Feb 125.497.407 + Mar 136.257.407 + Apr 122.424.074).
- Daya Mitra dikeluarkan dari total revenue bulanan (porsi bulanannya sudah masuk earned revenue; nilai kontrak total tidak ditambahkan agar tidak double-count).
- Sumber data: `Income monthly.xls` (tidak di-commit — confidential).

---

## 2026-06-04 (baseline awal repo)
- Penambahan slide **Rental Tenant (Long-Stay)** berbasis kas — *kemudian digantikan basis akrual di atas*.
- Penambahan landing chooser (`index.html`) dan password gate sisi-klien (`NESTLIVING`).
- Deck **April 2026** (Feb–Apr) dan **Mei 2026** (Apr–Mei), masing-masing 20 slide.

---

> **Catatan keamanan:** file data mentah (`List RENTAL TENANT.xls`, `Income monthly.xls`) berisi nama tenant + nominal dan **tidak di-commit** ke repo (lihat `.gitignore`). Password gate bersifat client-side (bukan proteksi keamanan riil) — pastikan repo tetap **private**.

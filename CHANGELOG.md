# Changelog — NEST Living Board Reports

Catatan revisi deck laporan operasional NEST Living (April & Mei 2026).
Format tanggal: YYYY-MM-DD. Angka revenue: basis **akrual (earned revenue)**, lingkup **PT Nest Kelola Hunian**, **incl. PPN (gross)** kecuali dinyatakan lain.

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

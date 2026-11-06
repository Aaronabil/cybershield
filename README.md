# CyberShield — Versi GitHub Pages (Statis)

Versi ini dibuat supaya CyberShield bisa di-hosting di **GitHub Pages**
(`https://aaronabil.github.io/cybershield/`), yang hanya melayani file
statis dan **tidak bisa menjalankan PHP / MySQL**.

## Bedanya dengan versi PHP

| | Versi PHP (pengumpulan tugas) | Versi ini (GitHub Pages) |
|---|---|---|
| File | `index.php` + `api.php` + `db.php` | Satu file `index.html` |
| Penyimpanan | MySQL (`firewall_rules`, `security_logs`, `blacklist_ips`) | `localStorage` browser (skema & data awal sama persis) |
| Cocok untuk | Dinilai dosen sesuai brief (PHP + MySQL) | Demo online lewat link |

Tampilan dan semua fitur **sama**: 4 kartu statistik, tambah/toggle/hapus
aturan firewall, simulasi traffic + 4 serangan, log keamanan, blacklist.
Perbedaannya hanya di mana datanya disimpan: di versi ini data tersimpan
di browser masing-masing pengunjung (buka di browser lain = data awal lagi),
sedangkan versi PHP datanya tersimpan di server dan sama untuk semua orang.

## Cara deploy ke GitHub Pages

1. Buat repo baru di GitHub, misal `cybershield` (public).
2. Upload `index.html` ini ke root repo (atau push lewat git).
3. Repo → **Settings → Pages** → Source: **Deploy from a branch** →
   Branch `main`, folder `/(root)` → **Save**.
4. Tunggu 1–2 menit, buka `https://aaronabil.github.io/cybershield/`

Kalau mau reset data demo ke awal: buka DevTools (F12) → Console →
ketik `localStorage.clear()` lalu refresh.

## Kalau mau hosting versi PHP-nya (bukan GitHub Pages)

Pakai **InfinityFree** (gratis, PHP 8.3/8.4 + MySQL, 5 GB, tanpa kartu):
daftar di infinityfree.com → buat subdomain → upload isi folder
`cybershield/` versi PHP → buat database MySQL → import `database.sql` →
isi kredensial database itu ke `config.php`. Panduan lengkap ada di
`HOSTING.md` di ZIP versi PHP.

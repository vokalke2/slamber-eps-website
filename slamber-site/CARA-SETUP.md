# Cara Setup Panel Admin (Sekali Saja)

Folder ini berisi website Slamber.eps + panel admin di /admin. Supaya panel admin
bisa dipakai (login + simpan perubahan), situs ini WAJIB di-deploy lewat GitHub + Netlify
(bukan Netlify Drop biasa), karena panel admin butuh tempat menyimpan perubahan (Git) dan
sistem login (Netlify Identity).

## Langkah 1 — Upload folder ini ke GitHub
1. Buat akun di https://github.com kalau belum punya.
2. Buat repository baru, misalnya "slamber-eps-website".
3. Upload semua isi folder ini (index.html, admin/, content/, uploads/) ke repository tersebut.
   (Bisa lewat tombol "Add file > Upload files" di GitHub, tanpa perlu command line.)

## Langkah 2 — Hubungkan ke Netlify
1. Buka https://app.netlify.com, daftar/login (bisa pakai akun GitHub).
2. Klik "Add new site" > "Import an existing project" > pilih GitHub > pilih repository "slamber-eps-website".
3. Biarkan pengaturan build kosong (situs ini tidak perlu proses build), lalu klik Deploy.
4. Situs akan online dengan link seperti https://nama-acak.netlify.app.

## Langkah 3 — Aktifkan Identity & Git Gateway (supaya panel admin bisa dipakai)
1. Di dashboard Netlify situs kamu, buka menu "Identity" > klik "Enable Identity".
2. Buka "Identity > Settings" > bagian "Registration", pilih "Invite only" (supaya tidak
   sembarang orang bisa daftar).
3. Masih di menu Identity, buka tab "Services" > "Git Gateway" > klik "Enable Git Gateway".
4. Kembali ke tab "Identity", klik "Invite users", masukkan email anggota tim yang boleh
   mengelola konten (misalnya PIC Media & Documentation).
5. Anggota tersebut akan menerima email undangan, klik link-nya untuk set password.

## Langkah 4 — Mulai edit konten
1. Buka https://nama-situs-kamu.netlify.app/admin
2. Login pakai email & password yang sudah diset di Langkah 3.
3. Di dashboard, kamu akan lihat:
   - **Sosial Media & Donasi** — untuk isi link Instagram/TikTok/YouTube/WhatsApp,
     data rekening, foto QRIS, dan daftar Rekap Aksi (foto, video, judul, deskripsi, dst).
4. Setiap kali klik "Publish", perubahan otomatis tersimpan dan situs ter-update
   dalam waktu singkat — tanpa perlu upload file manual lagi.

## Setelah setup ini, cara update konten sehari-hari:
Cukup buka /admin, login, edit field yang mau diubah (atau tambah "Aksi" baru lewat
tombol "Add" di daftar Rekap Aksi), lalu klik Publish. Selesai.

# Basic GitHub Commands untuk Kolaborasi

## Setup Awal

```bash
# Clone repository
git clone git@github.com:username/repo-name.git

# Masuk ke folder project
cd repo-name

# Cek remote
git remote -v
```

## Alur Kerja Harian

```bash
# Selalu pull dulu sebelum mulai kerja
git pull origin main

# Cek status perubahan
git status

# Tambahkan file ke staging
git add .                   # semua file
git add nama-file.txt       # file tertentu

# Commit perubahan
git commit -m "pesan commit yang jelas"

# Push ke GitHub
git push origin main
```

## Bekerja dengan Branch

```bash
# Lihat semua branch
git branch

# Buat branch baru
git checkout -b nama-branch

# Pindah ke branch lain
git checkout nama-branch

# Push branch ke GitHub
git push origin nama-branch

# Merge branch ke main
git checkout main
git merge nama-branch

# Hapus branch setelah merge
git branch -d nama-branch
```

## Kolaborasi

```bash
# Ambil perubahan terbaru dari remote (tanpa merge)
git fetch origin

# Pull perubahan dari branch tertentu
git pull origin nama-branch

# Lihat log commit
git log --oneline

# Lihat perbedaan perubahan
git diff
```

## Mengatasi Konflik

```bash
# Setelah konflik diselesaikan secara manual, lakukan:
git add .
git commit -m "resolve merge conflict"
git push origin main
```

## Undo / Rollback

```bash
# Batalkan perubahan yang belum di-staging
git restore nama-file.txt

# Batalkan staging
git restore --staged nama-file.txt

# Kembali ke commit sebelumnya (hati-hati!)
git revert HEAD
```

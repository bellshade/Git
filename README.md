# Git

## Clone Repositori

```bash
git clone --depth 1 https://[username]:[tokenGithub]@github.com/[username]/[repositori]
```

## Cek Status Repositori di Local

```bash
git status
```

## Menyimpan Perubahan di Staging Area
Sebelum melakukan commit, file perlu dipindah ke staging area. Hal ini dilakukan agar Git mengetahui apa yang berubah antara commit saat ini dan commit berikutnya.

```bash
git add nama_file_1
git add nama_file_2
```
atau
```bash
git add nama_file_1 nama_file_2
```

Jika terdapat banyak file yang diubah, perintah berikut dapat dilakukan.

```bash
git add -A
```
atau (untuk semua file dan direktori)
```bash
git add .
```

## Menyimpan Perubahan di Local

```bash
git commit -m "Tuliskan di sini, apa aja yang berubah"
```

## Upload Repositori dari Local

```bash
git push
```

## Mengambil Update Repositori dari Server
Jika belum ada perubahan/commit di Repositori lokal gunakan git pull. Pull akan mengambil commit terbaru dan secara otomatis melakukan merge dengan repositori lokal.
```bash
git pull
```

Jika sudah ada perubahan/commit di Repositori lokal gunakan git fetch. Fetch hanya mengambil commit terbaru dan perlu melakukan merge secara manual.
```bash
git fetch
```

## Reset di Local
Untuk membatalkan commit, kembali ke commit sebelumnya yang diinginkan dan menghapus commit berikutnya.
Untuk reset dengan file dalam keadaan belum masuk staging area/modified.
```bash
git reset --MIXED nomor_commit
```
Untuk reset dengan file dalam keadaan staged.
```bash
git reset --SOFT nomor_commit
```
Untuk reset dengan file dalam keadaan commited.
```bash
git reset --HARD nomor_commit
```

## Revert
Untuk menggabungkan commit terbaru dengan commit sebelumnya. Biasanya akan terjadi konflik file namun bisa diselesaikan secara manual.
```bash
git revert nomor_commit
```

## Menambah Branch baru

```bash
git branch nama_branch
```

## Berpindah Branch

```bash
git checkout nama_branch
```

### Mengubah nama commit

```bash
git commit --amend -m "Message Commit Terbaru"
```

### Mengubah origin url

```bash
git remote set-url urlorigin-terbaru.git
```


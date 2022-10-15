# Git

![Git Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/6/62/Git-logo-orange.svg/273px-Git-logo-orange.svg.png)

Repositori ini panduan dalam menggunakan git dan perintah-perintah yang biasa dilakukan.

## 🎉 Selamat Datang di Git 🎉

Git adalah software gratis dan sumber terbuka untuk *distributed version-control*, yaitu pelacakan perubahan dalam jenis file apapun. Git dugunakan terutama untuk kolaborasi antar programmer dalam pengembangan kode pada *software development*.

## 📜 Sejarah Git 📜

Git pada awalnya ditulis oleh **Linus Torvalds** pada tahun 2005 untuk pengembangan kernel Linux. Torvalds terpaksa membuat Git karena adanya kontroversi komunitas pengembang kernel Linux dengan *version-control system* (VCS) yang mereka gunakan sebelumnya, yaitu **BitKeeper**. Berawal dari situ Git menjadi salah satu program yang paling sering digunakan oleh developer di seluruh dunia.

## ❓ FAQ (Pertanyaan yang sering ditanyakan) ❓

### *Mengapa harus belajar Git?*

Karena Git merupakan program VCS yang paling populer di dunia. Selain itu banyak sekali fitur Git yang dapat digunakan dan memudahkan dalam pengembangan kode, seperti pelacakan perubahan file, dan kolaborasi dengan orang lain.

### *Apa bedanya Git dengan GitHub/GitLab?*

**Git** adalah program sistem kontrol versi yang dapat digunakan secara offline maupun online. **GitHub atau Gitlab** adalah layanan cloud untuk mengelola dan meniyampan repository git yang memiliki konsep kerja layaknya Git. Namun untuk menggunakan GitHub atau Gitlab, kita harus terhubung dengan internet. Developer juga bisa menggunakannya sebagai media sosial antar developer karena banyaknya fitur tambahan yang tidak ada di Git.

## ⚙ Instalasi ⚙

Git :

<https://git-scm.com/downloads>

Git GUI alternative (bila anda tidak suka Git versi CLI) :

<https://git-scm.com/downloads>

## 💨 Panduan Penggunaan 💨

Git bisa diakses melalui CLI maupun GUI. Perintah dasar berikut digunakan untuk Git CLI. Gunakan terminal dan pastikan Git sudah ada dalam ```$PATH``` sistem operasi yang anda gunakan. Ketikkan perintah berikut untuk memastikan Git sudah terpasang :

```bash
git help
```

Output :

```text
usage: git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path]

... dan seterusnya
```

## 🤖 Perintah Dasar 🤖

### Clone Repositori

```bash
git clone --depth 1 https://[username]:[tokenGithub]@github.com/[username]/[repositori]
```

### Cek Status Repositori di Local

```bash
git status
```

### Menyimpan Perubahan di Staging Area

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

### Menyimpan Perubahan di Local

```bash
git commit -m "Tuliskan di sini, apa aja yang berubah"
```

### Upload Repositori dari Local

```bash
git push
```

### Mengambil Update Repositori dari Server

Jika belum ada perubahan/commit di Repositori lokal gunakan git pull. Pull akan mengambil commit terbaru dan secara otomatis melakukan merge dengan repositori lokal.

```bash
git pull
```

Jika sudah ada perubahan/commit di Repositori lokal gunakan git fetch. Fetch hanya mengambil commit terbaru dan perlu melakukan merge secara manual.

```bash
git fetch
```

### Reset di Local

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

### Revert

Untuk menggabungkan commit terbaru dengan commit sebelumnya. Biasanya akan terjadi konflik file namun bisa diselesaikan secara manual.

```bash
git revert nomor_commit
```

### Menambah Branch baru

```bash
git branch nama_branch
```

### Berpindah Branch

```bash
git checkout nama_branch
```

### Menambah Branch baru + Checkout

Perintah ini secara otomatis membuat branch baru dan langsung checkout ke branch baru tersebut.

```bash
git checkout -b nama_branch
```

### Mengubah nama commit

```bash
git commit --amend -m "Message Commit Terbaru"
```

### Mengubah origin url

```bash
git remote set-url urlorigin-terbaru.git
```

## 📚 Referensi dan Bacaan Lebih Lanjut 📚

- Git Documentation <https://git-scm.com/docs>
- Pro Git Book (free) <https://git-scm.com/book/en/v2>
- Git Cheatsheet
  - from GitHub <https://education.github.com/git-cheat-sheet-education.pdf>
  - from BitBucket <https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet>
- GitHub Docs <https://docs.github.com/en>
- GitHub Skills <https://skills.github.com/>

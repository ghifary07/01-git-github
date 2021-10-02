# Laporan mengelola git

## Personal Access Token

Sebelum mengelola repository, hal pertama yang harus dilakukan adalah membuat personal access token.
Karena proses mengelola repo ini memerlukan akses repo dari command line / shell, sehingga wajib menggunakan token.
Setelah membuat personal akses token mengikuti [petunjuk](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token), hasilnya adalah:
![tokenconfig](images/03/auth.png)

## Membuat Repository

1. Klik tanda + pada bagian kanan atas setelah login ke github, lalu pilih new repository.                      
![repo](images/03/repo1.png)

2. Isi nama repository, deskripsi, pengaturan publik atau private, lisensi, dan tambahan lainnya. Setelah itu klik create repository.
![repo](images/03/repo2.png)

## Clone Repository

Selanjutnya adalah clone repository ke komputer lokal agar lebih mudah dikelola. Clone repository dilakukan dengan perintah:

```
$ git clone https://github.com/ghifary07/01-git-github
```

Setelah itu akan ada folder baru dengan nama repository tersebut di tempat dimana perintah itu diketikkan.
![repo](images/03/repo3.png)

Jika repo sudah di clone selanjutnya adalah mmengubah nama branch utama.
Nama branch utama di pengaturan default git adalah master.
Untuk mengubahnya menjadi main bisa digunakan:

```
$ cd 01-git-github
$ git branch -m main
```

## Mengubah isi git - Push

Untuk menambahkan file yang sudah dibuat dari folder repository lokal ke repository remote/online dapat dilakukan push.
Push dilakukan jika terdapat perubahan seperti membuat file, menghapus file, mengedit file, dan membuat direktori baru.
Push dapat dilakukan di direktori repo lokal dengan perintah:

```
$ git add . 
$ git commit -m "first commit" 
$ git push origin main
```
1. git add “.” atau nama file
untuk menambah file project yang akan di upload sebelum di commit, tanda titik setelah kata “add” pada perintah tersebut artinya semua file yang ada di folder akan diupload ke repository online. Perintah ini dapat digunakan ketika menambahkan file pertama kali. 

1. git commit -m “isi commit”
untuk menambah keterangan/status perubahaan saat upload ke repo online, keterangan ditulis setelah “git commit -m” ditambah tanda petik lalu komentar.

3. git push origin “nama branch”
Perintah untuk mengupload file yang ada pada repo lokal ke repo online yang diletakkan pada branch yang sudah tersedia di repo online.

Setelah itu refresh halaman repository di github dan file sudah berhasil ditambahkan.
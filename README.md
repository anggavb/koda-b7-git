# Basic Git Command (local)

### 1. Inisialisasi folder project dengan git
```sh
$ git init
```
Proses ini akan membuat folder tersembunyi bernama ``.git``.
### 2. Mengirim perubahan kedalam staging area
```sh
$ git add path/filename
```
### 3. Membarikan pesan kedalam perubahan yang dikirim
```sh
$ git commit -m "type: description"
```
Fungsi ``-m`` adalah untuk membuat pesan commit atau perubahan sebelum dikirim.  
Jika ingin memberikan pesan versi panjang:
```sh
$ git commit
```
Setelahnya akan menampilkan text editor vim, silahkan isi pesan commit dari baris pertama.
### 4. Menambahkan remote repository
```sh
$ git remote add [url_repository]
```
### 5. Kirim perubahan ke remote repository (sinkronisasi local ke remote)
```sh
$ git push -u [nama_remote] [nama_branch]
```
### 6. Untuk melakukan sinkronisasi dari remote ke local
```sh
$ git pull [nama_remote] [nama_branch]
```
### 7. Config

## 8. Cloning
Replikasi identik
```sh
# jika ingin menggunakan nama folder sama dengan nama repo
$ git clone [url]
# jika ingin menggunakan nama folder berbeda dari naam repo
$ git clone [url] [namaFolder]
```
namaFolder diberikan jika menginginkan nama folder yang berbeda dengan nama repo

## 7. History
- ``log`` = riwayat commit publik
```sh
$ git log
```
- ``reflog`` = riwayat git yang lebih private, tidak hanya riwayat commit namun juga riwayat lain seperti ``pull``, ``reset`` dan ``revert``
```sh
$ git reflog
```
## 8. Undoing Changes
- ``revert`` = menghilangkan commit dengan commit revert yang baru
```sh
$ git revert [commit_code]
```
- ``reset`` = mundur ke titik commit tertentu
```sh
$ git reset [commit_code]
```

## 9. Branching
- ``branch``
```sh
$ git branch [option] [argument]
```
```sh
# list branch
$ git branch
# create new branch
$ git branch [branch_name]
# rename branch
$ git branch [-m|-M] [old_branch] [new_branch]
# copy branch
$ git branch [-c|-C] [source_branch] [dest_branch]
# delete branch
$ git branch [-d|-D] [branch_name]
```
- ``checkout``
```sh
# moving between branch
$ git checkout [dest_branch]
# moving to branch (and create it if not exists)
$ git checkout -b [branch_name]
# moving between commit
$ git checkout [commit_code]
```
- ``merge``
```sh
# you have to move to destination branch first
$ git merge [source_branch...]
```
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
Setelahnya akan menampilkan text editor vim, silahkan isi pesan commit di baris pertama.
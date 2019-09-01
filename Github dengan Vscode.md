Akses Repo Github dengan Windows Explorer dan Vscode
====================================================

Artikel ini untuk ditujukan untuk blind coder yang merasa kesulitan tiap kali
harus mengolah repo github lewat versi web. Dengan mengikuti tutorial ini, Anda
akan bisa dengan mudahnya, menambah, mengedit, commit, dan mengupdate repository
github anda lewat windows explorer dan vscode saja.

Pengaturan Awal
===============

Instalasi Git Pada Windows 
---------------------------

Sebelum bisa menggunaka Git pada windows, kita perlu meng-install program Git
terlebih dahulu:

1.  Download git for windows (45.5 MB):

    <https://git-scm.com/download/win>

    Download akan mulai secara otomatis.

2.  Jalankan installer. Ada beberapa bagian yang harus di ubah konfigurasinya:

-   Tekan next terus sampai 4 kali sampai ketemu combo box “Use Vim (the
    ubiquitous text editor) as Git's default editor”. Pilih “Use Visual Studio
    Code as Git's default editor”.

-   Tekan Next 4 kali lagi sampai ketemu radio button “Use MinTTY (the default
    terminal of MSYS2)”, tekan panah atas untuk memilih “Use Windows' default
    console window”.

-   Tekan Next terus, lalu install.

Setup Akun Git pada Komputer Lokal.
-----------------------------------

Sebelum kita bisa menggunakan fitur git, kita harus setting akun git terlebih
dahulu.

### Git username

Pertama, kita harus memasukkan username untuk git kita. Username git ini beda
dengan username untuk log in ke github.com. Nama ini lah yang nantinya akan
muncul saat Anda melakukan commit pada proyek-proyek yang Anda jalani.
Disarankan menggunakan nama lengkap. Berikut langkahnya:

1.  Buka command prompt.

2.  Ketik:

    Git config --global user.name “Nama Anda”

3.  Selesai. Cek nama anda dengan mengetik:

    Git config --global user.name

### Git Email

Selanjutnya, set email pada git local Anda. Email ini sebenarnya boleh berbeda
dengan email yang digunakan pada Github. Namun, untuk konsistensi dan kemudahan,
sebaiknya gunakan email yang sama dengan email github. Pada command prompt
ketik:

Git config –global user.email <emailAnda@misalnya.com>

### Github credential helper

Berikutnya, jalankan perintah di bawah untuk menyuruh git mengingat username dan
password login github kita yang akan kita masukkan di tahap berikutnya. Ini
bertujuan agar kita tidak perlu memasukkan username dan password github
berulang-ulang setiap kali kita melakukan koneksi remote dari git local ke
github.

git config --global credential.helper wincred

Selamat! Proses pengaturan awal sudah selesai. Sekarang mari kita coba mengolah
repository github dengan vscode!

Sekarang, kita sudah siap membuat repository baru atau meng-clone repository
github kita ke git local. Nantinya, kita bisa dengan mudah menambah, mengedit,
meng-commit, serta mengupdate repository git kita ke github dengan lebih cepat
dan mudah, cukup menggunakan windows explorer dan vscode saja.

Clone Repository Github 
------------------------

Clone bertujuan untuk membuat Salinan dari online repository github ke
repository git local pada computer kita. Ketika kita sudah memiliki repo git
local, kita bisa dengan mudah mengedit file, menambahkan dan mensikronisasi repo
git ke github kita. Biar lebih jelas, mari kita langsung praktek:

1.  Buka halaman repository github yang Anda ingin clone. Jika Anda belum pernah
    buat repository, Anda bisa buat dulu. Tidak masalah jika repository baru
    Anda saat ini masih kosong.

2.  Copy alamat url resource anda dari browser address bar. Contoh link url
    repo:
    [https://github.com/adinugraha2611//javascript](https://github.com/adinugraha2611/javascript)

3.  Buka vscode

4.  Tekan Ctrl Shift P, lalu ketik “git clone”, lalu tekan enter.

    Tips: Ctrl Shift P menampilkan command palettes, yaitu list jalan pintas
    untuk menjalankan semua command yang ada dalam vscode. Jadi semisal Anda
    lupa shortcut untuk debug, anda cukup tekan Ctrl Shift P, ketikkan “debug”,
    lalu langsung muncul command-command yang berhubungan dengan debugging.
    Tekan panah atas/bawah untuk melihat list command. Tekan enter untuk
    menjalankannya. Tekan Escape untuk menutup command palletes.

5.  Akan muncul edit box. Langsung Paste aja url repositorynya di situ, lalu
    langsung tekan enter.

6.  Akan muncul “select folder dialog” yang meminta Anda untuk memilih tempat
    untuk menampung folder repository pada git local. Singkatnya, repository
    beserta seluruh isinya akan di download ke dalam satu folder yang Namanya
    persis dengan nama repository di github. . misalnya saya akan menaruh folder
    ini di direktori F:\\Documents. Setelah folder terpilih, tekan tab tab
    sampai ketemu “select repository location”

7.  Buka folder repo anda di windows explorer. Jadi untuk contoh saya, saya akan
    membuka direktori F:\\Documents\\javascript.

8.  Perhatikan isinya! File dan folder yang ada di dalamnya akan sama persis
    dengan yang ada di github. Jika repo yang anda clone adalah repo yang baru
    dibuat, maka isinya kemungkinan hanya aka nada 1 file .git saja.

9.  Sekarang anda bisa tambah atau edit file/folder didalam folder repo ini
    sepuasnya! Setiap file yang mengalami perubahan pada folder ini akan
    diketahui oleh vscode.

Meng-commit git dan Push ke Github.
-----------------------------------

Pada tahap ini, kita sudah memiliki sebuah repo git local yang sudah kita edit
dan siap untuk kita push ke repo github online. Istilah push ini artinya kita
meng-update perubahan-perubahan yang sudah kita lakukan di repo git local ke
repo github kita, sehingga repo github kita tersinkronisasi dengan repo git
local kita. Mudah-mudahan ini gak terlalu membingungkan ya.

Mari kita langsung saja

1.  buka vscode dan open folder (Ctrl + K lalu ctrl + o), pilih folder repo kita
    (yang terdapat file .git), lalu klik “select folder” (di tab tab saja sampai
    ketemu).

2.  Tekan ctrl shift G, akan muncul “Message (press Ctrl+Enter to commit)”,
    tekan tab sekali.

3.  Akan ada tree view, tekan panah bawah.

4.  Akan ada “Changes 3 blablabla”. Bilangan yang disebutkan setelah changes
    adalah jumlah file yang telah anda ubah sebelumnya. Dalam contoh saya, saya
    mengubah 3 file. Jika anda panah bawah lagi, dapat dilihat file apa saja
    yang telah diubah.

Sekarang mari kita comit changes. Perlu dipahami, file file yang sudah kita ubah
tadi masih hanya berstatus “ditandai” oleh git. Artinya, git tau kalua file
tersebut dirubah, namun perubahannya belum benar-benar disimpan. Proses commit
inilah yang akan menyimpan semua perubahan yang telah kita lakukan ke git local.
Semoga bisa dipahami yaa.

1.  Tekan ctrl shift G untuk memunculkan “Message (press Ctrl+Enter to commit)”.

2.  Ini adalah edit box yang menampung commit message kita. Di Disini Anda bisa
    mengetikkan catatan tentang commit yang anda buat. Misalnya, anda bisa
    mencatatkan kenapa anda membuat perubahan pada file, bagian mana yang
    diubah, atau catatan lain yang sekiranya perlu diketahui/diingat oleh Anda
    sendiri atau orang lain yang hendak bergabung dalam projek anda.

3.  Jika anda sudah yakin bahwa tidak ada lagi yang perlu diubah, tekan ctrl +
    Enter untuk menjalankan commit.

4.  Akan muncul notifikasi yang kurang lebih berisi “the commit is not staged.
    Do you want to automatically stage all changes?” dengan 3 pilihan: “always”,
    “yes”, dan “no”. pilih saja “yes”. Hal ini akan dijelaskan lebih rinci di
    bagian selanjutnya.

5.  Tunggu sesaat dan proses commit telah selesai!

6.  Untuk cek apakah commit sudah berhasil, tekan Ctrl Shift G lagi lalu tab ke
    bagian “tree view”, dan lihat bagian “changes blablabla”. Jika “Changes 0”
    dan tidak ada file yang tercatat di bawahnya, berarti commit berhasil.

Push Repo Git ke Repo Github.
-----------------------------

Perlu diingat, Commit yang dilakukan pada tahap sebelumnya masih sebatas pada
git local di computer Anda. Sekarang mari kita push commit tersebut ke repo
github kita.

1.  Tekan ctrl shift P, lalu ketik “git push”.

2.  Tunggu sebentar. Akan muncul window baru yang meminta anda mengisikan
    username dan password github anda. Silahkan masukkan dan klik tombol login
    (tekan tab tab saja untuk navigasi). Tahap ini hanya akan terjadi sekali
    saja.

3.  Tunggu sejenak dan proses push selesai! Cek halaman repo github Anda dan
    lihat last commit-nya.

Anda bisa mengulang proses diatas sesuka hati Anda. Untuk merekap, berikut
urutan langkah yang Anda lakukan:

1.  Clone repository github ke local git folder dalam computer Anda

2.  Edit file dalam local git repo sesukanya.

3.  Buka vscode, commit changes.

4.  Push commits ke repo github.

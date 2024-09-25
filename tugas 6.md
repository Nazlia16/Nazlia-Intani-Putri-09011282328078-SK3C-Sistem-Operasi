LAPORAN PRAKTIKUM 5 TUGAS 6 " JOB CONTROL "

Nama : Nazlia Intani Putri

NIM : 09011282328078


1. Eksekusi seluruh profile yang ada : 

a. Edit file profile /etc/profile dan tampilkan pesan sebagai berikut : 
echo “Profile dari /etc/profile”

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/1A.png)


b. Asumsi nama anda stD02001, maka edit semua profile yang ada yaitu : 

/home/stD02001/.bash_profile 

/home/. stD02001/.bash_login 

/home/mahasiswa/.profile 

/home/mahasiswa/.bashrc 

Ganti nama /home/mahasiswa dengan nama anda sendiri. Pada setiap 
file tersebut, cantumkan instruksi echo, misalnya pada /home/ mahasiswa/.bash_profile : 
echo “Profile dari .bash_profile”

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/1b%20pertama.png)

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/1B.png)

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/1BB.png)

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/1bbb.png)

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/1bbbb.png)


c. Jalankan instruksi subtitute user, kemudian keluar dengan perintah exit sebagai berikut: 

$ su mahasiswa 

$ exit 

kemudian gunakan opsi – sebagai berikut : 

$ su – mahasiswa 

$ exit 

Jelaskan perbedaan kedua utilitas tersebut.

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/1C.png)

1. su mahasiswa:  
Perintah su mahasiswa digunakan untuk beralih ke akun pengguna bernama "mahasiswa" tanpa mengubah lingkungan shell secara penuh. Dalam hal ini, hanya identitas pengguna yang berubah, tetapi variabel lingkungan (seperti $PATH, alias, dan pengaturan shell lainnya) tetap milik pengguna saat ini. Ini berarti beberapa program atau perintah mungkin tidak berfungsi dengan benar karena masih menggunakan konfigurasi dari pengguna asli.

2. su - mahasiswa:   
Sedangkan su - mahasiswa tidak hanya mengubah identitas pengguna, tetapi juga memulai sesi shell baru seperti halnya ketika pengguna "mahasiswa" masuk secara langsung. Semua variabel lingkungan akan direset sesuai dengan pengaturan default pengguna "mahasiswa", termasuk $HOME, $PATH, dan lainnya. Ini memberikan pengalaman yang lebih lengkap dan aman, seolah-olah Anda baru saja login sebagai "mahasiswa".

2. Prompt String (PS) 

a. Edit file .bash_profile, ganti prompt PS1 dengan ‘>’. Instruksi export diperlukan dengan 
parameter nama variable tersebut, agar perubahan variable PS1 dikenal oleh semua shell 
PS1=‟> „ 
export PS1

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/2A.png)

b. Eksperimen hasil PS1 :
$ PS1=“\! > “ 
69 > PS1=”\d > “ 
Mon Sep 23 > PS1=”\t > “ 
10:10:20 > PS1=”Saya=\u > “ 
Saya=mahasiswa > PS1=”\w >” 
~ > PS1=\h >” 


![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/2B.png)


3. Logout 
Edit file .bash_logout, tampilkan pesan dan tahan selama 5 detik, sebelum eksekusi logout 
Echo “Terima kasih atas sesi yang diberikan”
Sleep 5 
clear

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/3A.png)

4. Bash script 

a. Buat 3 buah script p1.sh, p2.sh, p3.sh dengan isi masing-masing : 
p1.sh 
#! /bin/bash 
echo “Program p1” 
ls –l 
p2.sh 
#! /bin/bash 
echo “Program p2” 
who 
p3.sh 
#! /bin/bash 
echo “Program p3” 
ps x

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/4A.png)

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/4AA.png)

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/4AAA.png)

b. Jalankan script tersebut sebagai berikut : 
$ ./p1.sh ; ./p3.sh ; ./p2.sh 
$ ./p1.sh & 
$ ./p1.sh $ ./p2.sh & ./p3.sh & 
$ ( ./p1.sh ; ./p3.sh ) &

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/4b.png)

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/4bb.png)

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/4bbb.png)

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/4bbbb.png)



5. Jobs 

a. Buat shell-script yang melakukan loop dengan nama pwaktu.sh, 
setiap 10 detik, kemudian menyimpan tanggal dan jam pada file hasil. 
#!/bin/bash 
while [ true ] 
do 
date >> hasil 
sleep 10 
done

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/5.png)

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/5A.png)


b. Jalankan sebagai background; kemudian jalankan satu program (utilitas find) di background 
sebagai berikut : 
$ jobs 
$ find / -print > files 2>/dev/null & 
$ jobs 

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/5bb.png)

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/5bbb.png)


c. Jadikan program ke 1 sebagai foreground, tekan ^Z dan kembalikan program tersebut ke 
background 
$ fg %1 
$ bg 

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/5c.png)


d. Stop program background dengan utilitas kil 
$ ps x 
$ kill [Nomor PID] 

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/5D.png)

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/5DD.png)


6. History 

a. Ganti nilai HISTSIZE dari 1000 menjadi 20 
$ HISTSIZE=20 
$ h 

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/6A.png)

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/6AA.png)



b. Gunakan fasilitas history dengan mengedit instruksi baris ke 5 dari instruksi yang terakhir
dilakukan 
$ !-5


![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/6B.png)

c. Ulangi instruksi yang terakhir. Gunakan juga ^P dan ^N untuk bernavigasi pada history bufer

$ !!

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/6C.png)

d. Ulangi instruksi pada history bufer nomor 150 
$ !150

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/6D.png)


e. Ulangi instruksi dengan prefix “ls” 
$ !ls

![Alt Text](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/Galeri%20SO%20P6/6E.png)

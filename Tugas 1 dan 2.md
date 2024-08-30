# LAPORAN PRAKTIKUM SISTEM OPERASI 1 DAN 2

## Oleh:
**Nama**: Nazlia Intani Putri  
**NIM**: 09011282328078

## Dosen Pengampu:
Adi Hermansyah, M.T.

## TAHUN AKADEMIK 2024/2025  
UNIVERSITAS SRIWIJAYA

---

# BAB I: PENDAHULUAN

## 1.1 Tujuan Praktikum
Tujuan dari sebuah praktikum adalah untuk memberikan pengalaman praktis yang langsung terkait dengan materi Sistem Operasi, seperti menjalankan Graphic User Interface (GUI) maupun menganalisis proses instalasi.

## 1.2 Alat yang Digunakan
1. Laptop
2. Virtual Machine
3. Sistem operasi Linux atau Ubuntu

---

# BAB II: PEMBAHASAN

## 2.1 Instalasi Virtual Machine
![Instalasi Linux pada Vmware](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/galeri%20so/instalasi%20Vmware.png)
![Instalasi Linux pada Vmware](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/galeri%20so/instalasi%20Vmware%202.png)
![Instalasi Linux pada Vmware](https://github.com/Nazlia16/Nazlia-Intani-Putri-09011282328078-SK3C-Sistem-Operasi/blob/main/galeri%20so/instalasi%20Vmware%203.png)

*Gambar tersebut merupakan bukti bahwa telah selesai melakukan instalasi Linux pada Vmware.*

## 2.2 Analisis “/“ pada Opsi Mount Point
Saat instalasi dilakukan, di bagian create partition kita memilih “/” pada opsi Mount Point. Hal ini dikarenakan partisi tersebut merupakan yang tertinggi pada Linux dan merupakan tanda Root. Root direktori ini adalah tempat awal di mana nantinya semua direktori akan bercabang.

## 2.3 Apa itu ext4, ext3, swap, ntfs, fat32, btrfs?

1. **Ext 4 (4th Extended)**  
   Ext 4 dirilis secara komplit dan stabil berawal dari kernel 2.3.28. Jika distro secara default memiliki versi kernel tersebut atau di atasnya, sistem Anda sudah mendukung ext4. Keuntungan meng-upgrade filesystem ke ext4 dibanding ext3 adalah kemampuan pengalamatan 48-bit block, yang berarti ukuran maksimum filesystem adalah 1 EB (1.048.576 TB) dengan maksimum ukuran file 16 TB. Selain itu, ext4 juga memiliki kelebihan seperti fast fsck, journal checksumming, dan defragmentation support.

2. **Ext 3 (3rd Extended)**  
   Ext3 adalah pendahulu dari ext4 dan juga mendukung fitur journaling. Ini memastikan integritas data dengan mencatat perubahan sebelum diterapkan. Namun, ext3 memiliki keterbatasan pada ukuran file (hingga 2 TB) dan kinerja yang lebih rendah dibandingkan ext4.

3. **Swap**  
   Swap bukan sistem berkas tetapi partisi khusus yang digunakan oleh Linux untuk menambah memori fisik (RAM) dengan menyediakan ruang pada disk sebagai memori virtual. Ketika RAM hampir habis, sistem akan menggunakan swap space ini untuk memindahkan data dari RAM ke disk sementara, memungkinkan operasi terus berjalan meskipun dengan kinerja yang lebih lambat.

4. **NTFS (New Technology File System)**  
   NTFS adalah sistem berkas standar untuk sistem operasi Windows modern. Ini mendukung fitur-fitur seperti enkripsi, kompresi file, kontrol akses, dan pemulihan kesalahan. NTFS dirancang untuk mendukung file dan partisi yang sangat besar serta memiliki fitur journaling untuk menjaga integritas data.

5. **FAT32 (File Allocation Table 32)**  
   FAT32 adalah sistem berkas yang lebih tua dan sangat kompatibel dengan hampir semua sistem operasi. Ini sering digunakan pada perangkat penyimpanan portabel seperti USB drive dan kartu SD. Keterbatasannya termasuk ukuran file maksimum 4 GB dan ukuran partisi maksimum 2 TB.

6. **BTRFS (B-tree File System)**  
   BTRFS adalah sistem berkas Linux yang dikembangkan untuk menyediakan fitur-fitur canggih seperti snapshotting, subvolume, checksumming data dan metadata, serta manajemen penyimpanan yang lebih fleksibel. BTRFS dirancang untuk menjadi alternatif yang lebih modern dan fleksibel dibandingkan ext4, meskipun ext4 masih lebih banyak digunakan dalam lingkungan produksi.

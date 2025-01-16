# Guide-ParrotOS-aeraski
my journey use parrot OS
# source : https://github.com/mikeroyal/Parrot-Security-Guide

<p align="center">
  <img src="https://user-images.githubusercontent.com/45159366/128566116-28363ba8-ad10-453c-9fe5-7857e11c136b.png">
  <br />
</p>

# Table of Contents

1. [EFI System Partition (ESP)](#efi-system-partition-esp)
2. [Root (/)](#root-)
3. [Swap (Opsional)](#swap-opsional)
4. [Cara Membuat Partisi di Installer Parrot OS](#cara-membuat-partisi-di-installer-parrot-os)
5. [Asus Battery Health Charging Script For Linux](#asus-battery-health-charging-script-for-linux)
6. [Section Baru Lainnya](#section-baru-lainnya)
7. [Set time and date](#set-time-and-date)
# EFI System Partition (ESP)

- **Ukuran**: 100–512 MB (biasanya cukup 300 MB).
- **Sistem File**: FAT32.
- **Mount Point**: /boot/efi.
- **Fungsi**: Menyimpan file bootloader untuk UEFI.
- **Catatan**: Partisi ini wajib ada jika menggunakan UEFI.

# Root (/)

- **Ukuran**: Gunakan seluruh ruang disk yang tersisa.
- **Sistem File**: EXT4.
- **Mount Point**: /.
- **Fungsi**: Menyimpan data sistem operasi dan file pengguna.

# Swap (Opsional)

- **Ukuran**: 2–4 GB, atau 16 GB untuk hibernasi.
- **Fungsi**: Memori cadangan atau untuk hibernasi.

# Cara Membuat Partisi di Installer Parrot OS

1. Pilih **Manual Partitioning**.
2. Buat Partisi EFI (FAT32, 100–512 MB).
3. Buat Partisi Root (EXT4, seluruh sisa kapasitas).
4. (Opsional) Buat partisi Swap.
5. Simpan konfigurasi dan lanjutkan instalasi.

# Asus Battery Health Charging Script For Linux
kunjungi https://github.com/sakibulalikhan/asus-battery-health

# Set time and date
To update the time and date from the internet on a Linux distribution that uses a modern version of systemd, you can use:
```bash
timedatectl set-ntp true
```
Source : https://unix.stackexchange.com/questions/79112/how-do-i-set-time-and-date-from-the-internet

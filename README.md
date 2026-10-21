# 🖥️ Windows Server Home Lab — Infrastructure & Network Documentation

Repositori ini berisi dokumentasi praktik mandiri dalam membangun, mengonfigurasi, dan mengelola lingkungan jaringan **Server–Client** menggunakan **Oracle VM VirtualBox**.

---

## ⚙️ Spesifikasi Lingkungan Virtual (Lab Environment)
* **Hypervisor:** Oracle VM VirtualBox
* **OS Server:** Windows Server (Domain Controller, DHCP, & File Server)
* **OS Client:** Windows 10 / 11 Pro
* **Topologi Jaringan:** Internal Network (Static IP pada Server & Dynamic DHCP pada Client)

---

## 1. Administrasi Active Directory (OU) & DHCP Server
* Membuat **Organizational Unit (OU)** untuk mengelompokkan akun pengguna dan perangkat berdasarkan divisi kerja secara terpusat.
* Mengonfigurasi **DHCP Scope (Address Pool)** untuk mendistribusikan alamat IP secara otomatis ke perangkat Client yang terhubung ke jaringan lokal.

![Active Directory dan DHCP](server-ad-dhcp.png)

---

## 2. Pengujian Konektivitas Jaringan Dua Arah (ICMP Ping)
* Memastikan komunikasi antara **Windows Server** dan **Client** berjalan lancar tanpa *packet loss* (`0% loss`) melalui pengujian `ping` dua arah di Command Prompt.

![Uji Koneksi Ping Server Client](jaringan-ping.png)

---

## 3. Centralized Software Deployment (File Server SMB — MS Office)
* **Studi Kasus Efisiensi IT Support:** Agar tidak perlu mengunduh ulang atau menyalin file *installer* menggunakan *flashdisk* satu per satu ke setiap komputer karyawan, Windows Server dikonfigurasi sebagai **File Server (Shared Folder)**.
* **Implementasi:** Menyimpan file instalasi **Microsoft Office** di dalam *shared directory* pada Server, mengatur izin akses (*Read/Execute Permissions*), dan mengeksekusi instalasi langsung dari komputer Client melalui jalur jaringan lokal (`\\IP-Server\Software\Office`).

*(Dokumentasi tangkapan layar instalasi via Network Share sedang dalam tahap pembaruan)*

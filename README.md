# 🖥️ Windows Server & Endpoint Administration — Home Lab Documentation

Repositori ini berisi dokumentasi praktik mandiri dalam membangun, mengelola, dan melakukan *troubleshooting* lingkungan jaringan **Server–Client** menggunakan **Windows Server** pada **Oracle VM VirtualBox**.

---

## ⚙️ Spesifikasi Lingkungan Virtual (Lab Environment)
* **Hypervisor:** Oracle VM VirtualBox
* **OS Server:** Windows Server (Domain Controller, DHCP, GPO, & SMB File Server)
* **OS Client:** Windows 10 / 11 Pro
* **Fokus Kompetensi:** Active Directory, DHCP, Group Policy, Network File Sharing, Endpoint Troubleshooting & Firewall

---

## 1. Administrasi Active Directory Domain Services (AD DS) & Organizational Unit (OU)
* **Skenario Industri:** Membangun *Domain Controller* dan merancang struktur **Organizational Unit (OU)** pada *Active Directory Users and Computers* untuk mengelompokkan akun pengguna serta perangkat komputer berdasarkan divisi kerja secara terpusat.

![Struktur Organizational Unit Active Directory](server-ad-dhcp.png)

---

## 2. Konfigurasi Layanan DHCP Server (Dynamic IP Distribution)
* **Skenario Industri:** Mengonfigurasi **DHCP Scope (IPv4 Address Pool)**, *Default Gateway*, dan *DNS Server* pada Windows Server agar komputer Client di jaringan lokal mendapatkan alamat IP secara otomatis (*Address Leases*).

> 📸 **Slot Screenshot DHCP Server:** 
[Konfigurasi DHCP Server](dhcp-server.png)

---

## 3. Pengujian Konektivitas Jaringan Dua Arah (ICMP Ping)
* **Skenario Industri:** Memverifikasi komunikasi jaringan timbal balik antara **Windows Server** dan komputer **Client** menggunakan protokol ICMP (`ping`) di Command Prompt dengan hasil `0% packet loss`.

### 3A. Uji Ping dari Server ke Client (`192.168.100.11`)
[Uji Koneksi Ping dari Server ke Client](jaringan-ping.png)

### 3B. Uji Ping dari Client ke Server
> 📸 **Slot Screenshot Ping Client ke Server:** 
[Uji Koneksi Ping dari Client ke Server](ping-client-ke-server.png) -->

---

## 4. Centralized Software Deployment (SMB File Server — MS Office)
* **Skenario Industri:** Menyediakan *Shared Folder* terpusat pada Windows Server sebagai wadah penyimpanan *installer* aplikasi (**Microsoft Office**), sehingga tim IT Support dapat menjalankan instalasi langsung dari komputer Client melalui jaringan lokal (`\\IP-Server\Software`) tanpa perlu menggunakan *flashdisk* di setiap perangkat.
* **Perintah & Konfigurasi:** Pengaturan *SMB Sharing Permissions* & *NTFS Security* (Read & Execute).

> 📸 **Slot Screenshot File Server:** Upload gambar dengan nama `fileshare-office.png`, lalu hapus tanda `<!--` dan `-->` di bawah ini.
<!-- ![File Server MS Office](fileshare-office.png) -->

---

## 5. Penerapan Kebijakan Terpusat dengan Group Policy Objects (GPO)
* **Skenario Industri:** Menerapkan standarisasi keamanan dan pembatasan akses pada komputer karyawan secara massal dari sisi Server menggunakan **Group Policy Management** yang dihubungkan ke *Organizational Unit (OU)*.
* **Perintah Verifikasi di Client:** `gpupdate /force` dan `gpresult /r`.

> 📸 **Slot Screenshot GPO:** Upload gambar dengan nama `gpo-policy.png`, lalu hapus tanda `<!--` dan `-->` di bawah ini.
<!-- ![Konfigurasi Group Policy Objects](gpo-policy.png) -->

---

## 6. Investigasi System Logs (Event Viewer) & Konfigurasi Windows Firewall
* **Skenario Industri:** Melacak penyebab *error* aplikasi maupun layanan sistem operasi menggunakan **Windows Event Viewer**, serta mengatur aturan keluar-masuk trafik *port* pada **Windows Defender Firewall with Advanced Security**.

> 📸 **Slot Screenshot 6A (Event Viewer):** Upload gambar dengan nama `event-viewer.png`, lalu hapus tanda `<!--` dan `-->` di bawah ini.
<!-- ![Investigasi Log di Windows Event Viewer](event-viewer.png) -->

> 📸 **Slot Screenshot 6B (Windows Firewall):** Upload gambar dengan nama `windows-firewall.png`, lalu hapus tanda `<!--` dan `-->` di bawah ini.
<!-- ![Aturan Inbound Outbound Windows Firewall](windows-firewall.png) -->

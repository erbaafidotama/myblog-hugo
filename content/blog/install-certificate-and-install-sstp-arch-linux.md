---
title: "Install Certificate and Install SSTP - Arch Linux"
date: 2021-09-15T11:41:21+07:00
draft: false
---

Assalamualaikum warahmatullahi wabarakatuh, teman-teman.
Pada tulisan kali ini, gua akan ngasih ngasih tau cara install certificate dan install SSTP pada Linux dengan distribusi Arch beserta turunannya seperti Manjaro dan EndeavourOS. Hal itu agar kita bisa terkoneksi dengan server lain menggunakan VPN yang disini menggunakan jenis SSTP.

#### **Install Cerificate**
Oke,,, langkah pertama install dulu nih certificate-nya. Biasanya ekstensi nya itu crt (*.crt).
1. Buka terminal
2. Copy file certificate ke /etc/ca-certificates/trust-source/anchors
Masuk ke folder dimana teman-teman nyimpen file nya. Lalu tinggal run ini:
    
    ``cp *.crt /etc/ca-certificates/trust-source/anchors``
3. Cek file teman-teman udah ada di folder anchors atau belum, caranya:

    ``cd /etc/ca-certificates/trust-source/anchors``

    lalu

    ``ls``
4. Ini langkah terakhir. Run di terminal juga:

    ``update-ca-trust``


#### **Install SSTP**
Untuk yang ini adalah adalah cara untuk install SSTP. Ada dua cara dalam install sesuatu pada Arch Linux beserta turunannya (Manjaro, EndeavourOS, dll), yaitu melalui Package Manager dan Terminal. Untuk kali ini, gua ngasih tau caranya yang lewat Package Manager.
Melalui Package Manager, caranya:
1. Buka Package Manager
2. Search dengan keyword “SSTP” (ingat teman-teman sebaiknya aktifin dulu repo untuk AUR nya)
3. Tinggal klik, lalu install
4. Selesai

Untuk memastikan SSTP nya udah terpasang atau belum, bisa buka Settings lalu Network Configurations. Di dalam Network Configurations bisa menambahkan koneksi VPN, tulisan atau simbol untuk tambah koneksi VPN tergantung dari desktop environment dan distro nya teman-teman. Kalo udah muncul tampilan untuk tambah koneksi VPN, teman-teman bisa pilih jenis VPN-nya apa. Bisa dicek dibagian itu, apa SSTP sudah terpasang atau belum.

---

Sekian dulu nih tulisan gua kali ini untuk Install Certificate dan Install SSTP di Arch Linux. Semoga bermanfaat ya teman-teman.
Kalo yang bingung dan mau ditanya silahkan. InsyaaAllah akan dibalas secepatnya. Terima kasih.
Wassalamualaikum warahmatullahi wabaratuh.
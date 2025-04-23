# Day 3

## ✅ Task 1: Akses Server via Windows Terminal

Langkah-langkah:

- Pada server install openssh server dengan menggunakan command

```bash
sudo apt install openssh-server
```

![install](img/install.png)

- Apabila OpenSSH telah terinstall, lalu jalankan Windows Terminal sebagai administrator dan berikan command

```bash
ssh username@ip-server
```

> ip server bisa dilihat dengan menggunakan command "ip a" pada server

![ssh](img/ssh1.png)

> CTRL + D digunakan untuk keluar dari server yang dijalankan pada windows terminal
> ![ssh](img/ssh2.png)

---

## ✅ Task 2: Konfigurasi SSH dengan Public Key Only (Password Disabled)

Langkah-langkah:

- Generate SSH Key di Client:

```bash
ssh-keygen
```

![ssh](img/ssh-keygen.png)

- Input password dari file "key.pub" yang sudah digenerate kedalam file authorized keys pada direktori .ssh milik server

![ssh](img/authorized%20key.png)

- Apabila sudah maka client dapat mengakses server tanpa memasukkan password menggunakan file key yang dimilikinya dengan cara

```bash
ssh -i .ssh/key username@ip-server
```

![ssh](img/tanpapw.png)

- Untuk membuat agar client tanpa public key tidak bisa mengakses server, maka dapat konfigurasi pada file sshd_config (/etc/ssh/sshd_config) dan mengubah baris `PasswordAuthentication no` seperti pada gambar.

![ssh](img/sshd_config.png)

- Restart ssh server dengan menggunakan command

```bash
sudo systemctl restart ssh
```

![ssh](img/restart.png)

- Selesai, Client yang tidak memiliki Public Key tidak dapat me-remote server

![ssh](img/pwdisabled.png)

---

## ✅ Task 3: Text Manipulation (grep, sed, cat, echo)

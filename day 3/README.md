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

---
title: "Quiz PBKK A"
date: 2023-10-16T07:28:54+07:00
draft: false
---

Quiz ini menjadi bagian dari nilai evaluasi tengah semester (ETS).

## Pertanyaan

1. Jelaskan struktur framework , dan apa saja kegunaanya dalam pengembangan Perangkat Lunak?
2. Dalam pembuatan aplikasi, dikenal dengan Universal Windows Platform. Digunakan untuk membuat aplikasi yang mempunyai karakteristik seperti apa? Jelaskan sertai dengan contoh.
3. Untuk memperjelas jawaban no 2, Buatlah desain aplikasi Koleksi Album foto yang bisa menghimpun foto, deskripsi , informasi foto diambil/ metadata, dan juga bisa menghapus maupun update.
4. Implementasikan soal no 4, kemudian buat video tutorial pengerjaannya, upload di Youtube, dan embedded di blog dokumentasi.

Soal: https://fajarbaskoro.blogspot.com/2023/10/quiz-pbkk-kelas-senin.html

## Jawaban

### 1. Framework

Kegunaan dari framework dalam pengembangan perangkat lunak (PL) antara lain:
- Menyediakan struktur kode, baik dalam tata cara penulisan maupun struktur file dan folder dalam proyek, yang dapat dimengerti baik oleh aplikasi dalam lingkup pengembangan _(development environment)_ maupun para pengembang aplikasi itu sendiri _(the developers)_. Selain itu, biasanya framework memiliki konvensi tersendiri bagaimana menulis sebuah aplikasi agar bisa berjalan dengan optimal.
- Mempermudah proses dan meningkatkan kualitas pengembangan PL _(improve developer experience)_ dengan menyediakan kode siap pakai _(boilerplate)_ sehingga pengembang tidak perlu menulis ulang kode yang sama setiap kali memulai suatu proyek. Dengan ini, kualitas kode bisa tetap konsisten dan pengembang dapat menghemat waktu untuk membuat aplikasi. Alhasil, produk dapat diselesaikan dengan cepat dan berkualitas serta sesuai sengan kebutuhan klien/pengguna.
- Mempermudah pembuatan dokumentasi dan perawatan aplikasi berkat struktur kode yang teratur. Tiap bagian dalam aplikasi dapat diidentifikasi dengan mudah untuk dipahami dan diperbaiki jika terdapat masalah dalam aplikasi.
- Meningkatkan keamanan aplikasi. Dengan menggunakan framework yang sudah matang seperti Laravel, Next.js, atau Ruby on Rails, keamanan aplikasi telah dipertimbangkan oleh para pengembang framework tersebut sehingga keluaran aplikasi akan menjadi lebih aman. Tentunya, para pengembang aplikasi untuk pengguna _(end user)_ tetap harus mengikuti ketentuan keamanan sesuai yang disyaratkan oleh framework itu sendiri.

Beberapa framework memiliki struktur tertentu dalam pengembangannya. Misalnya, ASP.NET Core menggunakan arsitektur MVC (Model, View, Controller) untuk memisahkan struktur data, presentasi data kepada pengguna, dan alur bisnis. Mirip dengan MVC, terdapat pula MMMV (Model, View, ViewModel) yang digunakan oleh WPF dan Xamarin.

### 2. Universal Windows Platform

Universal Windows Platform (UWP) didesain oleh Microsoft untuk aplikasi yang akan diluncurkan di Microsoft Store sebagai platform resmi untuk mendapatkan aplikasi di Windows 10 ke atas. Beberapa karakteristik dari aplikasi UWP adalah:

- Antarmuka yang seragam sehingga navigasi dengan aplikasi yang berbeda terasa lebih mudah, tidak perlu mempelajari dari awal bagaimana membuka menu yang umum digunakan.
- Keamanan yang lebih terjaga karena aplikasi harus secara gamblang menyatakan apa yang ingin dipakai dan harus disetujui oleh tiap pengguna yang memakai, seperti kamera, mikrofon, dan lokasi.
- Penggunaan API yang diseragamkan sehingga dapat digunakan pada berbagai jenis Windows, seperti Windows Phone, 10, 10X, 11, dll.
- Instalasi yang mudah karena tidak meminta runtime tertentu untuk dipasang terlebih dahulu dalam sistem seperti DirectX 9 atau Java. Meskipun ada, seharusnya telah tercakup dalam aplikasi tersebut. Selain itu, dalam proses penghapusan (_uninstall_), semua data aplikasi terhapus dengan bersih dengan sisa yang minimal atau terhapus semua.
- Tampilan dan resolusi aplikasi yang dapat beradaptasi dengan segala jenis tampilan, seperti Hi-DPI dan layar ponsel.

Contoh aplikasi yang menggunakan UWP adalah WhatsApp (yang baru), Facebook Messenger, Telegram, Adobe Photoshop Express, berbagai aplikasi dari Microsoft, bahkan game seperti Age of Empires dan Asphalt 8.

### 3. Desain Album Foto

### 4. Implementasi Album Foto

Source code dapat dilihat di [repositori GitHub](https://github.com/return215/fwbp2023-midexam)

## Referensi

- Carr, Richard. (2015). WPF Controls - Window - Showing Dialog Boxes (Page 2 of 2). Blackwasp.co.uk. http://www.blackwasp.co.uk/WPFWindowShowDialog_2.aspx
- CodeDocu Developer C# Asp Net Angular. (2017). WPF Load Images as Thumbnails with faster Speed [YouTube Video]. In _YouTube_. https://www.youtube.com/watch?v=p4tH5-ufvBc
- Grech, Andreas. (2009, April 8). _WPF ListView: Attaching a double-click (on an item) event_. Stack Overflow. https://stackoverflow.com/questions/728205/wpf-listview-attaching-a-double-click-on-an-item-event
- Naik, Kishor. (2013). _WPF - Image Gallery in WPF_. Blogspot.com. https://kishor-naik-dotnet.blogspot.com/2011/05/wpf-image-gallery-in-wpf.html
- Stovell, Paul. (2013). WPF Navigation - Paul Stovell. Paul Stovell; Paul Stovell. https://web.archive.org/web/20130405072224/http://paulstovell.com/blog/wpf-navigation
- n.a. _Automatically resize a Window to fit content in WPF_. (2023). C-Sharpcorner.com. https://www.c-sharpcorner.com/Resources/894/automatically-resize-a-window-to-fit-content-in-wpf.aspx



---
layout: post
title : "Perkenalan Github page & Jekyll "
---

Pertemuan 2

<p>
    Pada praktikum ini, kami mempelajari cara membuat dan mengelola personal website menggunakan 
    <strong>Jekyll</strong> serta mempublikasikannya melalui <strong>GitHub Pages</strong>. 
    Adapun langkah-langkah utama dalam praktikum ini dimulai dengan membuat akun GitHub dan 
    repository yang sesuai dengan format <em>username.github.io</em>, kemudian mengkloning repository tersebut ke komputer lokal.
  </p>

  <p>
    Setelah repository berhasil dikloning, kami menginstal Jekyll beserta Bundler menggunakan perintah:
  </p>

  <pre><code>gem install jekyll bundler</code></pre>

  <p>
    Selanjutnya, kami menginisialisasi folder project dengan perintah:
  </p>

  <pre><code>bundle init</code></pre>

  <p>
    Setelah itu, file <code>Gemfile</code> yang dihasilkan diedit untuk menambahkan dependensi Jekyll. 
    Kami juga membuat file HTML sederhana berisi tag <code>&lt;h1&gt;Hello World!&lt;/h1&gt;</code> untuk pengujian awal.
    Setelah konfigurasi awal selesai, kami melakukan build project menggunakan:
  </p>

  <pre><code>jekyll build</code></pre>

  <p>
    Perintah tersebut menghasilkan direktori <code>_site</code> yang berisi file website statis. 
    Untuk menjalankan dan menguji web secara lokal, digunakan perintah:
  </p>

  <pre><code>jekyll serve</code></pre>

  <p>
    Web kemudian dapat diakses melalui <a href="http://localhost:4000">http://localhost:4000</a>. 
    Jika berjalan dengan baik, project kemudian dipush ke GitHub dengan perintah berikut:
  </p>

  <pre><code>
git add .
git commit -m "pub: first publish"
git push
  </code></pre>

  <p>
    Terakhir, untuk memudahkan deploy otomatis, kami diarahkan membuat <strong>GitHub Actions</strong> 
    sebagai bagian dari penerapan <strong>CI/CD</strong>.
  </p>

  <p>
    <strong>Catatan:</strong> Selama pengembangan, disarankan menjalankan Jekyll dengan opsi 
    <code>--livereload</code> agar setiap perubahan file langsung terlihat di browser. 
    Jika terjadi konflik port, gunakan opsi <code>--host</code> dan <code>--port</code> untuk menyesuaikan alamat lokal.
  </p>
# Membuat Latihan 2 Microservice 

## Download Project Maven
**Langkah 1 :** Pertama kali yang harus dilakukan yaitu membuat project Maven menggunakan Spring Initializr https://start.spring.io/
<br>**Langkah 2 :** Pilih **Project Maven** dan pilih bahasanya yaitu **Java**
<br>**Langkah 3 :** Lalu pilih Spring Boot versi **2.6.12**, pilih rilis yang terbaru (tetapi bukan snapshot) 
<br>**Langkah 4 :** Beri nama Grub pada Project sebagai contoh yaitu **com.oktavianipratiwi**
<br>**Langkah 5 :** Beri id Artefak yaitu **latihan-service** untuk bagian Name akan otomatis langsung terisi mengikuti id Artefak
<br>**Langkah 6 :** Beri Description pada project
<br>**Langkah 7 :** Pilih Java 17 atau sesuai dengan jdk yang ada pada Pc/Laptop
<br>**Langkah 8 :** Tambahkan Dependensi disebelah kanan atas yaitu **Spring Web**
<br>**Langkah 9 :** Tekan **Generate the project**. file zip akan terunduh, lalu ekstrak file tersebut
<br>**Langkah 10 :** Buka Netbeants lalu Import Project yang telah dibuat sebelumnya
<br>**Langkah 11 :** Lalu klik kanan pada Project, pilih **Build and Dependencies**
<br>**Langkah 12 :** Lalu Jalankan **LatihanServiceApplication**, jika berhasil makan akan keluar tampilan tulisan Spring. utk memulai Tomcat pada Port (s) 8080 (http)

## Membuat Project Spring Boot
**Langkah 1 :**
<br> Menggunakan **start.spring.io** untuk membuat proyek "web". Dalam dialog "Dependencies" cari dan tambahkan Dependencies "web" seperti yang ditunjukkan pada tangkapan layar. Tekan tombol "Generate", unduh zip, dan buka kemasannya ke dalam folder diPc.
<br>![image](https://user-images.githubusercontent.com/113502499/192421018-25a095d6-da28-41b2-a855-0ee6471e635e.png)

**Langkah 2 :**
<br> Buka proyek di IDE Anda dan cari **LatihanServiceAplication.java** di **Source Packages** pada folder **com.oktavianipratiwi.latihan2service**. Sekarang ubah isi file dengan menambahkan metode tambahan dan anotasi yang ditunjukkan pada kode di bawah ini. Anda dapat menyalin dan menempelkan kode atau cukup mengetiknya.
<br>![image](https://user-images.githubusercontent.com/113502499/192435718-e1c4ccd3-8f05-46f9-958a-efc50b79abf2.png)

<br>Metode hello() yang kami tambahkan dirancang untuk mengambil parameter String yang disebut name, dan kemudian menggabungkan parameter ini dengan kata **"Hello"** dalam kode. Ini berarti bahwa jika Anda menyetel nama Anda ke **“Latihan 2”** dalam permintaan, responsnya adalah **“Hello Latihan 2”**.
<br>Anotasi **@RestController** memberi tahu Spring bahwa kode ini menjelaskan titik akhir yang harus tersedia melalui web. Memberi **@GetMapping(“/hello”)** tahu Spring untuk menggunakan hello() metode kami untuk menjawab permintaan yang dikirim ke **http://localhost:8080/helloalamat**. Akhirnya, **@RequestParamSpring** memberi tahu Spring untuk mengharapkan name nilai dalam permintaan, tetapi jika tidak ada, itu akan menggunakan kata "Dunia" secara default.

**Langkah 3 :**
Pada project pergi ke **Other Sources >> src/main/resources >> default package >> application.properties.** Lalu buat *server.port= *nomorPort*

**Langkah 4 :**
<br>Buka browser Anda dan di bilah alamat di bagian atas enter http://localhost:8011/halo . Anda harus mendapatkan respons ramah yang bagus seperti ini:
<br>![image](https://user-images.githubusercontent.com/113502499/192455031-9d8fb45b-72c0-4f4f-b538-5c3404fafa6e.png)


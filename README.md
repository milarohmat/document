# Pendahuluan

> ANTARES merupakan sebuah Horizontal IoT Platform, yang berarti kami mencoba untuk menjadikan layanan kami se-umum mungkin agar solusi vertikal IoT anda dapat menyesuaikan dengan arsitektur yang umumnya digunakan. Banyak kasus-kasus IoT yang dapat dipecahkan dengan menggunakan layanan kami, contohnya adalah smart home, smart metering, asset tracking, smart building, dan lain-lain.

Dokumentasi ini akan menunjukkan anda cara untuk mengirim data sensor ke ANTARES. Ada 4 tahapan yang dapat ditempuh untuk mencapai hal tersebut:

Registrasi akun
Buat app
Tambahkan device
Pengiriman data ke Antares
Langkah-langkah yang lebih rinci dapat anda temukan setelah segmen ini. Jika terdapat informasi yang salah atau ada bagian dari tutorial ini yang tidak lengkap, jangan ragu untuk memberitahu kami pada email support@antares.id
# Registrasi Akun
Konsol ANTARES terdapat pada link berikut. Jika anda telah memiliki akun ANTARES, silahkan langsung login ke konsol. Jika belum, anda perlu melakukan registrasi agar dapat menggunakan layanan ANTARES. Ingin melakukan registrasi? silahkan kunjungi link berikut atau dengan klik tombol Register di halaman konsol. 

<img width="1280" alt="register1" src="https://user-images.githubusercontent.com/60457179/73623258-ef199700-466e-11ea-9f67-250828fc9fea.png">
Gambar 1. Antarmuka Halaman Login
<img width="1264" alt="register2" src="https://user-images.githubusercontent.com/60457179/73623492-ae6e4d80-466f-11ea-95ff-9b089c88261c.png">
Gambar 2. Antarmuka Halaman Registrasi

Setelah mengisi hal-hal yang diperlukan, kami akan mengirim anda email verifikasi. Harap untuk klik tautan yang terdapat pada email tersebut untuk melakukan verifikasi pada akun anda. Jika email verifikasi belum muncul pada email anda, anda bisa klik Resend Verification seperti pada gambar di bawah.

<img width="1279" alt="register3" src="https://user-images.githubusercontent.com/60457179/73419040-4ad2e000-4350-11ea-8eee-33bc0305515a.png">
Gambar 3. Antarmuka Kirim Ulang Verifikasi

Karena anda sudah membuat akun, anda bisa langsung masuk ke konsol ANTARES. Tampilannya akan seperti di bawah.

![getting-started-4](https://user-images.githubusercontent.com/60457179/73419063-5b835600-4350-11ea-91b0-7151315835e2.jpg)
Gambar 4. Antarmuka Konsol Pengguna

# Buat App
Sebelum membuat application, anda harus membangkitkan access key. Proses ini hanya dilakukan sekali jika anda merupakan pengguna baru ANTARES. Anda dapat menemukan pilihan ini dengan mengunjungi menu Account -> Access Key -> Get Access key. Access Key merupakan identitas akun anda. Harap simpan access key anda secara aman.
![getting-started-7](https://user-images.githubusercontent.com/60457179/73419091-75bd3400-4350-11ea-9197-5bf420430b9b.jpg)
Gambar 4. Antarmuka Mendapatkan Access Key

Setelah selesai, kita dapat membuat application. Kembali ke menu Application pada halaman dashboard, klik Create an Application. Anda akan masuk ke halaman berikut:
![getting-started-8](https://user-images.githubusercontent.com/60457179/73419103-81a8f600-4350-11ea-9d23-2763db6b1c41.jpg)
Gambar 5. Antarmuka Pembuatan Application

Silahkan isi dengan informasi yang diperlukan.
![getting-started-8](https://user-images.githubusercontent.com/60457179/73419146-a69d6900-4350-11ea-879f-f9b5671d4f16.jpg)
Gambar 6. Antarmuka Pembuatan Application

Selamat, anda telah membuat application pertama anda di ANTARES! Anda dapat menemukan application yang telah dibuat pada dashboard anda.

#3. Tambah Device ke Application
Internet of Things bersangkutan dengan benda-benda atau things. Pada segmen ini, kita akan membuat suatu device untuk tempat menaruh data.

Halaman di bawah akan muncul. Silahkan klik Add Device. Selain klik Add Device untuk menambahkan device, anda juga dapat membuat device dengan menggunakan RESTful API pada segmen HTTP API. Anda juga dapat melakukan subscription ke device, jadi jika ada data baru yang masuk ke device, anda akan mendapatkan notifikasi. Anda dapat memanfaatkan notifikasi tersebut untuk membuat logika pada program yang anda buat.
![getting-started-10](https://user-images.githubusercontent.com/60457179/73419161-b321c180-4350-11ea-9af6-78fabe6133dc.jpg)
Ambil nama untuk device anda. Dalam kasus ini, kami akan beri nama "SmartEye1"
![getting-started-11](https://user-images.githubusercontent.com/60457179/73419183-c03eb080-4350-11ea-9be9-edc23c34c079.jpg)
Setelah device berhasil dibuat, akan muncul di dashboard anda seperti berikut.
![getting-started-13](https://user-images.githubusercontent.com/60457179/73419197-d3ea1700-4350-11ea-9b61-6345ef60b82d.jpg)
Anda telah sukses membuat sebuah device. Ikuti langkah berikutnya untuk menaruh data pada device yang telah anda buat.
#4. Quickstart
Di bawah ini adalah beberapa contoh kode yang dapat anda gunakan untuk mengirim data dari proyek yang telah anda buat ke ANTARES.
<p>Di bawah ini adalah beberapa contoh kode yang dapat anda gunakan untuk mengirim data dari proyek yang telah anda buat ke ANTARES.</p>

                            <div>
                                <ul class="nav nav-outline nav-round">
                                    <li class="nav-item">
                                        <a class="nav-link active" data-toggle="tab" href="#quickstart-esp8266-http" style="padding: 2px 10px;">ESP8266(HTTP)</a>
                                    </li>
                                    <li class="nav-item">
                                        <a class="nav-link" data-toggle="tab" href="#quickstart-esp8266-mqtt" style="padding: 2px 10px;">ESP8266(MQTT)</a>
                                    </li>
                                    <li class="nav-item">
                                        <a class="nav-link" data-toggle="tab" href="#quickstart-nodejs" style="padding: 2px 10px;">NodeJS</a>
                                    </li>
                                    <li class="nav-item">
                                        <a class="nav-link" data-toggle="tab" href="#quickstart-python" style="padding: 2px 10px;">Python</a>
                                    </li>
                                </ul>
                            </div>

                            <div>
                                <div class="tab-content">
                                    <!-- esp code start -->
                                    <div class="tab-pane fade show active" id="quickstart-esp8266-http">
                                    Di bawah ini adalah video tutorial yang dapat anda gunakan untuk mengirim dan mendapatkan data dari ANTARES melalui ESP8266 (HTTP).<br/>
                                    Harap install <a href="https://github.com/antaresdocumentation/antares-esp8266-http" target="_blank">library ini</a> pada Arduino IDE. <br />
                                    <div style="display:flex;justify-content:center;margin:20px">
                                      <iframe width="100%" id="esp8266video" width="560" height="315" src="https://www.youtube.com/embed/Eg06Q1HsWdM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen>Your browser does not support this video.</iframe>
                                    </div>





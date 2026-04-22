1. Step by step saat user klik google.com di browser sampai halaman muncul
2. Perbedaan HTTP dan HTTPS, dan mengapa HTTPS lebih aman?
3. Apa maksud dari stateless pada HTTP
4. Menyebutkan 4 HTTP method dan kegunaannya
5. Arti dari HTTP status (200, 404, 500, 301)
6. Apa yang dikerjakan oleh DNS, dan analogikan dengan kehidupan sehari hari


1. Saat kita mengetik google.com dan melakukan enter yang terjadi adalah browser akan mengecek terlebih dahulu ke cache lokal, jika tidak ada maka DNS akan mengubah domain menjadi alamat IP, setelah itu browser akan melakukan HTTP request ke alamat ip yang dituju dan setelahnya server ip akan mengirimkan HTTP response yang berisi data yang diperlukan untuk memuat halaman google.

2. HTTPS adalah HTTP yang dienkripsi, mengapa ini lebih aman jika dibandingkan dengan HTTP? karena semisal kita berada pada jaringan publik, orang bisa mengakses data yang sedang kita gunakan, maka dengan enkripsi ini data tidak bisa terbaca oleh orang lain.

3. Stateless pada HTTP berarti antar HTTP request itu independen dan tidak berkaitan, jadi server tidak mengingat HTTP request yang sebelumnya dilakukan.

4. GET = untuk melakukan request ke server
   DELETE = menghapus data
   POST = mengirim data ke server
   PUT = menimpa data

5. 200 (sukses) = oke
   404 (kesalahan dari client) = resources yang diminta tidak ditemukan
   500 (kesalahan dari server) = ada kondisi tidak terduga yang ditemukan
   300 (redirect) = akan dipindahkan ke URL baru

6. DNS bisa disebut sebagai penerjemah yang menerjemahkan nama domain ke alamat ip, karena komputer sejatinya tidak bisa membaca huruf dia hanya bisa membaca angka dan kurang lebih dns bisa dianalogikan dengan buku telepon yang berisi nama (nama domain) dan nomor telepon (alamat ip)

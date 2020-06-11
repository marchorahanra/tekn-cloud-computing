# Penjelasan Hasil UAS TCC (Di ambil dari Materi pada praktikum minggu ke 10)


1. Pada bagian yang pertama ini akan menjalankan perintah utama untuk mengonfigurasi dan mengelola jaringan kontainer. Seperti pada gambar dibawah ini :<br/>

2. Kemudian selanjutnya menjalankan perintah untuk melihat jaringan kontainer yang ada pada host Docker saat ini. Seperti pada gambar dibawah ini :<br/>

3. Selanjutnnya menggunakan perintah untuk melihat detail konfigurasi dari kontainer jaringan pada docker host saya. Seperti pada gambar dibawah ini :<br/>

4. Menjalankan perintah untuk melihat daftar plugin jaringan. Seperti pada gambar dibawah ini :<br/>

5. Kemudian melihat jaringan penghubung pada daftar docker host kita saat ini, dengan menggunakan perintah seperti pada gambar dibawah ini :<br/>

6. Melakukan instalasi brctl yang nantinya digunakan untuk mendaftar bridges Linux di host Docker. Untuk langkah- langkah perintahnya seperti pada gambar dibawah ini :<br/>

kemudian setelah itu, menjalankan perintah untuk menampilakan brctl, apakah sudah terdapat bridges yang berjalan pada dcoker host kita, seperti pada gambar dibawah ini :<br/>

7. Kemudian menjalankan perintah untuk melihat detail bridges docker0 yang sedang berjalan ketika ditampilkan pada perintah sebelumnya, seperti pada gambar dibawah ini :<br>

8. Selanjutnya membuat container baru. Pembuatan container baru ini berguna untuk dapat terhubung ke jaringan bridges yang ada, untuk perintahnya seperti pada gambar dibawah ini :<br/>

9. Kemudian melihat container baru yang dibuat tadi, container baru ini bernama ubuntu:lates, yang merupakan image yang berkondisi sleep tetapi sedang berjalan, untuk perintah dan hasilnya seperti pada gambar dibawah ini :<br/>

10. Karena tidak ada jaringan yang ditentukan pada perintah docker run, kontainer secara otomatis akan ditambahkan ke jaringan bridge. Oleh karena itu perlu melihat lagi brctl kita. Seperti pada gambar dibawah ini :<br/>

dari hasil diatas bagaimana bridges docker0 sudah terhubung. Bagian ini menghubungkan bridges docker0 ke container baru yang baru saja dibuat.
11. Kemudian memeriksa ulang jaringan bridges, dengan perintah baru, seperti pada gambar dibawah ini :<br/>

12. Dari hasil sebelumnya dimana ip address yang didapatkan pada bridges kita yaitu 172.17.0.2.Selanjutnya kita akan mencoba ping ke ip address tersebut untuk memastikan apakah sedang berjalan atau tidak, seperti pada gambar dibawah ini :<br/>

13. Kemudian selanjutnya melihat ID bridges kita, untuk nantinya dapat menghungkan dengan URL lainnya, untuk perintah dan hasilnya seperti pada gambar dibawah ini :<br/>

dimana id kita yaitu 079ed538c950, id ini nantinya akan digunakan untuk menjalankan shell pada container ubuntu kita. Seperti pada gambar dibawah ini :<br/>

dimana dari gambar diatas juga sekaligus melakukan penginstalan program ping. Apabila sudah melakukan instalasi program ping makan selanjutnya kita mencoba ping ke url www.github.com. Untuk perintah dan hasilnya seperti pada gambar dibawah ini :<br/>

Kemudian selanjutnya keluar dari running container tersebut, dengan menggunakan perintah seperti pada gambar dibawah ini :<br/>

dari hasil pada gambar diatas juga lansung melakukan pemberentian untuk kontainer yang sedang berjalan dengan ID kita tadi, untuk perintahnya seperti gambar diatas tersebut.<br/>
14. Kemudian memulai kontainer baru dan sekaligus menjalankannya dimana kontainer ini bernama official NGINX. Dimana image ini berjalan pada web server pada port 80. Untuk perintah dan hasilnya seperti pada gambar dibawah ini :<br/>

15. Kemudian melakukan cek status container dan port yang sedang berjalan, dari hasil start sebelumnya. Untuk perintah dan hasilnya seperti pada gambar dibawah ini :<br/>

16. Menghungkan host docker kita dengan port 80, apabila tidak dapat membukanya pada web browser. Untuk perintah dan hasilnya seperti gambar dibawah ini :<br/>

17. Kemudian selanjutnya inisialisasi swarm baru. Untuk perintah dan hasilnya seperti pada gambar dibawah ini :<br/>

18. Kemudian menjalankan perintah untuk melihat node swarm yang sedang berjalan, seperti pada gambar dibawah ini :<br/>

19. Kemudian membuat overlay jaringan dengan nama overnet. Untuk perintah dan hasilnya seperti pada gambar dibawah ini :<br/>

20. Menjalankan perintah untuk memastikan bahwa jaringan berhasil dibuat. Untuk perintah dan hasilnya seperti pada gambar dibawah ini :<br/>

21. Kemudian melihat kembali daftar jaringan pada docker host kita. Untuk perintah dan hasilnya seperti pada gambar dibawah ini :<br/>

22. Selanjutnya melihat detail informasi dari jaringan overnet. Untuk perintah dan hasilnya seperti pada gambar dibawah ini :<br/>

23. Kemudian membuat layanan baru dengan nama myservice pada jaringan overnet dengan dua bagian. Untuk perintah dan hasilnya seperti pada gambar dibawah ini :<br/>

24. Selanjutnya memastikan bahwa layanan yang dibuat dengan dua bagian sudah aktif. Untuk perintah dan hasilnya seperti pada gambar dibawah ini :<br/>

25. Selanjutnya memastikan bahwa dua node sedang berjalan. Untuk perintah dan hasilnya seperti pada gambar dibawah ini :<br/>

26. Selanjutnya melakukan verifikasi jaringan dua bagian node yang sedang berjalan pada jaringan overnet. Untuk perintah dan hasilnya seperti pada gambar dibawah ini :<br/>

27. Melihat detail jaringan overnet dan mendapatkan alamat ip dari running dua node yang ada. Untuk perintah dan hasilnya seperti pada gambar dibawah ini :<br/>

28. Melihat konfigurasi jaringan myservice. Untuk perintah dan hasilnya seperti pada gambar dibawah ini :<br/>

29. Melakukan remove layanan myservice. Untuk perintah dan hasilnya seperti pada gambar dibawah ini :<br/>

30. Kemudian melihat kembali list jaringan container yang ada. Untuk perintah dan hasilnya seperti pada gambar dibawah ini :<br/>

31. Kemudian yang terakhir menghapus node 1 dan 2 yang berjalan pada swarm. Untuk perintah dan hasilnya seperti pada gambar dibawah ini 





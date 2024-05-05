# Module 10 - Reflection
> Fathan Naufal Adhitama - 2206825965 - Pemrograman Lanjut A

## 1.2 Understanding how it works
![Image 1.2](images/timer.png)
Pada gambar di atas, terlihat bahwa output 'bonjour!' diprint lebih dulu daripada 'howdy!' dan 'done!'. Ini terjadi karena perintah print untuk 'howdy' dan 'done' terdapat didalam sebuah task yang di-spawn menggunakan `spawner.spawn(async { ... }),` di mana perintah tersebut akan dijalankan secara asinkronus setelah `executor.run()` dijalankan. Sementara itu, perintah print 'bonjour!' berada di main thread yang akan dieksekusi tanpa menunggu perintah executor.run(). Oleh karena proses tersebutlah, output di atas dapat dihasilkan.
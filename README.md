# PERTEMUAN 13

Nama : Rafi Suswidia
Nim  : 312210331
Kelas: TI.22B2


Pengertian
Pada python, ada dua fitur yang sangat penting untuk menangani kesalahan tidak terduga di dalam program dan juga menambah kemampuan debugging di dalamnya.

Exception Handling - adalah suatu mekanisme pada python yang bertujuan untuk menangani sebuah error pada program. Error ini nantinya akan menghentikan program yang dijalankan dengan cara yang tidak normal.
Assertion - pemeriksaan kewajaran yang dapat di aktifkan atau nonaktifkan setelah kita menyelesaikan uji pada program.

@Assertion Statement

Saat menemukan pernyataan, Python mengevaluasi ekspresi yang menyertainya, yang mana diharapkan semoga benar. Jika ekspresi salah, Python memunculkan pengecualian AssertionError. Syntax untuk assert itu adalah : assert Expression[, Arguments] Jika pernyataan gagal, Python menggunakan ArgumentExpression sebagai argumen untuk AssertionError. AssertionError exceptions dapat ditangkap dan ditangani seperti pengecualian lainnya menggunakan try-except statement, tetapi jika dibiarkan, mereka akan menghentikan program dan menghasilkan backtrace.


#Contoh

Berikut adalah fungsi yang mengubah suhu dari derajat Kelvin menjadi derajat Fahrenheit. Karena nol derajat Kelvin sedingin itu, fungsinya akan keluar jika melihat sebuah suhu negatif

![image](https://user-images.githubusercontent.com/115480539/213115924-dd1f750f-82f4-4c44-b322-e50ab10bdf8d.png)


Ketika kode di atas dijalankan, menghasilkan hasil sebagai berikut -

![image](https://user-images.githubusercontent.com/115480539/213115993-35a24660-6f34-4fee-9c67-ad33210e362a.png)


#Menangani Sebuah Pengecualian

Jika kita memiliki beberapa kode mencurigakan yang bisa memunculkan sebuah pengecualian, kita bisa mempertahankan programnya. Caranya adalah dengan menempatkan kode mencurigakan itu didalam sebuah try:block. Setelah try:block, masukkan sebuah except:statement, dibarengi dengan sebuah block kode yang menangani masalah itu dengan se-sempurna mungkin.

#Syntak

Ini adalah sebuah syntax sederhana dari try...except...else blocks

try:
    Opetasi dilakukan disini;
   ......................
except ExceptionI:
   Jika disini adalah pengecualian1, maka blok ini akan dieksekusi.
except ExceptionII:
   Jika disini adalah pengecualian2, maka blok ini akan dieksekusi.
   ......................
else:
   Jika sama sekali tidak ada pengecualian blok ini yang akan dieksekusi.
   
   Berikut adalah beberapa poin penting tentang sintaks yang disebutkan di atas -

Pernyataan try tunggal dapat memiliki beberapa pernyataan kecuali. pernyataan. Ini berguna saat mencoba blok berisi pernyataan yang mungkin melempar berbagai jenis pengecualian.

Anda juga dapat memberikan klausa kecuali umum, yang menangani pengecualian apa pun.

Setelah klausa kecuali, klausa, Anda dapat menyertakan sertakan klausa lain. lain-klausa. Kode di blok-lain-lain-blok dijalankan jika kode di try: block tidak memunculkan eksepsi.

Blok else adalah tempat yang bagus untuk kode yang tidak memerlukan perlindungan blok try:.

Contoh
Dicontoh ini akan membuka file, lalu menulis ini file, dan akan keluar dengan normal karena tidak ada masalah didalamnya.

![image](https://user-images.githubusercontent.com/115480539/213116344-9c3ef6b1-ee02-4fff-8da6-6c8e59df34db.png)


#Ini menghasilkan hasil berikut -

![image](https://user-images.githubusercontent.com/115480539/213116470-3c30d0bb-9ae7-4265-b152-e817f722746e.png)


Contoh
Dicontoh ini akan mencoba membuka sebuah file dimana kita tidak mempunyai izin untuk menulis, jadi nantinya akan memunculkan sebuah pengecualian. 

![image](https://user-images.githubusercontent.com/115480539/213116555-50ef0d86-0eba-4705-b29e-4461727b21d3.png)



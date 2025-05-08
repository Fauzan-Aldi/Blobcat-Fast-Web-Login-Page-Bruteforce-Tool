# Blobcat-Fast-Web-Login-Page-Bruteforce-Tool

## Deskripsi

Blobcat adalah alat brute-force yang dirancang untuk menguji halaman login web dengan cepat. Alat ini dibangun menggunakan Python dan memanfaatkan pustaka `requests` untuk mengirimkan permintaan HTTP secara paralel menggunakan multithreading.

## Fitur

* **Multithreading**: Meningkatkan kecepatan brute-forcing dengan pemrosesan paralel.
* **Random User-Agent**: Menggunakan user-agent acak untuk menyamarkan permintaan.
* **Dukungan untuk `x-www-form-urlencoded` dan `JSON`**: Memungkinkan pengiriman data dalam berbagai format konten.
* **Dukungan untuk protokol `http` dan `https`**: Kompatibel dengan kedua protokol ini.

## Penggunaan Sederhana

```bash
python3 main.py --url URL --data DATA --wordlist WORDLIST --expected EXPECTED

# Contoh
python3 main.py --url http://example.com/login --data "username=admin&password=*" --wordlist wordlist.txt --expected "Invalid username or password"
```

## Opsi

* `--url` - URL halaman login yang akan diuji.
* `--data` - Data POST yang akan dikirimkan ke halaman login. Gunakan karakter `*` untuk menggantikan nilai dari wordlist.
* `--ctype` - Jenis konten data POST. Pilih `0` untuk `x-www-form-urlencoded` dan `1` untuk `JSON`.
* `--wordlist` - Lokasi file wordlist yang digunakan.
* `--expected` - Respons yang diharapkan ketika login gagal.
* `--threads` - Jumlah thread yang digunakan untuk proses brute-force.
* `--random-agent` - Mengaktifkan penggunaan user-agent acak untuk setiap permintaan.

## Kontribusi

Pull request diterima. Untuk perubahan besar, harap buka isu terlebih dahulu untuk mendiskusikan perubahan yang diinginkan.

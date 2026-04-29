Eksploitasi SQL Injection (Lampiran A)Bagian ini mendokumentasikan bagaimana sebuah celah keamanan pada form login dapat dieksploitasi:Form Login Awal: Halaman login standar aplikasi uji.  Input Payload: Memasukkan payload ' OR '1'='1 ke dalam kolom username untuk memanipulasi logika query SQL .  Login Bypass: Menunjukkan hasil login yang berhasil menembus autentikasi meskipun menggunakan kredensial yang salah.  Query Analysis: Tampilan dari sisi database (phpMyAdmin) yang memperlihatkan bagaimana query berubah menjadi selalu bernilai TRUE akibat injeksi tersebut . 
<img width="933" height="161" alt="image" src="https://github.com/user-attachments/assets/a8fc39a8-5fb7-49e9-91e5-a59d79f3a9db" />

Eksploitasi Cross-Site Scripting / XSS (Lampiran B)Mendokumentasikan kerentanan Stored XSS pada fitur komentar:Payload Injection: Memasukkan skrip JavaScript <script>alert('XSS')</script> ke dalam form komentar .  Storage: Menunjukkan bahwa skrip tersebut tersimpan secara permanen di database karena tidak adanya sanitasi input .  Execution: Bukti bahwa browser mengeksekusi skrip berbahaya tersebut (muncul popup alert) saat halaman diakses oleh pengguna . 
<img width="556" height="139" alt="image" src="https://github.com/user-attachments/assets/50be9682-300e-4867-888d-143f54079f00" />

Mitigasi dan Hasil Akhir (Lampiran C & F)Bagian ini menunjukkan langkah perbaikan yang diambil:Countermeasures: Implementasi Prepared Statements untuk SQL Injection dan Output Encoding (htmlspecialchars) untuk mencegah XSS .  Verification: Setelah mitigasi diterapkan, serangan dengan payload yang sama dinyatakan gagal.  Hasil Cek Plagiasi: Menunjukkan skor orisinalitas sebesar 18%, yang berarti artikel ini memenuhi syarat orisinalitas tugas (maksimal 30%). <img width="368" height="146" alt="image" src="https://github.com/user-attachments/assets/3d8f67fb-bbc1-4e2a-bc5a-308c3c3074a9" />
<img width="1600" height="838" alt="image" src="https://github.com/user-attachments/assets/0f6c0fee-ab65-461f-b398-31f57ce5fd87" />




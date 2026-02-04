### A. SPA
Jelaskan apa itu SPA (Single Page Application) dan bagaimana SPA berbeda dari aplikasi web tradisional? Sebutkan juga beberapa keuntungan dan kerugian menggunakan SPA dalam pengembangan web.  
Jawab :  
__SPA (Single Page Application)__ merupakan sebuah konsep aplikasi web yang memiliki satu halaman saja. Pada web biasa atau multi page jika kita melakukan navigasi kehalaman lain, maka browser akan memuat ulang seluruh halaman setelah melakukan request ke server. Berbeda dengan web SPA, ketika berpindah ke halaman lain, maka javascript akan melakukan fetching ke server dan mengganti tampilan ke navigasi lain tanpa perlu browser memuat ulang seluruh halaman.  
Web SPA memiliki keuntungan yaitu waktu navigasi antar halaman lebih singkat serta front-end yang cepat dan responsif. Sementara itu kelemahan dari web SPA adalah karena menggunakan client-side routing, yang dapat membuat maka rentannya terkena serangan seperti Cross-Site Scripting (XSS).

### B. Service dalam Backend
Jawab :  Service dalam Backend memungkinkan developer mengalihkan aspek-aspek perhitungan dan layanan di balik layar atau di backend sehingga lebih mudah fokus pada pengembangan frontend dan peningkatan *user experience*.  
Service membantu modularitas WebDev karena memisahkan logika dari lapisan lain seperti akses database dan route/controller. Dengan service, setiap bagian punya tugas yang jelas. Contohnya route hanya menangani request dan response, sementara itu service fokus pada aturan dan proses pada aplikasi/web. 


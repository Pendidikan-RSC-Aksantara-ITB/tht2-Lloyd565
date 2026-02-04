## Path Planning dan Swarm Control
### A. Penjelasan
a. Jelaskan konsep dasar dari Artificial Potential Field (APF) dalam konteks navigasi robot. Sertakan penjelasan tentang bagaimana gaya tarik dan tolak bekerja dalam metode ini dan sertakan ilustrasi atau diagram yang digambar sendiri di kertas atau papan tulis digital.  
b. Jelaskan perbedaan antara Uniform Cost Search (UCS), Greedy Best First Search (GBFS), dan A* Search dalam konteks algoritma pencarian jalur. Sertakan kelebihan dan kekurangan masing-masing algoritma serta situasi di mana masing-masing algoritma lebih cocok digunakan.  

Jawab :  
a. Artificial Potential Field pada robot merupakan algoritma untuk navigasi robot dengan menghasilkan gaya tarik dan tolak dari berbagai titik di sekitar robot. Titik-titik yang menghasilkan gaya tarik secara aktif menarik UAV ke arah mereka. Namun, titik-titik yang menghasilkan gaya tolak, UAV akan ditolak dari mereka. Gaya tarik dan tolak ini dihasilkan dari perbedaan muatan yang ada pada rintangan maupun tujuan. Menggunakan hukum Couloumb, rintangan dan robot dibuat memiliki muatan yang sama agar menghindari adanya _crash_. Sementara itu tujuan akhir akan bermuatan yang berlawanan dengan robot agar tertarik menuju tujuan tersebut. Dengan cara ini, UAV akan menemukan jalur ke tujuannya tanpa menabrak hambatan.  
Sumber : [APF](https://www.sciencedirect.com/topics/computer-science/artificial-potential-field)  

b.  
- Uniform Cost Search, merupakan algoritma pencarian jalur yang menggunakan jarak kumulatif terendah pada graf berbobot. UCS pakai [priority queue](https://www.geeksforgeeks.org/dsa/priority-queue-set-1-introduction/) untuk menyimpan node yang dilalui, node dengan jarak yang terendah akan dihapus dari priority queue dan node tersebut akan di ekspansi yang kemudian pencarian dilanjut dengan menelusuri tetangga node tersebut. Untuk setiap tetangga dari node yang diperluas, algoritma menghitung biaya total dari node awal ke tetangga melalui node saat ini. Jika node tetangga tidak ada dalam priority queue, node tersebut ditambahkan ke antrian dengan biaya yang dihitung. Jika node tetangga sudah ada dalam antrian tetapi ditemukan jalur dengan biaya lebih rendah ke node tetangga tersebut, biaya dalam antrian diperbarui. UCS ini cocok dipakai saat tidak ada info tentang heuristik kasusnya, butuh jaminan jalur tersingkat.  
- Greedy Best First Search bekerja dengan cara menghitung jarak semua node tetangga, lalu mengekspansinya dengan node tersebut sampai ditemukan tujuan akhir. Cocok saat dibutuhkan solusi yang cepat, masalah relatif sederhana.  
- A* bekerja dengan menghitung value dari parameter yang sudah ditentukan. A* cocok jika diperlukan kecepatan dan ketepatan dalam pencarian jalur tersingkat. Algoritma A* menentukan langkah dengan melakukan perhitungan dari value f, g, dan h yang dijelaskan sebagai berikut :
  1. f = Nilai pada tiap kotak yang nantinya menentukan kemana arah gerak selanjutnya. Disini f adalah penjumlahan antara g dan h
  2. g = Jarak dari titik asal ke kotak tertentu
  3. h = perkiraan jarak dari "titik yang terdekat dengan titik asal" dengan titik tujuan. Nilai h ini merupakan heuristik yang memiliki banyak cara untuk dihitung.  

### B. Implementasi
soon
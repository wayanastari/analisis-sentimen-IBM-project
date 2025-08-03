Comparative Sentiment Analysis: Wondr by BNI vs BNI Mobile Banking
📌 Project Overview
PT Bank Negara Indonesia (BNI) merilis aplikasi Wondr by BNI sebagai pengganti resmi dari BNI Mobile Banking dalam rangka meningkatkan kualitas layanan digital banking. Peralihan ini bertujuan untuk menghadirkan antarmuka yang lebih modern, fitur yang lebih lengkap, dan performa yang lebih optimal.
Namun, setiap transisi teknologi besar kerap menghadirkan tantangan, khususnya dari sisi penerimaan pengguna. Melalui proyek ini, dilakukan analisis terhadap ribuan ulasan pengguna dari Google Play Store guna membandingkan persepsi, sentimen, serta topik yang paling sering muncul pada kedua aplikasi. Proyek ini menggunakan pendekatan data-driven berbasis Natural Language Processing (NLP) dan Large Language Model (LLM) untuk memperoleh insight yang mendalam.
📁 Raw Dataset Link
Dataset diperoleh melalui proses scraping Google Play Store menggunakan Apify, terdiri dari 3000 ulasan untuk masing-masing aplikasi.
https://drive.google.com/drive/folders/1zcCHpufx0O62ID7YrvwxpuqqghpRO79z?usp=sharing 

📊 Insight & Findings
Distribusi Sentimen:
Aplikasi	Positif (%)	Negatif (%)	Netral (%)
Wondr by BNI	30.44%	68.89%	0.67%
BNI Mobile Banking	5.87%	93.70%	0.40%
•	Wondr by BNI memiliki sentimen positif yang jauh lebih tinggi dibandingkan BNI Mobile Banking.
•	Sentimen negatif masih mendominasi pada kedua aplikasi, terutama terkait kendala teknis.
•	Sentimen netral sangat kecil, menunjukkan bahwa pengguna cenderung memiliki opini yang kuat terhadap aplikasi.

Temuan Topik Berdasarkan Word Cloud:
Wondr by BNI:
•	Sentimen Negatif: login gagal, verifikasi wajah, transaksi error, sistem lambat.
•	Sentimen Positif: aplikasi mudah digunakan, transaksi cepat, fitur lengkap.
•	Sentimen Netral: deskripsi fitur, penggunaan kartu dan saldo.
BNI Mobile Banking:
•	Sentimen Negatif: gagal login, koneksi terputus, update menyebabkan error.
•	Sentimen Positif: transaksi lancar, aktivasi mudah.
•	Sentimen Netral: pembaruan sistem, konektivitas, deskripsi fitur.

🤖 AI Support Explanation
Proses klasifikasi sentimen dilakukan menggunakan model LLM ibm-granite/granite-3.3-8b-instruct melalui layanan API Replicate.
Tahapan:
1.	Data Preparation:
o	Penggabungan dua dataset (Wondr dan BNI Mobile)
o	Pembersihan data (menghapus simbol, angka, URL)
2.	Prompting dan Klasifikasi:
o	Setiap review diklasifikasikan ke dalam tiga kategori: Positif, Negatif, dan Netral
o	Output disimpan dalam bentuk CSV untuk dianalisis lebih lanjut

✅ Conclusion & Recommendation
Kesimpulan:
•	Wondr by BNI memberikan pengalaman pengguna yang relatif lebih baik dibandingkan BNI Mobile Banking, terutama dalam hal desain dan fitur.
•	Masalah teknis seperti login, OTP, dan error sistem masih menjadi tantangan utama pada kedua aplikasi.
•	Pengguna menyambut baik fitur-fitur baru, tetapi stabilitas sistem masih menjadi prioritas utama yang harus dibenahi.
Rekomendasi:
1.	Tingkatkan stabilitas sistem pada proses login dan transaksi.
2.	Lakukan pengujian yang lebih ketat sebelum update aplikasi.
3.	Perkuat komunikasi fitur kepada pengguna melalui onboarding dan edukasi.
4.	Tambahkan kanal umpan balik langsung di dalam aplikasi untuk menampung keluhan pengguna secara real-time.


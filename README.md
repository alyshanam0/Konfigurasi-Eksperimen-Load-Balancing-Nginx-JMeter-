# Konfigurasi-Eksperimen-Load-Balancing-Nginx-JMeter-
Repositori ini berisi konfigurasi Nginx dan skrip Apache JMeter yang digunakan dalam eksperimen evaluasi performa algoritma load balancing pada arsitektur microservice di lingkungan cloud.  Repositori disediakan untuk mendukung reprodusibilitas eksperimen.

---

# Konfigurasi Nginx
Direktori nginx/ berisi konfigurasi load balancing menggunakan:
- Round Robin
- IP Hash
- Random

Konfigurasi digunakan sebagai reverse proxy untuk mendistribusikan request HTTP ke beberapa backend service.

---

# Skrip Apache JMeter
Direktori jmeter/ berisi file:

Test.jmx

Skrip ini digunakan untuk melakukan load test dan stress test dengan pengaturan utama:
- Metode: HTTP GET
- Target: frontend layanan microservice
- Parameter beban: jumlah thread (virtual users), ramp-up time, dan loop count disesuaikan dengan skenario pengujian
- Metrik yang diambil: throughput, latency p95, dan error rate.

---

# Catatan
Workload dan konfigurasi dijaga konsisten antar skenario pengujian.
Detail lingkungan cloud dan spesifikasi instance dijelaskan dalam naskah utama.

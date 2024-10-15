Garda Sudarmanto
5025221268
Tugas Pertemuan 5 KPPL

Mendefinisikan requirement dan model desain untuk aplikasi **Tech Support System** memerlukan pemahaman tentang kebutuhan pengguna, fungsionalitas yang diperlukan, dan desain yang mendukung alur kerja yang efisien.

### 1. **Requirement**

#### **Functional Requirement:**
- **User Management:**
  - Admin dapat membuat, mengedit, menghapus, dan mengelola pengguna (customer dan support agents).
  - Autentikasi pengguna dengan login dan logout menggunakan sistem peran (admin, support agent, customer).
  
- **Ticket Management:**
  - Pengguna (customer) dapat membuat ticket baru yang berisi deskripsi masalah.
  - Setiap ticket memiliki status (open, in progress, resolved, closed).
  - Sistem memungkinkan pengelompokan ticket berdasarkan prioritas (low, medium, high).
  - Agent support dapat menerima dan menangani ticket, memberikan update, dan menutup ticket.

- **Notification System:**
  - Pengguna mendapatkan notifikasi saat ada pembaruan status pada ticket.
  - Agent support mendapatkan notifikasi untuk ticket baru yang belum ditangani.

- **Knowledge Base:**
  - Admin dan agent dapat menambah artikel atau solusi ke dalam sistem knowledge base.
  - Customer bisa mencari dan mengakses artikel di knowledge base untuk solusi mandiri sebelum membuat ticket.
  
- **Chat System (Optional):**
  - Customer dapat berkomunikasi langsung dengan agent melalui chat untuk menyelesaikan masalah secara real-time.

- **Reporting:**
  - Admin dapat melihat laporan tentang kinerja agent, jumlah ticket, dan status ticket.
  - Dashboard untuk statistik dan metrik, seperti waktu rata-rata penyelesaian ticket, jumlah ticket per agent, dsb.

#### **Non-functional Requirement:**
- **Performance:**
  - Aplikasi harus mampu menangani sejumlah besar ticket tanpa mengalami penurunan performa.
  
- **Scalability:**
  - Sistem harus mudah diperluas untuk mendukung lebih banyak agent dan customer saat bisnis berkembang.

- **Security:**
  - Harus ada enkripsi data untuk melindungi informasi pribadi.
  - Autentikasi yang aman untuk mencegah akses yang tidak sah.

- **Usability:**
  - Antarmuka pengguna harus mudah digunakan oleh customer non-teknis dan support agent.
  
- **Availability:**
  - Sistem harus memiliki uptime yang tinggi, dengan rencana backup dan recovery untuk menjaga ketersediaan layanan.

---

### 2. **Model Desain**

#### **User Interface (UI):**
- **Customer Dashboard:**
  - Halaman beranda untuk customer menampilkan ticket yang pernah dibuat, statusnya, dan tombol untuk membuat ticket baru.
  - Form untuk membuat ticket baru dengan input untuk masalah, kategori, dan prioritas.
  - Integrasi knowledge base dengan fitur pencarian di dashboard.

- **Agent Dashboard:**
  - Halaman untuk agent menampilkan ticket yang harus ditangani dan tombol untuk melihat semua ticket.
  - Filter dan sorting ticket berdasarkan prioritas, status, atau waktu dibuat.
  - Halaman detail ticket dengan fitur update status, menambahkan komentar, dan opsi untuk menutup ticket.

- **Admin Dashboard:**
  - Halaman kontrol yang memungkinkan admin mengelola pengguna, melihat laporan, dan membuat artikel knowledge base.
  - Tampilan statistik dan metrik kinerja agent dan penyelesaian ticket.

#### **Backend System Design:**
- **Database Structure:**
  - **Users Table:** Menyimpan informasi pengguna (username, password, role).
  - **Tickets Table:** Menyimpan informasi ticket, seperti ID, deskripsi, status, prioritas, tanggal dibuat, dan pemilik.
  - **Knowledge Base Table:** Menyimpan artikel yang berisi solusi untuk masalah umum.
  - **Comments Table:** Menyimpan komentar yang ditambahkan oleh agent ke setiap ticket.

- **Workflow:**
  - Customer mengirimkan ticket → Ticket masuk ke dashboard agent → Agent mengambil dan menangani ticket → Agent memberi solusi dan mengubah status ticket.
  
- **API Design:**
  - REST API untuk integrasi dengan aplikasi mobile atau platform lain.
  - API endpoint untuk CRUD (Create, Read, Update, Delete) pada ticket, user, dan knowledge base.

- **Notification System:**
  - Menggunakan push notification atau email untuk notifikasi perubahan status pada ticket.

#### **Technology Stack:**
- **Frontend:**
  - HTML/CSS/JavaScript untuk web interface.
  - Framework seperti React atau Vue.js untuk membangun UI yang interaktif.

- **Backend:**
  - Node.js dengan Express untuk membangun REST API.
  - Atau, Python dengan Django/Flask.
  
- **Database:**
  - MySQL/PostgreSQL untuk penyimpanan data terstruktur.
  
- **Notification Service:**
  - Menggunakan Firebase Cloud Messaging (FCM) atau email service seperti SendGrid untuk notifikasi.

- **Deployment:**
  - Deploy ke cloud platform seperti AWS atau Heroku, dengan containerization menggunakan Docker untuk skalabilitas.

Dengan mendefinisikan requirement dan model desain ini, aplikasi **Tech Support System** akan siap mendukung layanan pelanggan dan penyelesaian masalah dengan efisien.

Untuk membuat model proses Waterfall menjadi lebih sederhana, kita bisa merangkum setiap fase dengan fokus pada poin-poin utama:

### 1. **Requirement Gathering (Pengumpulan Kebutuhan)**
- Kumpulkan kebutuhan dari pengguna (admin, customer, agent support).
- Buat daftar fitur yang diinginkan, seperti pembuatan ticket, notifikasi, dan knowledge base.

**Output:** Dokumen kebutuhan.

---

### 2. **System Design (Desain Sistem)**
- Buat rencana desain aplikasi, termasuk struktur database dan tampilan antarmuka (UI).
- Tentukan alur kerja utama untuk ticket management dan user management.

**Output:** Skema desain dan mockup UI.

---

### 3. **Implementation (Implementasi)**
- Bangun aplikasi berdasarkan desain yang sudah ada.
- Kembangkan frontend (antarmuka pengguna) dan backend (logika bisnis, API).
- Buat dan hubungkan database dengan sistem.

**Output:** Aplikasi yang bisa digunakan.

---

### 4. **Testing (Pengujian)**
- Uji aplikasi untuk memastikan semua fitur bekerja sesuai kebutuhan.
- Perbaiki bug atau error yang ditemukan.

**Output:** Aplikasi yang stabil dan bebas bug.

---

### 5. **Deployment (Peluncuran)**
- Pasang aplikasi di server yang akan digunakan.
- Lakukan uji coba terakhir di lingkungan produksi.

**Output:** Aplikasi yang siap digunakan oleh pengguna.

---

### 6. **Maintenance (Pemeliharaan)**
- Perbaiki bug yang muncul setelah peluncuran.
- Tambahkan fitur baru jika diperlukan.

**Output:** Aplikasi terus berjalan dengan baik.

---

### Diagram Proses Waterfall (Sederhana)

```mermaid
graph TD
  A[Requirement Gathering] --> B[System Design]
  B --> C[Implementation]
  C --> D[Testing]
  D --> E[Deployment]
  E --> F[Maintenance]
```

Dengan penyederhanaan ini, setiap tahap dalam proses Waterfall menjadi lebih mudah dipahami dan diikuti, tanpa kehilangan esensi dari proses pengembangan aplikasi.

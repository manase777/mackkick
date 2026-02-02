# 👟 Sepatu Ku - Aplikasi Toko Sepatu

Aplikasi toko sepatu online yang dibangun dengan **Ionic** dan **Angular**, fitur lengkap dengan sistem login, katalog produk, keranjang belanja, dan checkout.

## 🎯 Fitur Utama

### 1. **Autentikasi (Login & Register)**
   - ✅ Login dengan email dan password
   - ✅ Registrasi akun baru
   - ✅ Validasi form
   - ✅ Akun demo untuk testing
   - ✅ Persistent user session (localStorage)

### 2. **Toko & Katalog Produk**
   - ✅ Tampilkan daftar sepatu dengan grid layout
   - ✅ Fitur pencarian produk
   - ✅ Informasi produk lengkap (harga, rating, stok)
   - ✅ Badge stok terbatas
   - ✅ Responsive design

### 3. **Detail Produk**
   - ✅ Tampilan detail produk lengkap
   - ✅ Galeri gambar
   - ✅ Rating dan reviews
   - ✅ Pilihan ukuran sepatu
   - ✅ Pilihan warna
   - ✅ Pengaturan jumlah kuantitas
   - ✅ Tombol "Tambah ke Keranjang"

### 4. **Keranjang Belanja**
   - ✅ Lihat semua item di keranjang
   - ✅ Update jumlah item
   - ✅ Hapus item dari keranjang
   - ✅ Hitung total harga otomatis
   - ✅ Swipe untuk delete item
   - ✅ Checkout sederhana

### 5. **User Experience**
   - ✅ Logout dari aplikasi
   - ✅ Toast notification
   - ✅ Loading state
   - ✅ Error handling
   - ✅ Responsive UI untuk mobile & tablet

---

## 📱 Screen/Halaman Aplikasi

### 1. **Login Page** (`/login`)
- Form login dengan email & password
- Tab untuk register akun baru
- Akun demo untuk testing
- Validasi form

### 2. **Shop Page** (`/tabs/shop`)
- Grid list produk sepatu
- Searchbar untuk cari produk
- Kartu produk dengan info dasar
- Logout button di header
- Badge keranjang dengan jumlah item

### 3. **Product Detail Page** (`/tabs/product-detail/:id`)
- Gambar produk besar
- Info lengkap (nama, harga, deskripsi)
- Rating & reviews
- Pilihan ukuran & warna
- Kontrol kuantitas
- Tombol checkout & view cart

### 4. **Cart Page** (`/tabs/cart`)
- Daftar item di keranjang
- Update kuantitas per item
- Hapus item
- Summary harga (subtotal, ongkir, diskon)
- Tombol checkout
- Tampilan empty state jika kosong

---

## 🔐 Akun Demo Untuk Testing

```
Akun 1:
Email: user@example.com
Password: password123

Akun 2:
Email: test@example.com
Password: test123
```

---

## 📂 Struktur Project

```
src/app/
├── app.component.ts
├── app.module.ts
├── app-routing.module.ts
│
├── guards/
│   └── auth.guard.ts              # Proteksi routes yang membutuhkan login
│
├── services/
│   ├── auth.service.ts            # Login, register, logout, user state
│   └── product.service.ts         # Produk, cart management
│
├── models/
│   ├── user.model.ts              # Interface User
│   └── product.model.ts           # Interface Shoe, CartItem
│
├── pages/
│   ├── login/                     # Login & Register
│   │   ├── login.page.ts
│   │   ├── login.page.html
│   │   ├── login.page.scss
│   │   └── login.module.ts
│   │
│   ├── shop/                      # Katalog Produk
│   │   ├── shop.page.ts
│   │   ├── shop.page.html
│   │   ├── shop.page.scss
│   │   └── shop.module.ts
│   │
│   ├── product-detail/            # Detail Produk
│   │   ├── product-detail.page.ts
│   │   ├── product-detail.page.html
│   │   ├── product-detail.page.scss
│   │   └── product-detail.module.ts
│   │
│   └── cart/                      # Keranjang Belanja
│       ├── cart.page.ts
│       ├── cart.page.html
│       ├── cart.page.scss
│       └── cart.module.ts
│
└── tabs/
    ├── tabs.page.ts
    ├── tabs.page.html
    ├── tabs.page.scss
    ├── tabs.module.ts
    └── tabs-routing.module.ts
```

---

## 🔄 Data Flow

```
1. User membuka aplikasi
   ↓
2. Jika tidak login → Redirect ke /login
   ↓
3. Login/Register → AuthService menyimpan user di localStorage
   ↓
4. Redirect ke /tabs/shop → Tampilkan daftar sepatu
   ↓
5. User klik produk → Navigate ke detail dengan :id
   ↓
6. Pilih ukuran, warna, jumlah → Tambah ke cart via ProductService
   ↓
7. Cart disimpan di localStorage
   ↓
8. User bisa lihat cart, update, atau checkout
   ↓
9. Checkout → Clear cart & tampilkan success message
```

---

## 🛠️ Technologies Used

- **Angular 20**: Frontend framework
- **Ionic 8**: Mobile UI framework
- **TypeScript**: Language
- **RxJS**: Reactive programming
- **localStorage**: Data persistence

---

## 🚀 Cara Menjalankan

```bash
# Install dependencies
npm install

# Run development server
npm start

# Build untuk production
npm build

# Run tests
npm test
```

---

## 📝 Data Mock

Aplikasi menggunakan mock data untuk:
- **Users**: 2 akun demo yang sudah terdaftar
- **Shoes**: 6 produk sepatu dengan informasi lengkap (nama, harga, gambar, ukuran, warna, rating)
- **Cart**: Disimpan di localStorage

---

## 🎨 Styling

- **SCSS**: Untuk styling components
- **Ionic CSS**: Utility classes
- **Responsive**: Mobile-first design dengan breakpoints tablet & desktop
- **Color Scheme**: Primary (blue), Success (green), Danger (red), Warning (yellow)

---

## ✨ Fitur Tambahan yang Bisa Dikembangkan

- [ ] Backend API integration
- [ ] Payment gateway (Stripe, Midtrans)
- [ ] User profile & wishlist
- [ ] Product reviews & ratings (real)
- [ ] Order history
- [ ] Filter & sorting produk
- [ ] Promo codes & discounts
- [ ] Real-time inventory tracking
- [ ] Push notifications
- [ ] Admin dashboard

---

## 📄 License

MIT License - Bebas digunakan untuk project pribadi atau komersial.

---

**Dibuat dengan ❤️ untuk toko sepatu online modern**

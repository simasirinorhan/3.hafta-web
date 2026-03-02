BEUBlog, React ve Node.js/Express kullanılarak geliştirilmiş modern ve kullanıcı dostu bir blog platformudur. Kullanıcıların kayıt olabileceği, giriş yapabileceği, blog yazıları okuyup, kendi yazılarını paylaşabileceği dinamik bir web uygulamasıdır.

## 🚀 Özellikler

-   **Kullanıcı Kimlik Doğrulaması:** JWT (JSON Web Tokens) tabanlı güvenli kayıt ve giriş sistemi.
-   **Kullanıcı Rolleri:** Normal kullanıcılar ve admin kullanıcıları için farklı yetkilendirmeler.
-   **Blog Yönetimi:** Kullanıcılar blog yazılarını oluşturabilir, düzenleyebilir ve silebilir (sadece kendi yazılarını veya admin yetkisi ile).
-   **Zengin Metin Editörü:** Yazı oluştururken gelişmiş içerik biçimlendirmesi için React Quill entegrasyonu.
-   **Görsel Yükleme:** Blog yazıları için görsel yükleme desteği (Multer ile).
-   **Tema Desteği:** Açık (Light) ve Koyu (Dark) tema seçenekleri.
-   **Duyarlı Tasarım (Responsive):** Mobil, tablet ve masaüstü cihazlarla tam uyumlu modern arayüz (Lucide React ikonları ile).

## 🛠 Kullanılan Teknolojiler

### Frontend
-   **Kütüphane:** React (v18)
-   **Geliştirme Ortamı (Build Tool):** Vite
-   **Yönlendirme (Routing):** React Router DOM
-   **HTTP İstemcisi:** Axios
-   **Durum Yönetimi:** React Context API (AuthContext, ThemeContext)
-   **Stil/İkonlar:** CSS, Lucide React
-   **Zengin Metin Editörü:** React Quill

### Backend
-   **Çalışma Zamanı:** Node.js
-   **Web Çerçevesi:** Express.js
-   **Veritabanı:** MongoDB (Mongoose ODM ile)
-   **Kimlik Doğrulama:** JSON Web Token (JWT) & bcryptjs (şifreleme)
-   **Dosya Yükleme:** Multer

## 💻 Kurulum ve Çalıştırma

Projeyi lokal bilgisayarınızda çalıştırmak için aşağıdaki adımları izleyebilirsiniz.

### 1. Gereksinimler
-   Node.js (v18 veya üzeri önerilir)
-   MongoDB (Lokal kurulum veya MongoDB Atlas hesabı)

### 2. Depoyu Klonlayın
```bash
git clone <repository-url>
cd beublog
```

### 3. Backend Kurulumu ve Başlatılması

1.  Backend klasörüne gidin:
    ```bash
    cd backend
    ```
2.  Gerekli paketleri yükleyin:
    ```bash
    npm install
    ```
3.  Çevresel değişkenleri ayarlayın:
    `backend` klasöründe `.env` dosyanızı kontrol edin. Gerekirse MongoDB bağlantı adresinizi güncelleyin.
    ```env
    PORT=5000
    MONGODB_URI=mongodb://localhost:27017/blogdb
    JWT_SECRET=sizin-gizli-anahtariniz
    ```
4.  Sunucuyu geliştirme modunda başlatın:
    ```bash
    npm run dev
    ```
    *Backend sunucusu http://localhost:5000 adresinde çalışacaktır.*

### 4. Frontend Kurulumu ve Başlatılması

1.  Yeni bir terminal açın ve frontend klasörüne gidin:
    ```bash
    cd frontend
    ```
2.  Gerekli paketleri yükleyin:
    ```bash
    npm install
    ```
3.  Uygulamayı geliştirme modunda başlatın:
    ```bash
    npm run dev
    ```
    *Frontend uygulaması Vite tarafından sağlanan adreste (genellikle http://localhost:5173)* çalışacaktır.

## 🐳 Docker ile Çalıştırma

Eğer sisteminizde Docker kurulu ise projeyi tek bir komutla ayağa kaldırabilirsiniz. (Genoa vb. sistem hataları alıyorsanız lokal kurulum adımlarını izleyin.)

1.  Proje ana dizininde (`beublog` klasöründe) terminal açın.
2.  Aşağıdaki komutu çalıştırın:
    ```bash
    docker-compose up -d --build
    ```
3.  Frontend uygulamasına **http://localhost** adresinden erişebilirsiniz.

## 👥 Admin Kullanıcı Oluşturma (Opsiyonel)

Uygulamada bir kullanıcıyı 'admin' yapmak için, backend dizinindeyken aşağıdaki script'i çalıştırabilirsiniz:

```bash
cd backend
node make-admin.js "kullanici_eposta_adresi@ornek.com"
```
Not: İlgili e-posta adresi ile uygulamadan öncelikle kayıt olunmuş olması gereklidir.

## 📄 Lisans

Bu proje eğitim amaçlı geliştirilmiş olup MIT lisansı altındadır.

# VisionAI: Modern Nesne Tanımlama Uygulaması

Bu proje, eski .h5 model tabanlı sistemlerin yerine, Groq Cloud API'nın multimodal gücünü (Llama-3.2-11b-vision-preview) kullanarak her türlü nesneyi yüksek doğrulukla tanımlayan modern bir web uygulamasıdır.

## 🚀 Başlangıç

### 1. Hazırlık ve Ortam Kurulumu
Gerekli kütüphaneleri kurmak için aşağıdaki komutu çalıştırın:
```bash
pip install -r requirements.txt
```

### 2. API Anahtarı Yapılandırması
1. Proje dizininde `.env` dosyası oluşturun.
2. `.env.example` dosyasındaki içeriği kopyalayın ve kendi API anahtarınızı yapıştırın:
   ```env
   GROQ_API_KEY=gsk_your_real_api_key_here
   ```

### 3. Uygulamayı Çalıştırma
```bash
streamlit run app.py
```

## 🌍 Canlıya Alma (Deployment Guide)

### GitHub'a Yükleme
Projenizi GitHub'a yüklerken şu dosyaların kök dizinde olduğundan emin olun:
- `app.py` (Proje yapınıza göre `frontend/app.py` veya kök dizinde olmalı)
- `requirements.txt`
- `.gitignore` ( `.env` dosyasının yüklenmemesi için kritiktir!)

### Streamlit Cloud Üzerinden Yayınlama
1. [share.streamlit.io](https://share.streamlit.io) adresine gidin ve GitHub hesabınızla giriş yapın.
2. **"New app"** butonuna tıklayın.
3. GitHub deponuzu seçin, `Main/Master` branch'ini ve ana dosya yolunu (örneğin `frontend/app.py`) belirtin.
4. **Deploy!** butonuna basmadan önce API anahtarını eklememiz gerekiyor.

### Secrets (API Anahtarı) Tanımlama
Canlıdaki uygulamada API anahtarını güvenli bir şekilde saklamak için:
1. Uygulama ayarlarında (Settings) **"Secrets"** bölümüne gidin.
2. Aşağıdaki gibi JSON formatında veya TOML formatında anahtarınızı ekleyin:
   ```toml
   GROQ_API_KEY = "gsk_xxxx..."
   ```
3. Uygulama, `st.secrets["GROQ_API_KEY"]` veya `os.getenv("GROQ_API_KEY")` üzerinden bu anahtara erişecektir. (Kodumuz bu uyumluluğa sahiptir).

## 💡 Özellikler
- **Gerçek Zamanlı Analiz:** Groq Cloud ile saniyeler içinde yanıt.
- **Multimodal Mimari:** Her türlü nesne, bitki, hayvan veya eşyayı tanır.
- **Modern UI:** Streamlit ile geliştirilmiş, kullanıcı dostu ve premium tasarım.
- **Güvenli:** API anahtarları asla koda gömülmez, ortam değişkenleri ile yönetilir.

---
Geliştiren: Ali İhsan ÇETİN - 2026

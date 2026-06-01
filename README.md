# 🏨 HotelReviewAI

## Yapay Zekâ Destekli Otel Yorum Analiz ve Karar Destek Sistemi

HotelReviewAI, otel müşteri yorumlarını Doğal Dil İşleme (NLP) ve Makine Öğrenmesi teknikleri kullanarak analiz eden, yöneticilere müşteri memnuniyeti, risk analizi ve hizmet kalitesi hakkında veri odaklı içgörüler sunan tam yığın (Full-Stack) bir yazılım platformudur.

Bu proje, İstanbul Gedik Üniversitesi Veri Madenciliği dersi kapsamında geliştirilmiştir.

---

# 📖 Proje Hakkında

Konaklama sektöründe her gün Google Maps, Booking.com, TripAdvisor ve benzeri platformlarda binlerce müşteri yorumu paylaşılmaktadır. Bu yorumların manuel olarak incelenmesi zaman alıcı ve verimsiz bir süreçtir.

HotelReviewAI;

* Otel yorumlarını otomatik olarak toplar,
* Yapay zekâ ile duygu analizi gerçekleştirir,
* Memnuniyet ve risk skorları üretir,
* Hizmet kategorilerini belirler,
* Rakip otellerle karşılaştırma yapar,
* PDF raporları oluşturur,
* Karar destek mekanizması sunar.

Böylece yöneticilerin müşteri geri bildirimlerini hızlı ve verimli biçimde değerlendirmesine yardımcı olur.

---

# 🎯 Projenin Amacı

Bu projenin temel amacı;

* Otel yorumlarının otomatik analiz edilmesi,
* Müşteri memnuniyet seviyesinin ölçülmesi,
* Olumsuz deneyimlerin erken tespit edilmesi,
* Hizmet kalitesinin artırılması,
* Yöneticilere aksiyon alınabilir öneriler sunulmasıdır.

---

# 🚀 Temel Özellikler

## Veri Toplama

* Google Maps yorumlarını SerpAPI üzerinden çekme
* CSV dosyası ile toplu veri yükleme
* Manuel yorum ekleme
* Çok kaynaklı veri desteği

## Yapay Zekâ Analizleri

* Duygu Analizi (Pozitif / Negatif / Nötr)
* Risk Skoru Hesaplama
* Memnuniyet Skoru Üretimi
* Kategori Tespiti
* AI Destekli Özetleme
* BERT Destekli Derin Anlam Analizi

## Dashboard Özellikleri

* Genel Özet Ekranı
* Duygu Dağılım Grafikleri
* Risk Analizi
* Zaman Serisi Analizi
* Kategori Bazlı Analizler
* Otel Karşılaştırma Modülü
* Dış Platform Puan Analizi

## Raporlama

* PDF Rapor Üretimi
* KPI Analizleri
* Aksiyon Önerileri
* AI Destekli Yönetici Özeti

---

# 🏗️ Sistem Mimarisi

```text
React + Vite Frontend
          │
          ▼
      FastAPI API
          │
          ▼
      NLP Pipeline
          │
          ▼
 SQLAlchemy + SQLite
          │
          ▼
      SerpAPI Servisi
```

Sistem klasik üç katmanlı mimari kullanılarak geliştirilmiştir.

| Katman             | Teknolojiler                             |
| ------------------ | ---------------------------------------- |
| Sunum Katmanı      | React, Vite, Recharts                    |
| API Katmanı        | FastAPI, Pydantic                        |
| İş Mantığı Katmanı | NLP Pipeline, Scikit-Learn, Transformers |
| Veri Katmanı       | SQLite, SQLAlchemy                       |
| Harici Servisler   | SerpAPI, Google Maps                     |

---

# 🤖 NLP Analiz Boru Hattı

Yorum sisteme ulaştığında aşağıdaki işlemler gerçekleştirilir:

```text
Yorum
  │
  ▼
Ön İşleme
  │
  ▼
TF-IDF Vektörizasyonu
  │
  ▼
Lojistik Regresyon
  │
  ▼
Duygu Analizi
  │
  ▼
Risk Skoru
  │
  ▼
Kategori Tespiti
  │
  ▼
Aksiyon Önerisi
  │
  ▼
Veritabanına Kayıt
```

---

# 🧠 Kullanılan Yapay Zekâ Modelleri

## Makine Öğrenmesi

* TF-IDF Vektörizasyonu
* Logistic Regression

## Derin Öğrenme

* HuggingFace Transformers
* BERT Sentiment Analysis

Hibrit mimari sayesinde hem yüksek performans hem de daha güçlü bağlamsal analiz elde edilmektedir.

---

# 📊 Model Performansı

| Metrik            | Sonuç                        |
| ----------------- | ---------------------------- |
| Accuracy          | 0.667                        |
| Weighted F1 Score | 0.656                        |
| Model             | TF-IDF + Logistic Regression |
| Sınıf Sayısı      | 3                            |
| Diller            | Türkçe & İngilizce           |

---

# 🛠️ Kullanılan Teknolojiler

## Backend

* FastAPI
* SQLAlchemy
* SQLite
* Scikit-Learn
* PyTorch
* Transformers
* ReportLab
* SerpAPI
* Deep Translator
* Uvicorn

## Frontend

* React 18
* Vite
* Axios
* Recharts
* CSS Glassmorphism Tema

---

# 🗄️ Veritabanı Tasarımı

Sistem üç temel tablodan oluşmaktadır:

## Hotel

Otellere ait bilgiler

* Ad
* Adres
* Konum
* Google Puanı
* Place ID

## Review

Yorumlara ait bilgiler

* Yorum Metni
* Puan
* Duygu Etiketi
* Risk Skoru
* Memnuniyet Skoru
* Kategori
* Aksiyon Önerisi

## ExternalRating

Harici platform puanları

* Booking.com
* TripAdvisor
* Expedia
* Agoda
* Hotels.com
* ZenHotels
* Google Maps

---

# 🔌 API Endpointleri

## Dashboard

```http
GET /dashboard/summary
GET /dashboard/trend
GET /dashboard/reviews
GET /dashboard/nlp-summary
GET /dashboard/model-metrics
```

## Raporlar

```http
GET /reports/pdf
```

## Sistem Durumu

```http
GET /health
```

Swagger Dokümantasyonu:

```text
http://localhost:8000/docs
```

---

# ⚙️ Kurulum

## Gereksinimler

* Python 3.11+
* Node.js 18+
* 8 GB RAM
* İnternet Bağlantısı

---

## Backend

```bash
cd backend

pip install -r requirements.txt

uvicorn app.main:app --reload --port 8000
```

---

## Frontend

```bash
cd frontend

npm install

npm run dev
```

---

# 🌐 Uygulama Adresleri

Frontend

```text
http://localhost:5173
```

Backend

```text
http://localhost:8000
```

Swagger

```text
http://localhost:8000/docs
```

---

# 🧪 Test Süreci

Gerçekleştirilen testler:

* NLP Pipeline Testleri
* CSV Yükleme Testleri
* SerpAPI Entegrasyon Testleri
* PDF Rapor Testleri
* Otel Karşılaştırma Testleri
* Dashboard Testleri
* BERT Sağlık Kontrol Testleri

---

# ⭐ Projenin Özgün Katkıları

* Hibrit NLP Mimarisi (TF-IDF + BERT)
* Üç Kademeli Akıllı SerpAPI Arama Sistemi
* API Anahtarsız Harita Widget Yapısı
* Otomatik PDF Raporlama Sistemi
* Çok Sekmeli Dashboard Yapısı
* Çok Kaynaklı Veri Analizi Desteği

---

# 👨‍💻 Proje Ekibi

### Yasin Almaz

* Veri Mühendisliği
* Backend Geliştirme
* CSV İşleme Modülleri
* Dış Platform Entegrasyonları

### Berat Demirbaş

* Frontend Geliştirme
* Dashboard Tasarımı
* Veri Görselleştirme
* Kullanıcı Arayüzü

---

# 🎓 Akademik Bilgiler

**Ders:** Veri Madenciliği

**Üniversite:** İstanbul Gedik Üniversitesi

**Dönem:** 2025–2026 Bahar Dönemi

**Proje Türü:** Yapay Zekâ ve Doğal Dil İşleme Projesi

---

# 📌 Gelecek Çalışmalar

* BERTurk entegrasyonu
* Redis önbellekleme sistemi
* JWT kimlik doğrulama
* Docker desteği
* PostgreSQL geçişi
* Kubernetes dağıtımı
* Gerçek zamanlı bildirim sistemi
* Çok kullanıcılı yönetim paneli

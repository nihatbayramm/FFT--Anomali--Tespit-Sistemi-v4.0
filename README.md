# 🛡️ FFT Anomali Tespit Sistemi-v4.0

FFT, ağ trafiğindeki şüpheli hareketleri ve DDoS saldırılarını **Hızlı Fourier Dönüşümü (FFT)** kullanarak saptayan gelişmiş bir siber güvenlik analiz aracıdır.  
Klasik imza tabanlı sistemlerin aksine, trafiğin ritmini ve frekans spektrumunu analiz ederek anomali tespiti yapar.

---

## 🚀 Temel Özellikler

- **Spektral Analiz:**  
  Ağ paketlerini zaman domaininden frekans domainine aktararak periyodik saldırı imzalarını yakalar.

- **Gerçek Zamanlı Görselleştirme:**  
  Paket yoğunluğu ve FFT spektrumunu eş zamanlı grafikler halinde sunar.

- **Gelişmiş Anomali Motoru:**  
  Saniyeler içindeki paket değişimlerini istatistiksel olarak hesaplar ve bir **"Anomali Skoru"** üretir.

- **Siber Güvenlik Dashboard:**  
  Profesyonel *Dark Mode* arayüzü ve terminal tabanlı raporlama sistemi.

- **Hızlı PCAP İşleme:**  
  Scapy `PcapReader` mimarisi ile binlerce paketi bilgisayarı kasmadan saniyeler içinde analiz eder.

---

## 🛠️ Teknik Altyapı

Sistem, ağ trafiğini bir **sinyal** olarak ele alır.

- Rastgele insan trafiği → *White Noise* (beyaz gürültü)
- Botlar / flood araçları → Sabit frekansta tekrar eden sinyaller

Bu fark sayesinde sistem, saldırıları frekans bazlı yakalar.

### Kullanılan Teknolojiler

- Python 3.12+
- Scapy → Paket ayrıştırma ve PCAP okuma
- NumPy & SciPy → FFT ve istatistiksel analiz
- Matplotlib → Grafik çizimi
- Tkinter → Arayüz ve threading desteği

---

## 💻 Kurulum ve Çalıştırma

### 1️⃣ Gerekli Kütüphaneler

```

pip install scapy numpy scipy matplotlib

```

### 2️⃣ Sistemi Başlat

```
python3 ana_program.py

```

### 🧪 Test Verisi Oluşturma (Opsiyonel)

15 saniyelik saldırı trafiği simülasyonu:

```
sudo hping3 -S -p 80 --flood 127.0.0.1

```

### 📊 Analiz Çıktıları

**📈 Zaman Serisi**

**Trafiğin saniye saniye yoğunluğu**

**⚡ FFT Spektrumu**

**Belirli frekansta keskin spike (tepe) varsa → büyük ihtimal saldırı**

**Düz dağılım → normal trafik**

***Bu proje eğitim ve siber güvenlik araştırma amaçlı geliştirilmiştir.***

<img width="600" height="500" alt="image" src="https://github.com/user-attachments/assets/a0f854b7-f9a9-441d-b9a4-39f9cfb0bfee" />

<img width="600" height="500" alt="image" src="https://github.com/user-attachments/assets/4177bbc7-5063-4c5c-bb81-8f13db8fdbfb" />

<img width="600" height="500" alt="image" src="https://github.com/user-attachments/assets/241348db-7a98-49e3-ae16-fc60c8ca8d67" />


### 👨‍💻 Geliştirici

***Nihat Bayram***

**Sürüm: 4.0 (Stable)**

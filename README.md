# 🎯 K-Means ile Müşteri Segmentasyonu ve İş Zekası Analizi

Bu proje, bir perakende şirketinin müşteri kampanya verilerini kullanarak, müşterileri satın alma davranışlarına ve sosyo-demografik özelliklerine göre kümelemeyi amaçlayan uçtan uca bir makine öğrenmesi çalışmasıdır.

---

## 👥 Proje Ekibi Bilgileri
* **Adı Soyadı:** Betül Zağlı
* **Öğrenci Numarası:** ÖğrenciNumaranıBurayaYaz

---

## 🗂️ Veri Kaynağı ve Lisansı
* **Veri Seti Adı:** Marketing Campaign Dataset (`marketing_campaign.csv`)
* **Lisans:** Open Data Commons Open Database License (ODbL) / Public Domain (Eğitim ve araştırma amaçlı açık kaynaklı veri seti).
* **Açıklama:** Veri seti, müşterilerin demografik bilgilerini, farklı ürün kategorilerindeki harcama tutarlarını ve kampanya yanıt oranlarını içermektedir.

---

## 🛠️ Kullanılan Kütüphaneler
Projenin çalışması için aşağıdaki Python kütüphaneleri kullanılmıştır:
* `pandas`: Veri okuma, manipülasyon ve analiz işlemleri.
* `numpy`: Sayısal ve matris işlemleri.
* `scikit-learn`: Makine öğrenmesi modeli (K-Means) ve veri ölçeklendirme (StandardScaler).
* `matplotlib`: Temel veri görselleştirme.
* `seaborn`: İstatistiksel ve gelişmiş veri görselleştirme.

---

## 🚀 Projeyi Çalıştırma Talimatları

Projeyi yerel makinenizde sorunsuz bir şekilde çalıştırmak için şu adımları izleyin:

**1. Depoyu Klonlayın**
Bilgisayarınızda terminali açın ve projeyi klonlayın:
`git clone <github-repo-linkini-buraya-yapistir>`
`cd <repo-klasor-adi>`

**2. Gerekli Kütüphaneleri Yükleyin**
Sisteminizde kütüphanelerin eksiksiz olduğundan emin olmak için terminale şu komutu girin:
`pip install pandas numpy scikit-learn matplotlib seaborn`

**3. Jupyter Notebook'u Başlatın**
Proje klasörünün içindeyken terminale aşağıdaki komutu yazarak arayüzü başlatın:
`jupyter notebook`

Tarayıcınızda açılan arayüzden `.ipynb` uzantılı proje dosyasını seçin ve üst menüden **"Run All"** (Tümünü Çalıştır) seçeneğine tıklayarak kodları baştan sona çalıştırın. *(Not: `marketing_campaign.csv` veri setinin kod dosyasıyla aynı klasörde olduğundan emin olun).*

---

## 🧠 Proje Mimarisi ve Geliştirme Adımları
1. **Veri Ön İşleme:** Aykırı değerler (Outliers) IQR yöntemi ile temizlenmiş, eksik veriler medyan ile doldurulmuş ve tarih sütunları dönüştürülmüştür.
2. **Özellik Mühendisliği (Feature Engineering):** Parçalı harcamalar birleştirilerek `Total_Spent`, evdeki bireyler birleştirilerek `Total_Kids` ve yaş gruplandırmaları oluşturulmuştur.
3. **Modelleme:** K-Means algoritması için StandardScaler ile özellikler ölçeklendirilmiş, Elbow (Dirsek) yöntemi ile optimal küme sayısı **k=4** olarak belirlenmiştir.

---

## 📊 Segmentasyon Çıktıları
K-Means modellemesi sonucunda müşteriler 4 ana profile ayrılmıştır:
* **Segment 0 (Düşük Bütçeli Genç Aileler):** İndirime duyarlı, düşük gelirli ve çocuklu grup.
* **Segment 1 (Orta Bütçeli Olgun Aileler):** Sadakat programlarına yatkın, orta gelirli grup.
* **Segment 2 (VIP Senior):** Kalite ve deneyim odaklı, yüksek gelirli ve yaşça olgun grup.
* **Segment 3 (VIP Gençler):** Dijital kanallara açık, harcama potansiyeli en yüksek genç profesyoneller.

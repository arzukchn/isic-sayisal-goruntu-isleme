# ISIC 2018 ROI Segmentasyonu ve Öznitelik Çıkarımı Projesi
ISIC 2018 Deri Lezyonu Görüntülerinde ROI Segmentasyonu + Öznitelik Çıkarımı Projesi.

Bu proje, **ISIC 2018 deri lezyonu görüntü veri seti** kullanılarak  
**ROI (Region of Interest) segmentasyonu** ve **öznitelik (feature) çıkarımı** işlemlerini gerçekleştirmeyi amaçlamaktadır.

Projenin temel hedefi, deri lezyon bölgelerinin doğru şekilde maskelemesi ve bu bölgeler üzerinden istatistiksel ve şekil tabanlı özelliklerin elde edilmesidir.

---

## Proje Amaçları

- Dermoskopik görüntülerin ön işlenmesi  
- Lezyon bölgelerinin ROI maskesi ile segmentasyonu  
- Maske birleştirme ve iyileştirme işlemleri  
- ROI üzerinden öznitelik çıkarımı  
- Tıbbi görüntü analizi çalışmalarına katkı sağlamak  

---

## Kullanılan Veri Seti

- **Veri Seti:** ISIC 2018 Challenge Dataset  
- **İçerik:** Deri lezyonu dermoskopik görüntüleri  
- **Ground Truth:** Segmentasyon için ikili (binary) maske görüntüleri  

---

## Kullanılan Yöntemler

Projede aşağıdaki görüntü işleme teknikleri uygulanmıştır:

- Görüntü ön işleme (grayscale dönüşümü, filtreleme)
- Morfolojik işlemler (erosion, dilation, closing)
- ROI maskesi oluşturma ve birleştirme
- Segmentasyon sonrası öznitelik çıkarımı

---

##  Çıkarılan Öznitelikler

### 1. Birinci Dereceden (İstatistiksel) Özellikler

ROI içindeki piksel değerlerinden elde edilen özellikler:

- Ortalama (mean)
- Standart sapma (std)
- Varyans (variance)
- Minimum / maksimum değerler
- Medyan (median)
- Çarpıklık (skewness)
- Basıklık (kurtosis)
- Entropi / Enerji

---

### 2. Şekil (Shape) Özellikleri

Binary ROI maskesi üzerinden çıkarılan özellikler:

- Alan (area)
- Çevre (perimeter)
- Dairesellik (circularity)
- Kompaktlık (compactness)

---

## Proje Dosya Yapısı

```bash
isic-sayisal-goruntu-isleme/
│── notebooks/        # Jupyter Notebook dosyaları
│── data/             # Veri seti örnekleri
│── results/          # Çıktı maskeler ve öznitelik tabloları
│── report/           # Proje raporu (PDF)
│── README.md

Arzu Koçhan
Bilgisayar Mühendisliği Yüksek Lisans Öğrencisi
Sayısal Görüntü İşleme Projesi

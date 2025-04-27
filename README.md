# MNIST Veri Seti ile Rakam Sınıflandırma

Bu proje, MNIST veri seti üzerinde temel bir derin öğrenme modeli kurularak rakam sınıflandırma problemini çözmeyi amaçlamaktadır.  
Projede veri görselleştirme, model oluşturma, eğitme ve değerlendirme adımları gerçekleştirilmiştir.

---

## 🧩 Kullanılan Kütüphaneler
- **NumPy**
- **Keras**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**

---

## 📚 Proje Akışı

### 1. Verilerin Hazırlanması
- MNIST veri seti `keras.datasets` üzerinden indirildi.
- Eğitim ve test veri setleri oluşturuldu.
- 9 adet rastgele görsel seçilerek görselleştirildi.
- Etiketler `one-hot encoding` formatına çevrildi.

### 2. Modelin Oluşturulması
- `Sequential` model kullanıldı.
- Katmanlar:
  - Conv2D (32 filtre, 3x3 çekirdek)
  - MaxPooling2D
  - Conv2D (64 filtre, 3x3 çekirdek)
  - MaxPooling2D
  - Flatten
  - Dropout (%50)
  - Dense (10 sınıf, Softmax aktivasyon)

### 3. Modelin Derlenmesi ve Eğitilmesi
- Kayıp fonksiyonu: `categorical_crossentropy`
- Optimizasyon: `adam`
- Eğitim:
  - Batch size: 256
  - Epochs: 15
  - Validation Split: %10

### 4. Modelin Değerlendirilmesi
- Test veri seti üzerinde değerlendirme yapıldı.
- Başarı oranı:
  - **Test accuracy: %98.93**
  - **Test loss: 0.035**

### 5. Confusion Matrix
- Tahmin sonuçları ve gerçek değerler karşılaştırılarak karışıklık matrisi (`confusion matrix`) oluşturuldu ve görselleştirildi.

---

## 📷 Çıktı Örnekleri

- Model Özeti (model.summary())
- Eğitim doğruluğu ve kaybı (loss ve accuracy değerleri)
- Test veri seti doğruluk ve kayıp sonuçları
- Confusion Matrix görseli

---

## 📝 Kurulum ve Çalıştırma

1. Gerekli kütüphaneleri yükleyin:
    ```bash
    pip install numpy keras matplotlib seaborn scikit-learn
    ```
2. Notebook'u (`.ipynb` dosyası) açın ve hücreleri sırasıyla çalıştırın.
3. Eğitim tamamlandıktan sonra sonuçları ve confusion matrix çıktısını gözlemleyin.

---

## ✍️ Yazar
- Hafize Şenyıl

---

## 📢 Not
Bu proje eğitim amaçlı hazırlanmıştır. MNIST veri seti makine öğrenmesi ve derin öğrenme modelleri için yaygın bir benchmark veri setidir.



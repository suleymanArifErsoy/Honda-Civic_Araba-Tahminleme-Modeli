# Yapay Zeka ile Honda Civic Fiyat Tahmini
Proje Hakkında
Bu proje, makine öğrenimi tekniklerini kullanarak ikinci el Honda Civic araçlarının fiyatlarını tahmin etmeyi amaçlamaktadır. Proje, bir veri setini kullanarak veri ön işleme adımlarını gerçekleştirmekte ve bir regresyon modeli oluşturmaktadır.

--- 

## Kullanılan Teknolojiler
Proje aşağıdaki kütüphaneleri kullanmaktadır:

pandas: Veri manipülasyonu ve analizi için.

numpy: Sayısal işlemler için.

matplotlib: Veri görselleştirmesi için.

scikit-learn: Makine öğrenimi modeli oluşturma ve değerlendirme için.

random: Genetik algoritma ile özellik seçimi için.

---

## Veri Seti
Projelerde "civic-yeni-data.csv" ve "civic_güncel_veri_seti_4.csv" adlarında iki farklı veri seti kullanılmıştır. Veri setleri, araçların yılı, kilometresi, motor gücü, motor hacmi, vites tipi, yakıt türü, hasar durumu (boyalı, değişen) ve fiyat gibi özelliklerini içermektedir.

---

## Metodoloji
Veri Okuma ve Temizleme: İlk olarak civic-yeni-data.csv dosyası pandas DataFrame'ine yüklenir. Ardından, 'year', 'enginePower' ve 'engineCapacity' sütunlarındaki boş (null) değerler içeren satırlar kaldırılmıştır. Son olarak, 'painted' ve 'changed' sütunlarındaki boş değerler "yok" olarak doldurulmuştur.

Özellik Mühendisliği: Fiyat ('price') verisi, modelin performansını artırmak için np.log1p fonksiyonu kullanılarak logaritmik dönüşüme tabi tutulmuştur.

Model Oluşturma: Tahmin modeli olarak LinearRegression kullanılmıştır.

Performans Değerlendirmesi: Modelin başarısı, Ortalama Mutlak Hata (MAE), Ortalama Kare Hata (MSE) ve R² skoru metrikleri ile değerlendirilmiştir.

---

## Sonuçlar
Modelin performans değerlendirmesi aşağıdaki sonuçları vermiştir:

Test MAE: 62947.54 TL

Test R² Skoru: 0.9623

Test MSE: 0.01

Test MAE: 0.09

Test R²: 0.9550

---
## Kullanım
civic-yeni-data.csv ve civic_güncel_veri_seti_4.csv veri dosyalarını projenin kök dizinine ekleyin.

Jupyter ortamında Yapay_Zeka_Civic_Araba.ipynb dosyasını açın ve hücreleri sırayla çalıştırın.

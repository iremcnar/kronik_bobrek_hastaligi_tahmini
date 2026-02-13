# 🩺 Sağlıkta Yapay Zeka: Kronik Böbrek Hastalığı (CKD) Teşhis ve Tahmin Modeli

Bu çalışma, **Burdur Mehmet Akif Ersoy Üniversitesi** bünyesindeki **Sağlıkta Yapay Zeka** dersi kapsamında geliştirilmiştir. Projenin temel odağı, klinik laboratuvar verilerini kullanarak kronik böbrek hastalığı (CKD) riskini yüksek doğrulukla tahmin eden uçtan uca bir makine öğrenmesi iş akışı oluşturmaktır.

## 📌 Proje Özeti
Kronik Böbrek Hastalığı, erken teşhis edildiğinde ilerlemesi yavaşlatılabilen bir durumdur. Bu projede, gerçek dünya sağlık verilerinde karşılaşılan veri kalitesi sorunları (eksik veriler, hatalı veri tipleri) çözülmüş ve en iyi sonucu veren sınıflandırma algoritması tespit edilmiştir.

**Veri Seti:** [Chronic Kidney Disease Dataset](https://www.kaggle.com/datasets/mansoordaku/ckdisease)

## 🛠️ Kullanılan Teknolojiler
- **Python** (Veri Bilimi Ekosistemi)
- **Pandas & NumPy** (Gelişmiş veri manipülasyonu ve tip dönüşümleri)
- **Matplotlib & Seaborn** (Klinik bulguların dağılım ve korelasyon analizleri)
- **Scikit-Learn** (Ön işleme, Model Eğitimi ve Hiperparametre Optimizasyonu)

## 🚀 Proje Uygulama Adımları

### 1. Veri Ön İşleme ve Temizleme
- **Tip Dönüşümü:** `pcv`, `wc` ve `rc` gibi sayısal olması gerekirken hatalı girilmiş sütunlar temizlenerek `numeric` formata getirilmiştir.
- **Gelişmiş Eksik Veri Yönetimi:** Sağlık verilerinin varyansını korumak adına eksik değerler **Random Sample Imputation** (Rastgele Örnekleme) yöntemiyle doldurulmuştur.
- **Kategorik Kodlama:** Tıbbi terimler (normal/abnormal vb.) modelin anlayabileceği sayısal değerlere dönüştürülmüştür.

### 2. Keşifçi Veri Analizi (EDA)
- Özelliklerin birbirleriyle olan ilişkileri korelasyon matrisi ile incelenmiştir.
- Hemoglobin, Serum Kreatinin ve Kan Üresi gibi kritik metriklerin hastalık üzerindeki etkisi görselleştirilmiştir.

### 3. Makine Öğrenmesi ve Modelleme
Proje kapsamında birçok farklı sınıflandırma algoritması eğitilmiş ve performansları karşılaştırılmıştır:
- **Logistic Regression**
- **K-Nearest Neighbors (KNN)**
- **Decision Tree & Random Forest**
- **Extra Trees Classifier**
- **XGBoost & AdaBoost**

### 4. Hiperparametre Tünelleme (Optimization)
En iyi performansı veren modeller üzerinde **GridSearchCV** kullanılarak parametre optimizasyonu yapılmış, modelin genelleme yeteneği artırılmıştır.

## 📊 Öne Çıkan Bulgular
- **Belirleyici Faktörler:** Hemoglobin seviyesi ve Serum Kreatinin değerlerinin hastalık teşhisinde en yüksek ayırt edici güce sahip olduğu saptanmıştır.
- **Model Başarısı:** Extra Trees ve Random Forest gibi ensemble (topluluk) yöntemlerinin, sağlık verilerindeki karmaşık ilişkileri yakalamada daha başarılı olduğu gözlemlenmiştir.
- **Metrik Odaklılık:** Model değerlendirmesinde sadece doğruluğa (Accuracy) değil, hatalı teşhis riskini minimize etmek için **Recall** ve **F1-Score** metriklerine odaklanılmıştır.

## 📂 Dosya Yapısı
- `kronik_bobrek_hastaligi_tahmini_uyg4.ipynb`: Veri hazırlığından model tünellemeye kadar tüm süreci içeren ana dosya.
- `kidney_disease.csv`: Analizde kullanılan ham klinik veri seti.

 **⚠️ Önemli Uyarı:** Bu proje eğitim ve araştırma amaçlı bir akademik çalışmadır. Üretilen sonuçlar ve tahminler tıbbi tavsiye niteliği taşımaz. Gerçek bir teşhis veya tedavi süreci için mutlaka bir uzman hekime danışınız.


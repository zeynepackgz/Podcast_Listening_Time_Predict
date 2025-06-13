# 🎧 Podcast Dinlenme Süresi Tahmin Projesi

---

![Podcast Dinleme](podcast.jpg)

Bu projede, bir podcastin dinlenme süresini (**dakika cinsinden**) tahmin etmeye yönelik bir regresyon modeli geliştirdim. Modelin doğruluğunu değerlendirmek için **RMSE (Root Mean Squared Error)** metriğini kullandım. Bu metriği tercih etmemin nedeni, yarışmayı düzenleyen **Kaggle** platformunun resmi değerlendirme metriği olarak RMSE’yi belirlemiş olmasıdır. Ayrıca RMSE, büyük tahmin hatalarını daha fazla cezalandırarak modelin performansını hassas biçimde ölçen etkili bir yöntemdir.

---

## 🔍 Proje Adımları

### ✅ 1. Eksik Verilerin İşlenmesi
Veri ön işleme sürecinde, eksik değerlere müdahale ederken her boş sütun için ek bir `_na` sütunu oluşturdum. Bu sütunlar, eksik olup olmadığını `True/False` olarak göstererek modelin bu durumdan öğrenmesini sağladı.

### ⚠️ 2. Aykırı Değer Temizliği
Aykırı değerleri **IQR (Interquartile Range)** yöntemiyle tespit edip veriden temizledim.

### 📊 3. Veri Görselleştirme
Verinin dağılımını ve yapısını daha iyi anlayabilmek için çeşitli **grafikler ve görselleştirme teknikleri** kullandım.

### 🧠 4. Modelleme
Verileri sayısallaştırarak hem `LinearRegression` hem de `XGBRegressor` algoritmalarını denedim. Uygulanan deneyler sonucunda **XGBRegressor**, daha başarılı tahminler verdiği için final model olarak tercih edildi.

---

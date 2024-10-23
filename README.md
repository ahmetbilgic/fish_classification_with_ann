##Balık Sınıflandırma Projesi
Proje Özeti
Bu proje, çeşitli balık türlerini sınıflandırmak amacıyla Yapay Sinir Ağı (ANN) modeli kullanmayı hedeflemektedir. Balık türlerine ait görüntülerden oluşan bir veri seti kullanılarak, model eğitildi ve performansı değerlendirildi. Bu projede veri yükleme ve ön işleme, model oluşturma ve değerlendirme adımları yer alıyor.

Amaç
Projenin amacı, farklı balık türlerini doğru bir şekilde sınıflandırabilecek bir model geliştirmektir. Bu amaçla, ANN (Artificial Neural Network) yapısı kullanılarak sınıflandırma işlemi gerçekleştirilmiştir.

Veri Seti
Balık türlerine ait çeşitli görüntülerden oluşan bir veri seti kullanılmıştır. Görüntüler, modelin girişi için uygun boyut olan 
64
×
64
64×64 piksel olarak yeniden ölçeklendirilmiştir. Veri seti eğitim ve doğrulama olmak üzere ikiye ayrılmıştır:

Eğitim seti: Veri setinin %80’i modelin eğitimi için kullanıldı.
Doğrulama seti: %20’lik kısım modelin doğrulama aşamasında kullanıldı.
Temel Adımlar
Veri Yükleme ve Ön İşleme

ImageDataGenerator ile veri seti yüklendi ve görüntüler 1/255 ile yeniden ölçeklendirilerek normalize edildi.
Veri seti, eğitim ve doğrulama setlerine bölündü.
Model Mimarisi

Proje kapsamında kullanılan model, bir Yapay Sinir Ağı (ANN) yapısına dayanmaktadır. Bu yapı aşağıdaki katmanlardan oluşmaktadır:
Flatten katmanı: Girdi olarak alınan iki boyutlu görüntüleri tek boyutlu vektörlere dönüştürmek için kullanıldı.
Dense katmanlar: Tam bağlı sinir ağı katmanları. İlk katmanda ReLU aktivasyon fonksiyonu, son katmanda ise softmax aktivasyonu kullanıldı.
Dropout katmanı: Aşırı öğrenmeyi (overfitting) engellemek için rastgele bazı nöronları sıfırlayarak düzenleme yapıldı.
Model Eğitimi

Model, eğitim seti üzerinde eğitildi ve doğrulama seti ile test edilerek performansı ölçüldü.
Adam optimizasyon algoritması kullanılarak model optimize edildi.
Model Değerlendirme

Modelin performansı, doğrulama seti üzerinde ölçüldü. Performansı değerlendirmek için doğruluk (accuracy) ve karışıklık matrisi (confusion matrix) kullanıldı.

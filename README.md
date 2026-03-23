FLO Müşteri Segmentasyonu Analizi (RFM)
Bu proje, veri bilimi metodolojilerini kullanarak FLO müşterilerini alışveriş davranışlarına göre segmente etmek ve bu segmentler üzerinden kişiselleştirilmiş pazarlama stratejileri geliştirmek amacıyla hazırlanmıştır.

📌 İş Problemi
FLO, müşteri kitlesini daha iyi anlamak ve bu kitleyi davranış öbeklerine göre gruplandırmak istemektedir. Bu sayede her segmente özel pazarlama kampanyaları (indirimler, yeni marka tanıtımları) kurgulanarak müşteri sadakati ve karlılık artırılacaktır.

📊 Veri Seti Hikayesi
Veri seti, 2020 - 2021 yıllarında OmniChannel (hem online hem offline) alışveriş yapan 19.945 müşterinin geçmiş davranış bilgilerinden oluşmaktadır.

master_id: Eşsiz müşteri numarası.

order_channel: Alışveriş yapılan kanal (Android, iOS, Desktop, Mobile, Offline).

last_order_date: En son alışveriş tarihi.

total_order_num: Toplam alışveriş sayısı.

total_customer_value: Toplam harcama tutarı.

interested_in_categories_12: Son 12 ayda alışveriş yapılan kategoriler.

🛠️ Uygulanan Adımlar & Teknik Detaylar
1. Veri Hazırlama & Anlama

OmniChannel müşterilerin toplam harcama ve sipariş sayıları için yeni değişkenler türetilmiştir.

Tarih ifade eden değişkenler datetime formatına dönüştürülmüştür.

Aykırı değer analizi ve veri ön hazırlık süreçleri fonksiyonlaştırılmıştır.

2. RFM Metriklerinin Hesaplanması

Müşteriler için üç temel metrik hesaplanmıştır:

Recency (Yenilik): Analiz tarihi ile müşterinin son alışveriş tarihi arasındaki fark.

Frequency (Sıklık): Müşterinin toplam alışveriş sayısı.

Monetary (Parasal Değer): Müşterinin toplam harcaması.

3. RFM Skorlama ve Segmentasyon

Metrikler qcut yöntemi ile 1-5 arasında skorlara dönüştürülmüştür.

recency_score ve frequency_score birleştirilerek RF_SCORE oluşturulmuş ve regex kullanılarak 10 farklı segmente (Champions, Loyal Customers, Hibernating, vb.) ayrılmıştır.

🚀 Aksiyon Planı ve Sonuçlar
Analiz sonucunda spesifik iş vakaları için hedef kitleler belirlenmiştir:

Vaka A (Yeni Marka Tanıtımı): Sadık müşteriler arasından (Champions, Loyal Customers) kadın kategorisinden alışveriş yapanlar filtrelenerek hedeflenmiştir.

Vaka B (İndirim Kampanyası): Kaybedilmemesi gereken (Cant_Loose), uykuda olan (Hibernating) ve yeni gelen müşteriler arasından erkek/çocuk kategorisiyle ilgilenenler için özel liste oluşturulmuştur.

💻 Kullanılan Teknolojiler
Python
Pandas
Datetime

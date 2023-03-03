# Project 1: RFM Analysis (CRM Work)

## RFM Nedir?
* RFM analizi, müşteri segmentasyonu için kullanılan bir tekniktir.
* Müşterilerin satın alma alışkanlıkları üzerinden gruplara ayrılması ve bu gruplar özelinde stratejiler geliştirilmesini sağlar.
* CRM çalışmaları için birçok başlıkta veri odaklı aksiyonlar alınmasını sağlar.
* RFM analizi için gerekli veriler şunlardır: 
    * Recency - Müşterilerin bizden en son ne zaman alışveriş yaptığı gün cinsinden.  
    * Frequency - Müşterinin yaptığı toplam alışveriş sayısı. 
    * Monetary - Müşterilerin bize kazandırdığı parasal değer.
* RFM metrikleri daha iyi anlaşılabilmesi için RFM skorlarına çevrilir.
* Skorlara çevirmek demek aynı cinsten ifade etmek demektir (Standartlaştırma) ve bu durum 3 metriği de kıyaslanabilir hale getirir

## Proje Hakkında
Bir ayakkabı firması bizden müşterilerini RFM analizi kullanarak segmente etmemizi istiyor. Ve bunun için bana müşterilerine ait ham satın alma geçmişi verilerini veriyor. Ben bu ham verileri kullanarak müşterileri segmente ediyorum. Ama nasıl?

* Öncelikle veriyi inceliyorum örneğin tiplerine bakıyorum Null değer var mı yok mu ona bakıyorum betimsel istatistiklerine bakıyorum v.b"
![](https://github.com/HuseyinEfkanAlp/HuseyinEfkanAlpPortfolyo/blob/main/images/columns.jpg)
* Veri hakkında edindiğim bilgilerden sonra veriyi hazırlama kısmına geçiyorum. Boş değer varsa veriden çıkartıyorum, İade olan ürünleri çıkartıyorum, tipi obje olan fakat datetime olması gereken verilerin tipini değiştiriyorum v.b
![](https://github.com/HuseyinEfkanAlp/HuseyinEfkanAlpPortfolyo/blob/main/images/dataprepearing.jpg)
* Veriyi hazırladıktan sonra Recency,Frequency,Monetary değerleri ile yeni bir dataframe e RFM metriklerini oluşturuyorum.
![](https://github.com/HuseyinEfkanAlp/HuseyinEfkanAlpPortfolyo/blob/main/images/rfmMetrics.jpg)
* RFM metriklerini oluşturduktan sonra 1 ile 5 arasında olacak şekilde standartlaştırarak RFM scoreları oluşturuyorum ve sonra RF score adında sütun oluşturup Recency ve Frequency skorlarını yan yana getirip Her bir müşteriye özel RF scoreları oluşturuyorum.
![](https://github.com/HuseyinEfkanAlp/HuseyinEfkanAlpPortfolyo/blob/main/images/rfScore.jpg)
* Daha sonra Regex kullanarak RF score larına göre müşterileri segmentleştiriyorum.
![](https://github.com/HuseyinEfkanAlp/HuseyinEfkanAlpPortfolyo/blob/main/images/segment.jpg)

* Segmentleri aşşağıdaki grafiğe göre oluşturdum RFM metriklerinde çok kullanılır
![](https://github.com/HuseyinEfkanAlp/HuseyinEfkanAlpPortfolyo/blob/main/images/rfmGraph.jpg)

## Proje Sonucu
* Proje sonucunda : Firma bu segmentlere bakarak hangi müşterilere yoğunlaşacağına hangilerine kampanyalar yapacağına kolaylıkla karar verebilir.

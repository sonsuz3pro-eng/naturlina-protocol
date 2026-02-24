# Naturlina: Ajan Entegrasyon Stratejisi

Naturlina projesi, "Medeniyet Protokolü"nü hayata geçirmek için farklı otonom ajanların ve araçların entegre bir şekilde çalışmasını öngörmektedir. Bu strateji, her bir aracın kendi uzmanlık alanında en verimli şekilde kullanılmasını ve n8n gibi bir iş akışı otomasyon platformu üzerinden orkestrasyonunu hedefler.

## 1. Entegre Edilecek Ajanlar ve Rolleri

| Ajan/Araç | Temel Yetenekler | Naturlina Projesindeki Rolü |
| :-------- | :--------------- | :-------------------------- |
| **GenSpark** | Veri toplama, analiz, raporlama, gerçek dünya entegrasyonu (API, e-posta) | Tedarikçi verilerini (köyden bulgur, lot ID, foto, video) otomatik çekme ve QR sayfasına yükleme. | 
| **Avys** | E-ticaret CRM, müşteri segmenti, stok takip, fiyat önerisi | Naturlina satışlarında %2.5 sosyal fonu otomatik hesaplama, "katkı seç" kutusunu yönetme ve raporlama (Avrupa regülasyonu uyumlu). |
| **n8n + Make.com** | AI workflow builder, güçlü otomasyon, çeşitli AI entegrasyonu | Depo stokundan satışa, oradan fon transferine kadar tüm zinciri kurma ve farklı AI modellerini (Claude, Gemini, OpenAI) ayrı tool olarak bağlama. |
| **Composio** | Developer odaklı, 500+ uygulama bağlantısı | Tarım Kredi API veya CSV export üzerinden direkt lot verilerini çekme, blockchain hash ekleme. Düşük maliyetli pilot uygulamalar için ideal. |
| **IBM Watsonx + Hugging Face** | Kurumsal supply chain AI, blockchain entegrasyonu (IBM Food Trust) | Ürün pasaportu için traceability (QR tarayınca geçmişini gösterme), AI ile sahtecilik tespiti. |

## 2. Entegrasyon Yaklaşımı (n8n Odaklı)

Naturlina sisteminde n8n, tüm bu ajanları ve araçları birbirine bağlayan merkezi bir otomasyon katmanı olarak işlev görecektir. Her bir ajan, n8n içindeki özel bir düğüm (node) veya harici bir API çağrısı aracılığıyla entegre edilecektir. Bu yaklaşım, sistemin modülerliğini ve esnekliğini artırırken, her bir bileşenin bağımsız olarak geliştirilmesine ve güncellenmesine olanak tanır.

### Örnek İş Akışı Adımları:

1.  **Veri Girişi:** Tarım Kredi veya ERP sistemlerinden gelen yeni ürün lotu verileri (Composio aracılığıyla).
2.  **Veri Zenginleştirme:** GenSpark, toplanan ham veriyi (LID, çiftçi bilgileri, toprak analizleri) zenginleştirir ve görsel materyallerle (fotoğraf, video) destekler.
3.  **Blockchain Kaydı:** Zenginleştirilmiş veriler, Composio kullanılarak blockchain üzerine hashlenir ve benzersiz QR kodları oluşturulur.
4.  **Satış ve Fon Hesaplama:** Avys, e-ticaret platformundan gelen satış verilerini işleyerek sosyal katkı ve döngüsel dönüşüm fonlarını hesaplar.
5.  **Raporlama ve Bildirim:** n8n, tüm bu süreçlerin sonunda ilgili paydaşlara (tüketiciler, sosyal fon yöneticileri) şeffaflık raporları ve bildirimler gönderir.

Bu entegrasyon stratejisi, Naturlina projesinin karmaşık gereksinimlerini karşılamak ve "İyiliği sisteme gömmek" vizyonunu teknolojik olarak desteklemek için sağlam bir temel sunmaktadır.

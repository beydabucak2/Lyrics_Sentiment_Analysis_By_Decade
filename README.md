## Proje Açıklaması 📂
**projeI.ipynb**
Bu proje, farklı dönemlere ait şarkı sözlerinin analizini içerir. Dönemlere ve sanatçılara göre ayrılmış veri setiyle, hangi dönemde hangi duyguların baskın olduğunu yorumlamayı amaçlamaktadır.

## Projedeki Eksiklikler 🛠️

- **Yetersiz Veri Çeşidi**: Proje, ücretsiz API kısıtlamaları ve Hugging Face modelinin karakter sınırlaması nedeniyle sınırlı veriyle yapıldı. Dönemleri direkt olarak çekemediğim için her bir sanatçıyı ayrı kaydedip, sonradan dönemlere ilişkilendirdim. Bu nedenle proje süresi uzadı ve veri hazırlamaya çok zaman harcadım.
  
- **Yetersiz Duygu Kategorisi**: Projede yalnızca 3 kategori (pozitif, negatif, nötr) kullanıldı. Hugging Face modelindeki "label" sınırlamaları nedeniyle başka kategorilere ulaşamadım. Proje II dersimde, savaş, aşk, ayrılık, dans gibi temalar eklemeyi ve Hugging Face kullanmadan projeyi genişletmeyi hedefliyorum.

## Proje İçeriği 📂

- **Veri Setinin Bulunması**: Genius API ve lyricsgenius kütüphanesiyle, farklı dönemlerde popüler şarkılara sahip sanatçıların şarkı sözlerini derledim. Sanatçılar döneme göre ayrıldı ve ayrı datasetler oluşturuldu. Böylece hem sanatçılar hem de dönemler üzerinden işlem yapma imkânı sağlandı.

- **Veri Setinin Temizlenmesi ve Hazırlanması**: Şarkı sözlerindeki gereksiz kelimeler temizlendi. NLTK modülü kullanılarak açıklamalar çıkarıldı. JSON dosyaları önce DataFrame’e, sonra pickle dosyalarına dönüştürülerek analize uygun hale getirildi.

- **Analiz**: Hugging Face kütüphanesindeki bir model entegre edilerek duygu analizi yapıldı. Model, şarkı sözlerini "pozitif", "negatif" ve "nötr" etiketleriyle sınıflandırdı.

- **Veri Görselleştirme**: Dönemlere göre hangi kelimelerin daha fazla kullanıldığı belirlendi ve görselleştirildi. Ayrıca, belirli kelime gruplarıyla hangi dönemde hangi kelimelerin kullanıldığı incelendi.

## Kütüphaneler:

- **transformers**: Hugging Face Transformers kütüphanesi, şarkı sözlerinin duygu analizini gerçekleştirmek için kullanıldı.
- **torch**: PyTorch kütüphanesi, modelin çalıştırılması için gerekli.
- **pandas**: Veri analizi ve işleme için kullanıldı.
- **matplotlib**: Grafik ve görselleştirme için kullanıldı.
- **scikit-learn**: Kelime sıklığı analizi için metin vektörizasyonu yapar.
- **nltk**: Doğal dil işleme için kullanılan, kelime temizleme ve stopwords gibi işlemler için kullanıldı.
- **collections**: `Counter` sınıfı, kelime sayımlarını yaparken kullanıldı.
- **re**: Düzenli ifadeler (regex), metin temizleme ve özel kelimeleri ayıklama için kullanıldı.
- **pickle**: Veri dosyalarını (pkl formatı) yüklemek ve kaydetmek için kullanıldı.
- **os**: Dosya yolu işlemleri için kullanıldı.
- **CountVectorizer (scikit-learn)**: Kelimeleri vektör haline getirmek ve kelime sıklığı analizi yapmak için kullanıldı.
- **stopwords (nltk)**: Stopwords (gereksiz kelimeler) listesi oluşturmak için kullanıldı.

  
## Analizler ve Sonuçlar 📈
Duygu Analizi (Sentiment Analysis)

Duygu analizi için Twitter-roBERTa modeli kullanıldı. Model, şarkı sözlerini pozitif, negatif ve nötr olarak sınıflandırdı. Her dönem için elde edilen duygu dağılımları şöyle:

Örnek Duygu Dağılımı:

1960lar:

Pozitif: 15
Nötr: 33
Negatif: 25
1980ler:

Pozitif: 30
Nötr: 27
Negatif: 23
Kelime Sıklığı Analizi (Word Frequency Analysis)

Kelime sıklığı analizi ile her dönemdeki en çok kullanılan kelimeler belirlendi ve yıllara göre görselleştirildi.

Örnek Kelime Sıklıkları:

1960lar:

love: 25
girl: 15
baby: 30
1980ler:

love: 20
girl: 10
baby: 18


# IMDB Sentiment Analysis Project
Bu proje, IMDB film yorumları verisi üzerinde **Doğal Dil İşleme (NLP)** teknikleri, **Makine Öğrenmesi (ML)**, **Derin Öğrenme (DL)** ve **Kümeleme (Clustering)** algoritmalarını kullanarak yorumların **olumlu** ya da **olumsuz** olarak sınıflandırılmasını ve analiz edilmesini amaçlamaktadır.

---

## Veri Seti

- **Kaynak:** [IMDB Dataset of 50K Movie Reviews](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews)
- **Özellikler:**
  - `review`: Film yorumu (metin)
  - `sentiment`: Etiket (positive veya negative)

---

## Doğal Dil İşleme (NLP) Adımları

Yorum verisi, analiz öncesi çeşitli ön işleme adımlarından geçirilmiştir:

- HTML etiketlerinin temizlenmesi (`BeautifulSoup`)
- Köşeli parantez içeriğinin silinmesi
- Özel karakterlerin ve rakamların kaldırılması
- Küçük harfe çevirme
- İngilizce stopwords kelimelerinin silinmesi (`NLTK`)
- Kelime köklerine indirgeme (stemming)

---

## Makine Öğrenmesi Modelleri

### Özellik Çıkarımı

- **Bag of Words (CountVectorizer)**
- **TF-IDF (TfidfVectorizer)**  
Her ikisi de n-gram aralığı `(1,3)` olacak şekilde kullanılmıştır.

---

### Modeller

- **Logistic Regression**
- **Naive Bayes**
- **Random Forest**
- **Support Vector Machine (SVM)**

> Her model, eğitim ve test doğruluğu, confusion matrix ve classification report (precision, recall, f1-score) metrikleri ile değerlendirilmiştir.

## Derin Öğrenme (DL) Modelleri

Veri, `Tokenizer` ve `pad_sequences` ile vektörleştirilmiş ve sıralar eşit uzunluğa getirilmiştir.

### Kullanılan Modeller

- **LSTM (Long Short-Term Memory)**
- **BiLSTM (Çift yönlü LSTM)**
- **CNN (1D Convolutional Neural Network)**

> Her model, doğruluk ve kayıp grafikleri ile eğitilmiş ve örnek yorumlar için tahmin yapma kabiliyeti test edilmiştir.

---

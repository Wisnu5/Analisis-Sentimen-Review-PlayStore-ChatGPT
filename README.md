# Analisis-Sentimen-PlayStore-ChatGPT

Proyek ini merupakan implementasi analisis sentimen berbasis Machine Learning dan Deep Learning pada ulasan aplikasi Google Play Store, khususnya untuk aplikasi ChatGPT. Tujuan dari proyek ini adalah untuk mengklasifikasikan ulasan menjadi tiga kategori sentimen: **positif**, **netral**, dan **negatif**.

## Struktur Dataset
Dataset berisi ulasan aplikasi dengan format:

| Kolom               | Deskripsi                          |
|---------------------|-------------------------------------|
| `content`           | Teks ulasan asli                    |
| `normalized_content`| Teks ulasan yang telah dinormalisasi|
| `score`             | Label sentimen (0: negatif, 1: netral, 2: positif) |

Dataset diambil dari Google Play Store dan diproses melalui tahapan pembersihan, normalisasi, dan pelabelan sentimen.

## Proses Analisis
1. **Preprocessing Teks**
   - Case folding, tokenisasi, penghapusan stopword, stemming (Sastrawi)
2. **Visualisasi Data**
   - Distribusi sentimen, WordCloud per sentimen
3. **SMOTE**
   - Mengatasi ketidakseimbangan kelas
4. **Model Klasifikasi**
   - `Support Vector Machine (SVM)`
   - `Random Forest`
   - `BiLSTM` dengan arsitektur `Embedding → BiLSTM → Dropout → Dense`
  
## Insight
- Mayoritas ulasan bersentimen positif, namun ulasan negatif tetap signifikan.
- BiLSTM menunjukkan akurasi terbaik dalam menangkap konteks kalimat.
- SMOTE membantu meningkatkan performa model klasik.

## Referensi
- Dataset: Google Play Store
- Sastrawi: [https://github.com/har07/PySastrawi](https://github.com/har07/PySastrawi)
- TensorFlow: [https://www.tensorflow.org](https://www.tensorflow.org)

---

## Author
**Wisnu — Machine Learning Enthusiast**  
IPB University, Computer Science 💻

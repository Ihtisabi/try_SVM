# Report - Sentiment Analysis using SVM

## Langkah-langkah Implementasi

1. Persiapan Dataset:

    Dataset yang digunakan adalah dataset ulasan film yang sudah diklasifikasikan menjadi sentimen positif dan negatif.

    Dataset diunduh dari repository asli yang terdapat pada [GitHub Vasista Reddy](https://github.com/Vasistareddy/sentiment_analysis).

2. Preprocessing dan Vectorization:

    Data teks diubah menjadi vektor menggunakan metode TF-IDF untuk memungkinkan pengolahan data teks oleh model SVM.

    Parameter penting dalam TF-IDF:

    min_df = 5

    max_df = 0.8

    sublinear_tf = True

    use_idf = True

3. Model Training:

    Model SVM dengan kernel linear dilatih menggunakan data training.

    Waktu training dan prediksi dicatat untuk evaluasi performa model.

4. Testing dan Evaluasi:

    Data testing digunakan untuk mengevaluasi akurasi model menggunakan metrik precision, recall, dan f1-score.

5. Pickling Model:

    Model dan vectorizer disimpan dalam format .sav agar dapat digunakan kembali tanpa harus melatih ulang model.

## Hasil dan Evaluasi

Training time: 5.447832s; Prediction time: 0.541076s

positive:  {'precision': 0.9191919191919192, 'recall': 0.91, 'f1-score': 0.914572864321608, 'support': 100.0}

negative:  {'precision': 0.9108910891089109, 'recall': 0.92, 'f1-score': 0.9154228855721394, 'support': 100.0}

Akurasi model pada data testing mencapai sekitar 91% untuk f1-score, baik untuk kelas positif maupun negatif.

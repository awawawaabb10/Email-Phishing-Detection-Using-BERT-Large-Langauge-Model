#Email Phishing Detection Using BERT Large Language Model

📌 Deskripsi

Proyek ini mengimplementasikan BERT (Bidirectional Encoder Representations from Transformers) untuk mendeteksi email phishing secara akurat. Model ini diuji pada dua skenario:

Scenario 1: Menggunakan 7 dataset phishing email secara terpisah, dibandingkan dengan model machine learning tradisional (SVM, RF, ET, XGB, ADB).

Scenario 2: Menggunakan dataset gabungan besar berisi 203.176 email untuk meningkatkan kemampuan generalisasi model.

Hasil eksperimen menunjukkan bahwa BERT secara konsisten mengungguli model tradisional, baik dalam hal akurasi, presisi, recall, maupun F1-score.

📂 Dataset

Dataset terdiri dari email phishing dan legitimate dari 7 sumber publik terkenal:

Ling

Enron

SpamAssassin

TREC-05

TREC-06

TREC-07

CEAS-08

🔹 Total data gabungan: 203.176 email
🔹 Distribusi: 53% legitimate, 47% phishing

⚙️ Metodologi

Preprocessing

Menghapus nilai kosong dan karakter tidak relevan

Lowercasing seluruh teks

Tokenisasi menggunakan BERT WordPiece

Panjang maksimum 512 token

Pembagian Data

Scenario 1: Stratified 10-Fold Cross Validation

Scenario 2: 80% train – 20% test

Model

BERT Base (12 encoder layers, hidden size 768)

Fine-tuning untuk klasifikasi biner (phishing / legitimate)

Evaluasi

Accuracy

Precision

Recall

F1-Score

AUC-ROC

📊 Hasil Eksperimen
Scenario 1 (Dataset terpisah)

Akurasi tertinggi: 99.64% pada Ling dataset

BERT unggul di hampir semua dataset dibanding model tradisional

Pada TREC-07, ET sedikit mengungguli BERT (99.85% vs 99.82%)

Scenario 2 (Dataset gabungan)

Akurasi: 99.35%

Precision: 99.45%

Recall: 99.04%

F1-Score: 99.24%

AUC-ROC: 99.97%

Hanya 78 False Positives dan 148 False Negatives dari 40.102 email uji

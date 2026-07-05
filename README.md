# Proyek-Deep-Learning

Data yang digunakan adalah <a href="https://www.kaggle.com/datasets/prashant268/chest-xray-covid19-pneumonia">Chest X-Ray (Covid-19 & Pneumonia)</a> yang tersedia secara publik di platform Kaggle (Prashant, 2020). Dataset ini berisi 6.432 gambar foto rontgen dada yang terbagi dalam dua folder, yaitu train dan test. Masing-masing folder mempunyai tiga subfolder sesuai label kelas yang digunakan, yaitu COVID-19, Pneumonia, dan Normal.

## Latar Belakang
Diagnosis COVID-19 dan pneumonia lewat foto rontgen dada membutuhkan interpretasi manual oleh radiolog. Proses ini memakan waktu dan bergantung pada pengalaman individu. Model klasifikasi citra dapat membantu mempercepat identifikasi awal ketiga kondisi tersebut berdasarkan pola visual pada gambar rontgen.

## Metode
Model dibangun menggunakan pendekatan transfer learning dengan arsitektur VGG16. Bobot awal model diambil dari hasil pelatihan pada dataset ImageNet, lalu bagian akhir jaringan disesuaikan untuk klasifikasi tiga kelas.

## Evaluasi

| Kelas     | Precision | Recall | F1-Score | Support |
|-----------|-----------|--------|----------|---------|
| COVID-19  | 1.0       | 0.98   | 0.99     | 116     |
| Normal    | 0.79      | 0.98   | 0.87     | 317     |
| Pneumonia | 0.99      | 0.91   | 0.95     | 855     |
| Akurasi   |           |        | 0.93     | 1288    |
| Macro Avg. | 0.93     | 0.96   | 0.94     | 1288    |
| Weighted Avg. | 0.94  | 0.93   | 0.93     | 1288    |

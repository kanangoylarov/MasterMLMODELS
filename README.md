# MasterMLMODELS

**Müəllif:** Kənan Göylərov  
**İl:** 2025  
**Akademik iş:** Mətn əsaslı fişinq (phishing) aşkarlanması üçün maşın öyrənməsi modelləri  

---

## Layihənin Təsviri

Bu GitHub reposu magistr dissertasiyası çərçivəsində hazırlanmış mətn əsaslı fişinq aşkarlanması layihəsini əhatə edir. Layihənin əsas məqsədi e‑poçt və veb mətnlərinə əsaslanaraq mesajların **Legitimate (qanuni)** və ya **Phishing (fişinq)** kimi təsnif edilməsidir.

Bunun üçün müxtəlif klassik və müasir maşın öyrənməsi modelləri tətbiq edilmiş, nəticələr müqayisə olunmuş və ən optimal modellər müəyyənləşdirilmişdir. Repositoriyada bütün kodlar, Jupyter notebooklar və vizual analizlər yerləşdirilmişdir.

Bu repo dissertasiyada **Supplementary Material (Əlavə material)** kimi istifadə olunmaq üçün hazırlanmışdır.

---

## İstifadə Olunan Texnologiyalar

- Python 3.10+
- Pandas, NumPy
- Scikit‑learn
- XGBoost
- CatBoost (GPU dəstəyi ilə)
- PyTorch
- Matplotlib, Seaborn
- Jupyter Notebook

---

## Layihənin Strukturu

MasterMLMODELS/
│
├── README.md
├── ML_Classification_Notebook.ipynb
├── Visualization.ipynb
├── data/
│ └── dataset.csv
├── requirements.txt



---

## Notebookların İzahı

### ML_Classification_Notebook.ipynb

Bu notebook layihənin əsas hissəsidir və aşağıdakı mərhələləri əhatə edir:

- Datasetin oxunması və təmizlənməsi (NaN dəyərlərin silinməsi)
- Mətnlərin TF‑IDF üsulu ilə vektorizasiyası
- Train/Test bölgüsü (80/20)
- Aşağıdakı modellərin qurulması və öyrədilməsi:
  - Naive Bayes (MultinomialNB)
  - Logistic Regression
  - Decision Tree
  - Random Forest
  - XGBoost
  - CatBoost
  - Neural Network (PyTorch)
- Model performansının ölçülməsi:
  - Accuracy
  - Precision
  - Recall
  - F1‑score
- Nəticələrin müqayisəli analizi

---

### Visualization.ipynb

Bu notebook modellərin nəticələrinin vizual təqdimatı üçün istifadə olunur:

- Confusion Matrix qrafikləri
- ROC Curve və AUC dəyərləri
- Modellərin səhv və düzgün təsnifat davranışlarının izahı

---

## Dataset Haqqında

- Dataset ölçüsü: **82,486 sətir**
- Sütunlar:
  - `text_combined` – təmizlənmiş mətn məzmunu
  - `label` – 0 (Legitimate), 1 (Phishing)
- Sinif balansı:
  - Normal mesajlar ≈ 40%
  - Fişinq mesajları ≈ 60%

Dataset real fişinq kampaniyaları, spam mesaj bazaları və Enron e‑poçt datasetinin təmizlənmiş versiyasının birləşməsi əsasında formalaşdırılmışdır.

---

## Əsas Modellər və Nəticələr

| Model                  | Accuracy (%) | F1‑score (%) |
|------------------------|--------------|--------------|
| Naive Bayes            | 96.24        | 96.32        |
| Logistic Regression    | 98.05        | 98.13        |
| Decision Tree          | 96.43        | 96.56        |
| Random Forest          | 98.71        | 98.76        |
| XGBoost                | 97.59        | 97.58        |
| CatBoost               | 98.79        | 98.76        |
| Neural Network         | 99.24        | 99.22        |

Ən stabil və yüksək nəticə Random Forest, CatBoost və Neural Network modelləri ilə əldə edilmişdir.

---

## Quraşdırma və İstifadə

1. Repositoriyanı klonlayın:
```bash
git clone https://github.com/kanangoylarov/MasterMLMODELS.git
cd MasterMLMODELS


python -m venv venv
source venv/bin/activate    # macOS/Linux
venv\Scripts\activate       # Windows


```




# 📊 YouTube Trending Videos – Analyse & Machine Learning

## 📝 Projektbeschreibung

Dieses Projekt analysiert Trending Videos auf YouTube aus mehreren Ländern und untersucht die Faktoren, die den langfristigen Trend-Erfolg eines Videos beeinflussen. Neben der klassischen Datenanalyse wurden Machine-Learning-Modelle (RandomForest, XGBoost) eingesetzt und Textdaten (Titel, Tags) in die Vorhersage integriert.

---

## 🎯 Ziel des Projekts
- **Verstehen, welche Faktoren YouTube-Videos langfristig in den Trends halten.**
- **Kombination von Engagement-Daten (Views, Likes, Kommentare) mit Textdaten (Titel, Tags, Buzzwords).**
- **Vorhersage: Bleibt ein Video 'lange' in den Trends?**

---

## 📦 Datengrundlage
- **YouTube Trending Dataset** (Kaggle): 375.000+ Videos aus 10 Ländern
- **Spalten:** Video-Metriken (Views, Likes, Kommentare), Titel, Tags, Veröffentlichungszeitpunkt, Kategorie

---

## 🔍 Explorative Datenanalyse (EDA)

### ▶️ Erfolgsmetriken
| Metrik        | Median | Durchschnitt | Maximalwert |
|---------------|--------|--------------|-------------|
| **Views**      | 119.277 | 603.455      | 113.876.217 |
| **Likes**      | 2.699   | 21.875       | 4.924.056   |
| **Kommentare** | 376     | 2.785        | 1.084.435   |

### 🌍 Länder-Insights
- **USA & GB: Höchste Views gesamt, aber geringere Interaktion pro View.**
- **Russland & Mexiko: Weniger Views, aber **höchste Kommentare pro View** → Community-stark.**

### 📺 Top-Videos
- **YouTube Rewind, Avengers-Trailer, BTS, Childish Gambino** → Internationale Viral-Hits.

---

## 🧑‍💻 Machine Learning – Vorhersage "Langzeit-Trend"

### 🧠 Modelle:
- **RandomForest**
- **XGBoost**
- **Text + Engagement Modell (final)**

### 🧪 Ergebnisse:
| Metrik                | Nur Engagement | Text + Engagement | Optimiertes RF |
|------------------------|-----------------|-------------------|----------------|
| **Accuracy**            | 89,75 %        | 95,23 %           | **95,33 %** ✅ |
| **Precision (Lang)**    | 87,65 %        | 96,16 %           | **96,27 %** ✅ |
| **Recall (Lang)**       | 79,95 %        | 88,81 %           | **89,01 %** ✅ |
| **F1-Score (Lang)**     | 83,62 %        | 92,34 %           | **92,50 %** ✅ |

**➡️ Bestes Modell: RandomForest + Hyperparameter-Tuning (Text + Engagement)**

---

## 🧠 Key Insights:
- **Textdaten wie Titel & Tags massiv wichtig für Langzeit-Erfolg.**
- **Engagement (Likes, Kommentare) bleibt zentral – aber ohne Titelanalyse bleibt Potenzial liegen.**
- **Kombination aus Text + Interaktion = Bestes Ergebnis (F1-Score 92,5 %).**

---

## 📂 Projektstruktur
```
youtube-trending-analysis/
│
├── data/             # Rohdaten CSVs
├── notebooks/        # Jupyter Notebooks
├── scripts/          # Python-Skripte
├── visuals/          # Plots & Grafiken
│
├── .gitignore
├── README.md
```

---

## 🚀 Learnings
- **EDA → Daten aus 10 Ländern analysiert, große Unterschiede im User-Verhalten.**
- **Feature Engineering → Titel, Tags & Buzzwords als zusätzliche Features.**
- **Machine Learning → Kombi aus Text + Engagement liefert bestes Modell.**
- **Hyperparameter-Tuning → Letzte Prozente für optimale Genauigkeit.**

---

## 🛠️ Technologien
- **Python, Pandas, Matplotlib, Seaborn, Scikit-Learn, XGBoost**

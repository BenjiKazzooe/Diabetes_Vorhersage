
README.md:

# 🏥 Diabetes-Klassifikation mit SHAP-Analyse  

📊 **Maschinelles Lernen zur Vorhersage von Diabetes mit XGBoost & Explainable AI (SHAP)**  

---

## 🔹 **Projektbeschreibung**  
Dieses Projekt nutzt **Machine Learning (XGBoost)**, um vorherzusagen, ob eine Person an Diabetes erkrankt ist.  
Mit **SHAP (SHapley Additive Explanations)** analysieren wir die Bedeutung einzelner Features und verstehen, wie unser Modell Entscheidungen trifft.  

---

## 🔹 **Daten**  
📂 **Datensatz:** [Pima Indians Diabetes Dataset](https://www.kaggle.com/datasets/nancyalaswad90/review)  

**Spalten im Datensatz:**  
- `Glucose`: Blutzucker-Wert  
- `BMI`: Body Mass Index  
- `Age`: Alter der Person  
- `Pregnancies`, `BloodPressure`, `SkinThickness` u.a.  

---

## 🔹 **Verwendete Technologien**  
🐍 **Python** (pandas, numpy, matplotlib)  
🤖 **Machine Learning**: XGBoost  
🎯 **Explainable AI**: SHAP  
📈 **Datenvisualisierung**: Matplotlib, Seaborn  

---

## 🏆 Modellvergleich: XGBoost vs. Random Forest vs. Logistische Regression

| Modell                     | Accuracy| Precision |   Recall   | F1-Score|
|----------------------------|---------|-----------|------------|---------|
| **XGBoost**                | 0.6039  | 0.4706    | **0.8727** | 0.6115  |
| **Random Forest**          | 0.7208  | 0.6071    | 0.6182     | 0.6126  |
| **Logi. Regression**       |**0.7532**|**0.6491**| 0.6727     |**0.6607**|

### Fazit
- **XGBoost hat den höchsten Recall** (87,3%) → Bestes (und dann auch gewähltes) Modell, wenn möglichst viele Diabetes-Fälle erkannt werden sollen.  
- **Logistische Regression hat die höchste Accuracy (75,3%)** → Bestes Modell, wenn Balance aus Precision & Recall gewünscht ist.  
- **Random Forest liegt in der Mitte** → Kann evtl. mit Feature Engineering verbessert werden.  
---
## ⏳ ARIMA-Zeitreihenanalyse für Glucose-Level

Das ARIMA(5,1,0)-Modell wurde trainiert, um den Glucose-Level über die Zeit zu modellieren.

**Modellstatistiken:**
- **AIC = 7614, BIC = 7642** → Niedrigere Werte sind besser.
- **Alle AR-Koeffizienten sind signifikant** (p-Wert < 0.05).
- **Kurtosis = 3.38, Skew = 0.20** → Fast normalverteilte Residuen.
- **Ljung-Box-Test (`Prob(Q) = 0.58`)** → Kein Hinweis auf starke Autokorrelation.

### 📌 Interpretation:
- **Das Modell kann für Glucose-Vorhersagen genutzt werden.**
- **Es zeigt eine autoregressive Struktur (Glucose-Level hängt von vorherigen Werten ab).**
  
---

## 🔹 **Feature Importance Analyse mit SHAP**  
### 📊 **Wichtigste Features laut SHAP**  
Hier eine SHAP Summary-Analyse, die zeigt, welche Features den größten Einfluss auf die Diabetes-Vorhersage haben:  

- **Glucose ist der wichtigste Faktor für eine Diabetes-Diagnose**  
- **BMI & Alter haben ebenfalls einen starken Einfluss**  
- **Andere Faktoren (SkinThickness, BloodPressure) haben geringere Auswirkungen**  
![Figure_1](https://github.com/user-attachments/assets/fb4df2e0-9850-4e17-b586-d63661ef5c96)

---

## **SHAP-Abhängigkeitsanalysen**  
### 🔹 **Glucose vs. Diabetes-Risiko**  
- Je höher der **Glucose-Wert**, desto größer die Wahrscheinlichkeit einer Diabetes-Erkrankung  
- Der Effekt ist **linear** (höhere Werte = höheres Risiko)  

![Figure_2](https://github.com/user-attachments/assets/3fe9f36b-0631-493d-a4c3-fa08ea2084b5)
### 🔹 **BMI vs. Diabetes-Risiko**  
- Ein **BMI über 30** erhöht das Diabetes-Risiko sprunghaft  
- Ältere Personen (rote Punkte) sind stärker betroffen  
![Figure_3](https://github.com/user-attachments/assets/4ee3611b-b677-4ef2-b23a-7ab2e414b8e5)



---





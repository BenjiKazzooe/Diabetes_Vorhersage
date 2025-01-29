# diabetes-classification-shap

README.md:

🏥 Diabetes-Klassifikation mit SHAP-Analyse
📊 Maschinelles Lernen zur Vorhersage von Diabetes mit XGBoost & Explainable AI (SHAP)

🔹 Projektbeschreibung
Dieses Projekt nutzt Machine Learning (XGBoost), um vorherzusagen, ob eine Person an Diabetes erkrankt ist.
Mit SHAP (SHapley Additive Explanations) analysieren wir die Bedeutung einzelner Features und verstehen, wie unser Modell Entscheidungen trifft.


🔹 Daten
📂 Datensatz: Pima Indians Diabetes Dataset (Source: https://www.kaggle.com/datasets/nancyalaswad90/review)


Spalten:

Glucose: Blutzucker-Wert
BMI: Body Mass Index
Age: Alter der Person
Pregnancies, BloodPressure, SkinThickness u.a.


🔹 Verwendete Technologien
🐍 Python (pandas, numpy, matplotlib)
🤖 Machine Learning: XGBoost
🎯 Explainable AI: SHAP
📈 Datenvisualisierung: Matplotlib, Seaborn


🔹 Modell-Training & Evaluierung
Wir haben XGBoost als Hauptmodell gewählt und folgende Metriken zur Evaluierung genutzt:

Modell	  Accuracy	  Precision	  Recall	  F1-Score
XGBoost	  85.4%	      82.1%	      79.5%    	80.8%


🔹 Feature Importance Analyse mit SHAP
📊 Wichtigste Features laut SHAP
Hier eine SHAP Summary-Analyse, die zeigt, welche Features den größten Einfluss auf die Diabetes-Vorhersage haben:


Glucose ist der wichtigste Faktor für eine Diabetes-Diagnose
BMI & Alter haben ebenfalls einen starken Einfluss
Andere Faktoren (SkinThickness, BloodPressure) haben geringere Auswirkungen


🏆 SHAP-Abhängigkeitsanalysen
Glucose vs. Diabetes-Risiko:

Je höher der Glucose-Wert, desto größer die Wahrscheinlichkeit einer Diabetes-Erkrankung
Der Effekt ist linear (höhere Werte = höheres Risiko)

BMI vs. Diabetes-Risiko:

Ein BMI über 30 erhöht das Diabetes-Risiko sprunghaft
Ältere Personen (rote Punkte) sind stärker betroffen

![Figure_2](https://github.com/user-attachments/assets/3fe9f36b-0631-493d-a4c3-fa08ea2084b5)
![Figure_3](https://github.com/user-attachments/assets/4ee3611b-b677-4ef2-b23a-7ab2e414b8e5)

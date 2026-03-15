# Titanic ML Analysis

Dieses Projekt wurde im Rahmen eines Machine-Learning-Wettbewerbs erstellt, um zu vergleichen, wie effizient verschiedene Klassifikationsmodelle Passagiere der Titanic-Daten korrekt einordnen koennen (ueberlebt/nicht ueberlebt).

## Projektziel

Ziel ist es,

- unterschiedliche ML-Modelle auf demselben Datensatz zu trainieren,
- die Vorhersageguete fair zu vergleichen,
- und auf Basis objektiver Kennzahlen das geeignetste Modell auszuwaehlen.

Im Fokus stehen dabei sowohl die Genauigkeit als auch die Robustheit der Modelle.

## Datengrundlage

Verwendet werden die klassischen Titanic-Wettbewerbsdaten:

- train.csv: Trainingsdaten mit Zielvariable Survived
- test.csv: Testdaten ohne Zielvariable
- gender_submission.csv: einfache Baseline-Einreichung

Die zentrale Aufgabe ist eine binaere Klassifikation:

- 1 = ueberlebt
- 0 = nicht ueberlebt

## Projektstruktur

- titanic_classificationmodels.ipynb: Hauptanalyse der Klassifikationsmodelle
- Clustering.ipynb: zusaetzliche explorative Analyse mit Clustering-Ansatz
- train.csv, test.csv, gender_submission.csv: Datensaetze
- README.md: Projektdokumentation

## Vorgehensweise

1. Daten laden und ueberblicken
2. Fehlende Werte analysieren und behandeln
3. Kategoriale Merkmale kodieren
4. Relevante Features auswaehlen oder ableiten
5. Mehrere Modelle trainieren
6. Modelle anhand geeigneter Metriken vergleichen
7. Bestes Modell fuer Vorhersagen auf test.csv nutzen

## Verglichene Modelle

Abhaengig vom Notebook-Stand werden typischerweise mehrere der folgenden Modelle verglichen:

- Logistic Regression
- Decision Tree
- Random Forest
- K-Nearest Neighbors
- Support Vector Machine
- ggf. weitere Ensemble-Modelle

## Bewertungsmetriken

Zur fairen Bewertung werden typischerweise genutzt:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

Wichtig: Eine hohe Accuracy allein ist nicht immer ausreichend. Deshalb werden mehrere Metriken gemeinsam betrachtet.

## Ausfuehrung

### 1. Voraussetzungen

- Python 3.10+
- Jupyter Notebook oder VS Code mit Notebook-Support

### 2. Empfohlene Pakete

- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

Beispielinstallation:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

### 3. Notebook starten

```bash
jupyter notebook
```

Dann das Notebook titanic_classificationmodels.ipynb oeffnen und die Zellen der Reihe nach ausfuehren.

## Erwartetes Ergebnis

Am Ende liegt ein nachvollziehbarer Modellvergleich vor, inklusive:

- Datenaufbereitung,
- Trainings- und Evaluationsschritten,
- sowie einer begruendeten Auswahl des effizientesten Modells fuer die Titanic-Klassifikation.

## Hinweise zur Nachvollziehbarkeit

- Fuer reproduzierbare Ergebnisse sollten Random-States gesetzt werden.
- Datensplitting (z. B. Train/Validation) sollte konsistent erfolgen.
- Feature-Engineering-Schritte sollten im Notebook klar dokumentiert sein.

## Moegliche Erweiterungen

- Hyperparameter-Optimierung mit GridSearchCV/RandomizedSearchCV
- Cross-Validation statt einmaligem Holdout
- Feature-Importance-Analyse
- Vergleich mit XGBoost/LightGBM
- Export der finalen Submission-Datei

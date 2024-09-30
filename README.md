# Tech Stack:
![image](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
![image](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)\
![image](https://img.shields.io/badge/spaCy-09A3D5.svg?style=for-the-badge&logo=spaCy&logoColor=white)
![image](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![image](https://img.shields.io/badge/Numpy-777BB4?style=for-the-badge&logo=numpy&logoColor=white)
![image](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)

# Klasyfikacja opinii WCCRS
[Korpus WCCRS](https://clarin-pl.eu/dspace/handle/11321/700) sklada się z recenzji dla nastepujących dziedzin: `hotele`, `medycyna`, `produkty` i `uniwersytet`.\
W zadaniu przeprowadzono klasyfikację opinii za pomocą 5 modeli:
- Naive Bayes
- Logistic Regression
- SVC
- kNN
- Ridge Classifier

W każdym modelu wybrano hiperparametry za pomocą  przeszukiwania siatki (GridSearchCV).

## Preprocessing
Wykonano:
- Lematyzacje
- Usunięcie znaków interpunkcyjnych
- Usunięcie stopwrdsów
- Przekształcenie na rzadką macierz cech

## Wyniki
Uwzględniając nierównomierne rozłożenie klas wybrano metrykę F1-Score (weighted).

### Wyniki dla CountVectorizer:

| Model               | Domyślne hiperparametry | Najlepsze hiperparametry |
|---------------------|------------------|---------------|
| Naive Bayes         | 0.9766           | 0.9832        |
| Logistic Regression | 0.9875           | 0.9905        |
| SVC                 | 0.9809           | 0.9858        |
| kNN                 | 0.4582           | 0.5103        |
| Ridge Classifier    | 0.9617           | 0.9791        |

### Dla TfidfVectorizer:

| Model               | Domyślne hiperparametry | Najlepsze hiperparametry |
|---------------------|------------------|---------------|
| Naive Bayes         | 0.8040           | 0.9820        |
| Logistic Regression | 0.9797           | 0.9911        |
| SVC                 | 0.9899           | 0.9905        |
| kNN                 | 0.6530           | 0.9546        |
| Ridge Classifier    | 0.9869           | 0.9869        |

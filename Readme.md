# НЕДЕЛЯ 1 — Линейные модели

## День 1: Linear Regression
- Что такое MSE и почему она используется
- Формулы коэффициентов (нормальное уравнение)
- Мультиколлинеарность и почему она ломает регрессию
- R² и скорректированный R²
- Практика: `LinearRegression()` в sklearn

## День 2: Ridge и Lasso
- L2-регуляризация (Ridge) — формула и эффект
- L1-регуляризация (Lasso) — формула и почему обнуляет веса
- Когда использовать Ridge, а когда Lasso
- Elastic Net — комбинация
- Практика: `RidgeCV()`, `LassoCV()`

## День 3: Logistic Regression
- Sigmoid функция и почему она нужна
- Log-loss (binary cross-entropy) — формула
- Почему нельзя использовать MSE для классификации
- Интерпретация коэффициентов (odds ratio)
- Практика: `LogisticRegression(C=1.0)`, `predict_proba()`

## День 4: Softmax и многоклассовая классификация
- Softmax функция
- Связь с cross-entropy для N классов
- One-vs-Rest (OvR) и One-vs-One (OvO)
- Практика: логистическая регрессия на 3+ классах

## День 5: Градиентный спуск
- Batch GD, SGD, Mini-batch GD — различия
- Learning rate и что будет при слишком большом/маленьком
- Momentum, Nesterov
- Практика: `SGDClassifier(loss='log_loss')`

## День 6: Пайплайны с линейными моделями
- `StandardScaler` — почему важен для линейных моделей
- `PolynomialFeatures` — создание нелинейных признаков
- `Pipeline` — объединение шагов
- `GridSearchCV` — подбор alpha/C
- Практика: полный пайплайн регрессии

## День 7: Алгоритмы + повтор
- Решить 2 задачи на Two Sum (Easy)
- Написать `train_test_split()` руками
- Повторить все формулы недели

---

# НЕДЕЛЯ 2 — Метрики, KNN, Naive Bayes, SVM

## День 8: Метрики классификации
- Матрица ошибок (TP, TN, FP, FN)
- Accuracy, Precision, Recall, F1-score
- Specificity, TPR, FPR
- Когда какая метрика важна
- Практика: `classification_report`, `confusion_matrix`

## День 9: ROC-AUC и PR-AUC
- ROC-кривая (TPR vs FPR)
- AUC — что означает и как интерпретировать
- PR-кривая (Precision vs Recall)
- Когда ROC-AUC обманывает (сильный дисбаланс)
- Практика: `roc_auc_score()`, `precision_recall_curve()`

## День 10: KNN
- Метрики расстояния (Евклид, Манхэттен)
- Выбор K (эмпирическое правило sqrt(n))
- Проклятие размерности
- Почему KNN lazy learner
- Практика: `KNeighborsClassifier()`, `StandardScaler` перед KNN

## День 11: Naive Bayes
- Формула Байеса
- "Наивное" допущение о независимости
- GaussianNB (непрерывные признаки)
- MultinomialNB (счетчики/частоты)
- BernoulliNB (бинарные признаки)
- Практика: `GaussianNB()` на классификации

## День 12: SVM — линейный случай
- Гиперплоскость, margin, support vectors
- Hard margin vs Soft margin (параметр C)
- Зачем нужен SVM при наличии логистической регрессии
- Практика: `SVC(kernel='linear', C=1.0)`

## День 13: SVM — kernel trick
- Проблема линейной разделимости
- Kernel trick — как работает без поднятия размерности
- RBF, polynomial, sigmoid ядра
- Параметры C и gamma
- Практика: `SVC(kernel='rbf')`, подбор C и gamma

## День 14: Алгоритмы + повтор
- Решить задачу на два указателя (3Sum — Medium)
- Решить задачу на хэш-таблицы (Subarray Sum Equals K)
- Сравнить KNN, SVM, Logistic Regression на одном датасете

---

# НЕДЕЛЯ 3 — Деревья и ансамбли

## День 15: Decision Tree
- Как дерево выбирает признак для split
- Gini impurity и Entropy — формулы
- Information Gain
- Pruning (max_depth, min_samples_split, min_samples_leaf)
- Практика: `DecisionTreeClassifier()`, `plot_tree()`

## День 16: Feature importance и переобучение
- Как считаются feature_importances_ у дерева
- Почему деревья склонны к переобучению
- Как ограничить глубину и другие параметры
- Bias-variance tradeoff для деревьев
- Практика: визуализация важности признаков

## День 17: Random Forest — Bagging
- Bagging — bootstrap aggregation
- Random subspace method (выбор признаков на каждом сплите)
- Почему RF не переобучается с ростом деревьев
- OOB (out-of-bag) оценка
- Практика: `RandomForestClassifier()`, `oob_score=True`

## День 18: Gradient Boosting — основы
- Идея последовательного обучения на остатках
- Разница между Bagging и Boosting
- Learning rate (shrinkage) — зачем нужен
- Subsample (стохастический бустинг)
- Практика: `GradientBoostingClassifier()`

## День 19: XGBoost
- Почему XGBoost быстрее обычного бустинга
- Вторые производные (Newton boosting)
- Как XGBoost обрабатывает пропуски
- Регуляризация в XGBoost
- Практика: `xgb.XGBClassifier()`

## День 20: LightGBM и CatBoost
- LightGBM: leaf-wise vs level-wise рост
- Категориальные фичи без One-Hot
- CatBoost: симметричные деревья
- Когда какой бустинг выбирать
- Практика: `lgb.LGBMClassifier()`, `catboost.CatBoostClassifier()`

## День 21: Алгоритмы + повтор
- Решить задачу на BFS (Number of Islands — Medium)
- Решить задачу на динамику (Maximum Subarray — Easy)
- Сравнить Decision Tree vs RF vs XGBoost на одном датасете

---

# НЕДЕЛЯ 4 — Кластеризация и снижение размерности

## День 22: K-means
- Алгоритм (инициализация → assign → update)
- Проблема случайной инициализации (K-means++)
- Как выбрать K: elbow method, silhouette score
- Ограничения K-means (только выпуклые кластеры)
- Практика: `KMeans()`, `silhouette_score()`

## День 23: DBSCAN
- Параметры eps и min_samples
- Типы точек: core, border, noise
- Преимущества: произвольная форма кластеров, шум
- Когда DBSCAN лучше K-means
- Практика: `DBSCAN(eps=0.5, min_samples=5)`

## День 24: Иерархическая кластеризация
- Agglomerative vs Divisive
- Метрики расстояния между кластерами (single, complete, average, ward)
- Дендрограмма — как читать
- Когда использовать вместо K-means
- Практика: `AgglomerativeClustering()`, `dendrogram`

## День 25: PCA
- Геометрический смысл (поворот осей на максимальную дисперсию)
- Explained variance ratio
- Когда PCA полезен, а когда нет
- Ограничения: только линейные связи
- Практика: `PCA(n_components=2)`, визуализация

## День 26: t-SNE и UMAP
- t-SNE: что делает и как работает (probability distribution)
- Perplexity — что это и как выбирать
- Только для визуализации, нельзя использовать перед обучением
- UMAP — быстрее и сохраняет глобальную структуру
- Практика: `TSNE()`, сравнение с PCA на синтетических данных

## День 27: LDA (Linear Discriminant Analysis)
- Разница между PCA и LDA (unsupervised vs supervised)
- Как LDA ищет оси, разделяющие классы
- Когда LDA лучше PCA для классификации
- Практика: `LinearDiscriminantAnalysis()`

## День 28: Алгоритмы + повтор
- Решить задачу на слайдинг окно (Longest Substring — Medium)
- Решить задачу на графы (Clone Graph — Medium)
- Сравнить K-means и DBSCAN на датасете с шумом

---

# НЕДЕЛЯ 5 — Пайплайны, препроцессинг, кросс-валидация

## День 29: Sklearn Pipeline
- `Pipeline` — последовательное применение трансформеров
- `make_pipeline` — сокращенная запись
- Доступ к параметрам через `model__param`
- Практика: пайплайн из scaler + модель

## День 30: ColumnTransformer
- Разные трансформеры для разных колонок
- `OneHotEncoder` для категориальных
- `StandardScaler` для числовых
- `remainder='passthrough'` или `'drop'`
- Практика: полный препроцессинг

## День 31: FeatureUnion и кастомные трансформеры
- `FeatureUnion` — параллельные ветки обработки
- `FunctionTransformer` — свои функции
- Наследование от `BaseEstimator`, `TransformerMixin`
- Практика: кастомный трансформер для выбросов

## День 32: Кросс-валидация — продвинутые стратегии
- `KFold` vs `StratifiedKFold` (для несбалансированных классов)
- `TimeSeriesSplit` (для временных рядов)
- `GroupKFold` (когда есть группы, например, пациенты)
- `LeaveOneOut` (маленькие датасеты)
- Практика: `cross_val_score` с разными сплиттерами

## День 33: Подбор гиперпараметров
- `GridSearchCV` — полный перебор
- `RandomizedSearchCV` — случайный поиск
- `HalvingGridSearchCV` — последовательное отсеивание
- `Optuna` — байесовская оптимизация
- Практика: поиск параметров для XGBoost

## День 34: Learning curves и валидационные кривые
- `learning_curve` — диагностика bias/variance
- `validation_curve` — влияние одного параметра
- Как читать графики (underfitting/overfitting)
- Практика: построить learning curve для Random Forest

## День 35: Алгоритмы + повтор
- Решить задачу на бинарный поиск (Find Peak Element — Medium)
- Решить задачу на стек (Min Stack — Medium)
- Собрать полный пайплайн с `ColumnTransformer` + `GridSearchCV`

---

# НЕДЕЛЯ 6 — Продвинутые техники и сквозной проект

## День 36: Работа с пропусками
- `SimpleImputer` (mean, median, most_frequent, constant)
- `KNNImputer` — imputation по соседям
- `IterativeImputer` (MICE) — моделирование пропусков
- Когда какой метод использовать
- Практика: сравнение imputer'ов

## День 37: Кодирование категориальных признаков
- `OneHotEncoder` — когда категорий мало
- `OrdinalEncoder` — когда есть порядок
- `TargetEncoder` — кодирование целевой переменной (Category Encoders)
- `FrequencyEncoder` — частота вместо OHE
- Практика: `from category_encoders import TargetEncoder`

## День 38: Работа с несбалансированными классами
- `class_weight='balanced'` в моделях
- SMOTE — синтез новых объектов
- Under-sampling (RandomUnderSampler)
- Комбинация (SMOTE + Tomek Links)
- Практика: `imblearn.pipeline.Pipeline` с SMOTE

## День 39: Интерпретация моделей
- SHAP values — вклад каждого признака в предсказание
- `shap.Explainer` для любой модели
- `shap.summary_plot` — глобальная важность
- `shap.waterfall_plot` — одно предсказание
- Практика: интерпретация XGBoost через SHAP

## День 40: Feature engineering
- `PolynomialFeatures` (степени и взаимодействия)
- `KBinsDiscretizer` — бинаризация непрерывных
- `SplineTransformer` — сплайны вместо полиномов
- Временные признаки (dayofweek, hour, month)
- Практика: добавить 10 новых признаков к датасету

## День 41: Алгоритмический финал
- Решить задачу на BFS/DFS (Course Schedule — Medium)
- Решить задачу на динамику (House Robber — Medium)
- Решить задачу на кучи (Top K Frequent Elements — Medium)

## День 42: Сквозной проект (один день интенсивно)
- Взять датасет (Titanic, Churn, или House Prices)
- Сделать EDA + обработку пропусков
- Построить пайплайн с ColumnTransformer
- Сравнить 3 модели (Logistic Regression, Random Forest, XGBoost)
- Подобрать параметры через Optuna
- Оценить по ROC-AUC и PR-AUC
- Построить SHAP-интерпретацию
# Анализ данных и прогнозирование рейтинга приложений в App Store [RU]
#
## Описание проекта:

Данный проект охватывает анализ данных о приложениях в App Store с целью прогнозирования их пользовательских рейтингов. Мы используем набор данных, включающий информацию о различных параметрах приложений, таких как размер, цена, жанр и другие, чтобы создать модель машинного обучения и оценить ее производительность.

## Инструкции по запуску кода:

Убедитесь, что у вас установлены все необходимые библиотеки, такие как pandas, numpy, matplotlib, и scikit-learn. Вы можете установить их с помощью pip:
#
pip install pandas numpy matplotlib scikit-learn
#
Загрузите набор данных. В данном случае, мы используем файл AppleStore.csv, который должен быть размещен в том же каталоге, где находится ваш код.


## Описание кода:

1) Начинаем с импорта необходимых библиотек и загрузки данных из файла AppleStore.csv. Затем мы выбираем несколько колонок для анализа, включая числовые и категориальные признаки.

2) Очищаем данные, удаляя символ "плюс" из колонки cont_rating и преобразуя ее в целое число.

3) Проверяем наличие пропущенных значений в данных и выводим их процентное соотношение.

4) Далее анализируем распределение категориальных признаков currency и prime_genre.

5) Удаляем колонку currency, так как она не представляет интерес для нашей задачи, и обновляем список категориальных признаков cat_cols.

6) Строим гистограммы числовых и категориальных признаков для визуального анализа данных.

7) Вычисляем корреляции между признаками и обнаруживаем, что они в основном невысокие.

8) Строим матрицу рассеяния (scatter matrix) для более подробного анализа зависимостей между признаками и целевой переменной.

9) Добавляем новый категориальный признак is_free, который указывает, является ли приложение бесплатным.

10) Выполняем one-hot кодирование категориальных признаков и подготавливаем данные для обучения модели.

11) Стандартизируем признаки с помощью StandardScaler и применяем метод главных компонент (PCA) для снижения размерности данных.

12) Разделяем данные на обучающий и тестовый наборы.

13) Обучаем две модели машинного обучения: линейную регрессию и k-ближайших соседей (KNN).

14) Оцениваем производительность моделей с помощью коэффициента детерминации R^2 и средней квадратической ошибки MSE.

## Вывод:

Обе модели показали низкое качество предсказаний на тестовых данных, что может быть связано с отсутствием сильных корреляций между признаками и целевой переменной.

Задача прогнозирования пользовательского рейтинга приложений в App Store оказалась сложной и, возможно, требует более глубокого анализа и/или использования более сложных моделей машинного обучения.
#
#
#
#
#

# Data Analysis and App Store Rating Prediction [ENG]
#
## Project Description:

This project involves data analysis of apps in the App Store with the aim of predicting their user ratings. We use a dataset containing information on various app parameters, such as size, price, genre, and more, to create a machine learning model and evaluate its performance.

## Instructions for Running the Code:

Make sure you have all the required libraries installed, such as pandas, numpy, matplotlib, and scikit-learn. You can install them using pip:
#
pip install pandas numpy matplotlib scikit-learn
#
Download the dataset. In this case, we use the AppleStore.csv file, which should be placed in the same directory as your code.


## Code Overview:

1) Start by importing the necessary libraries and loading data from the AppleStore.csv file. We then select several columns for analysis, including numerical and categorical features.

2) Clean the data by removing the plus symbol from the cont_rating column and converting it to an integer.

3) Check for missing values in the data and print the percentage of missing values.

4) Next, we analyze the distribution of categorical features currency and prime_genre.

5) Remove the currency column as it is not relevant to our task and update the list of categorical features, cat_cols.

6) Plot histograms of numerical and categorical features for visual data analysis.

7) Calculate the correlations between features and find that they are generally low.

8) Create a scatter matrix for a more detailed analysis of relationships between features and the target variable.

9) Add a new categorical feature, is_free, indicating whether the app is free.

10) Perform one-hot encoding of categorical

11) Standardize the features using StandardScaler and apply Principal Component Analysis (PCA) to reduce the dimensionality of the data.

12) Split the data into training and testing sets.

13) Train two machine learning models: linear regression and k-nearest neighbors (KNN).

14) Evaluate the performance of the models using the coefficient of determination R^2 and mean squared error (MSE).

## Conclusion:

Both models showed low prediction quality on the test data, which may be due to the lack of strong correlations between features and the target variable.

Predicting user ratings for apps in the App Store turned out to be a challenging task and may require further in-depth analysis and/or the use of more advanced machine learning models.

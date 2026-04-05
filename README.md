# Spotify Music Genre Classification 🎸

## 0. *Project Overview*
This project aims to develop a machine learning classification model that accurately identifies tracks labeled under the "Rock" genre and assigns them to their correct genres. The primary goal is to address the common issue of genre mislabeling, where tracks tagged as "Rock" may span various subgenres or even belong to entirely different musical categories. By utilizing a dataset of audio and music categorical features, this project will apply supervised learning techniques to improve genre classification accuracy, helping to refine the categorization process and ensure that "Rock" songs are appropriately classified according to their actual sound characteristics

![genre-pitch-your-single-to-spotify-playlist-curators](https://github.com/user-attachments/assets/6bc6ddc3-7e53-4efe-80ab-7d9bc1db4758)

### Key Steps:
1. **Data Cleaning**: Removed duplicates and missing values for better data integrity.

2. **Exploratory Analysis**: Examined the distributions of song features like danceability, energy, and tempo, and visualized genre popularity and correlations between features.

3. **Genre Popularity**: Analyzed the most and least popular genres based on song popularity.

4. **Modeling**: Built and evaluated classification models, such as Random Forest, to predict whether a song belongs to the "Rock" genre based on its features.

<br>

## 1. ***Data Overview***

### **Spotify Song Dataset**:
>Dataset is comprised of 114k songs from Spotify with genre categories for each song.

<br>

***Dataset (preview)***:

![image](https://github.com/user-attachments/assets/38aa3a83-6f27-4838-90b3-2e4de1f4c3da)

***Column Info***:

![image](https://github.com/user-attachments/assets/e37d5b69-95dd-4113-9411-b8105ba1496c)

***Summary Statistics for Quantitative Columns***:

![image](https://github.com/user-attachments/assets/298cc84f-f994-428b-a00b-1d1aa98410db)

<br>

## 2. ***Exploratory Analysis***

***Histograms of Numeric Features***:

![image](https://github.com/user-attachments/assets/ec1e5659-f56a-419b-93e6-b567566166f3)

***Correlation Matrix***:

![image](https://github.com/user-attachments/assets/c4acaacf-404c-49ef-814b-de0de7d6afc5)

***Value Count for Each Genre***:

![image](https://github.com/user-attachments/assets/945dc916-4847-4cf4-b84c-eb7238dd4f51)

***Top 10 Most Popular Genres (By Average Popularity)***:

![image](https://github.com/user-attachments/assets/84de6021-146c-4b13-be14-87f824326a4b)

***Top 10 Least Popular Genres (By Average Popularity)***:

![image](https://github.com/user-attachments/assets/772d0aeb-4723-471f-a3e4-f69aa7a239b6)

***25 Most Popular Rock Songs (Graph)***:

![image](https://github.com/user-attachments/assets/128f917a-43de-442e-86ca-54b1bace3053)

***50 Most Popular Rock Songs (Table)***:

![image](https://github.com/user-attachments/assets/f2668b59-2db9-4b4b-bd6f-4f8ed38e64b1)

<br>

## 3. ***Data Preprocessing***

***Preparing Features***:

![image](https://github.com/user-attachments/assets/9aed0f25-bfbc-4779-ab1f-e17fa560c0df)

***Features & Labels***:

![image](https://github.com/user-attachments/assets/b63f7063-4e41-4103-b79a-6df532252c9a)

![image](https://github.com/user-attachments/assets/9ac23272-c000-4eb5-ae71-e1104ca04c32)

<br>

## 4. ***Multi-Model Evalutation***

### ***Training and Performance Metrics w/ Default Parameters***

![image](https://github.com/user-attachments/assets/27d45250-7919-4a21-99a1-e416a17db234)

From a simple overview of model performance, each of our models is doing a great job; however, let's take a closer look into the accuracy of predicting certain labels.

<br>

***Random Forest Classifier***:

![image](https://github.com/user-attachments/assets/d8935513-6b5b-4df5-9a79-1c34a11fb32e)

***Gradient Boosting Classifier***:

![image](https://github.com/user-attachments/assets/db376d70-b5cb-47c1-9dd4-a158ab755e2b)

***K-Nearest Neighbors***:

![image](https://github.com/user-attachments/assets/65a0fa5a-ce63-455d-b335-49cd79082791)

K-Nearest Neighbors provides the strongest precision score when predicting values that fall under the "Rock" genre compared to the other tested models, so we'll work with this model and improve its precision even more in predicting values under the "Rock" label.

<br>

## 5. ***K-Nearest Neighbors Optimization***

### ***Feature Importance***

![image](https://github.com/user-attachments/assets/9d249876-27c7-4a72-a1d9-d706eda82b10)

Important to note that Permutation Importance is being used in this case as this method is model-agnostic and works well for KNN, because it doesn't have built-in feature importance like tree-based models.

As well, Normalization is also being used as normalizing the importance scores makes sure that they sum to 1, making it easier to compare relative importance.

<br>

### ***Hyperparameter Tuning***

![image](https://github.com/user-attachments/assets/357b97c3-dea7-4cdb-8fd8-a1aedd62e673)

Maximum KNN score on the train data: 99.34%

Maximum KNN score on the test data: 99.12%

<br>

Setting our n_neighbor parameter to 4 within our K-Nearest Neighbors model we get the results below with our training and test sets.

<br>

## 6. ***Results & Conclusion***

### *Classification Report & Confussion Matrix*

![image](https://github.com/user-attachments/assets/b346ce93-82af-4972-b61b-cd792d2002d8)

![image](https://github.com/user-attachments/assets/9893b484-2189-49b6-9c93-6bbe90b355ab)


# Spotify Music Genre Classification 🎸

## 0. *Project Overview*
This project aims to develop a machine learning classification model that accurately identifies tracks labeled under the "rock" genre and assigns them to their correct genres. The primary goal is to address the common issue of genre mislabeling, where tracks tagged as "rock" may span various subgenres or even belong to entirely different musical categories. By utilizing a dataset of audio and music categorical features, this project will apply supervised learning techniques to improve genre classification accuracy, helping to refine the categorization process and ensure that "Rock" songs are appropriately classified according to their actual sound. characteristics

![genre-pitch-your-single-to-spotify-playlist-curators](https://github.com/user-attachments/assets/6bc6ddc3-7e53-4efe-80ab-7d9bc1db4758)

### Key Steps:
1. **Data Cleaning**: Removed duplicates and missing values for better data integrity.

2. **Exploratory Analysis**: Examined the distributions of song features like danceability, energy, and tempo, and visualized genre popularity and correlations between features.

3. **Genre Popularity**: Analyzed the most and least popular genres based on song popularity.

4. **Modeling**: Built and evaluated classification models, such as Random Forest, to predict whether a song belongs to the "Rock" genre based on its features.

<br>

## 1. ***Data Overview***

### **Spotify Song Dataset**:
>Comprised of 114k songs from Spotify with genre categories for each song

<br>

***Dataset***:

![image](https://github.com/user-attachments/assets/38aa3a83-6f27-4838-90b3-2e4de1f4c3da)

***Column Info***:

![image](https://github.com/user-attachments/assets/e37d5b69-95dd-4113-9411-b8105ba1496c)

***Summary Statistics for Quantitative Columns***:

![image](https://github.com/user-attachments/assets/298cc84f-f994-428b-a00b-1d1aa98410db)

<br>

## 2. ***Exploratory Analysis***

***Histograms of Numeric Features***:

![image](https://github.com/user-attachments/assets/96e1a579-4a54-4749-9198-77fef6292bc3)

***Correlation Matrix***:

![image](https://github.com/user-attachments/assets/c1d4afb2-3441-4d6d-9adc-6128468e8402)

***Value Count for Each Genre***:

![image](https://github.com/user-attachments/assets/945dc916-4847-4cf4-b84c-eb7238dd4f51)

***Top 10 Most/Least Popular Genres (By Average Popularity)***:

![image](https://github.com/user-attachments/assets/d1775273-b462-44fd-88c9-d71a02c63276)

![image](https://github.com/user-attachments/assets/641963d5-643d-4981-8ae1-c572f3bd9aee)

***50 Most Popular Rock Songs***:

![image](https://github.com/user-attachments/assets/128f917a-43de-442e-86ca-54b1bace3053)

![image](https://github.com/user-attachments/assets/45c60b70-c957-4b3f-aae6-63bf7b914a1b)


<br>

## 3. ***Data Preprocessing***

***Preparing Features***:

![image](https://github.com/user-attachments/assets/9aed0f25-bfbc-4779-ab1f-e17fa560c0df)

***Features & Labels***:

![image](https://github.com/user-attachments/assets/b63f7063-4e41-4103-b79a-6df532252c9a)

![image](https://github.com/user-attachments/assets/9ac23272-c000-4eb5-ae71-e1104ca04c32)

<br>

## 4. ***Multi-Model Evalutation***

***Training and Performance Metrics w/ Default Parameters***:

![image](https://github.com/user-attachments/assets/6170de50-a357-4375-99a9-6707526c1933)

From a simple overview of model performance, each of our models is doing a great job; however, let's take a closer look into the accuracy of predicting certain labels.

<br>

Random Forest Classifier:

![image](https://github.com/user-attachments/assets/d8935513-6b5b-4df5-9a79-1c34a11fb32e)

Gradient Boosting Classifier:

![image](https://github.com/user-attachments/assets/db376d70-b5cb-47c1-9dd4-a158ab755e2b)

K-Nearest Neighbors:

![image](https://github.com/user-attachments/assets/65a0fa5a-ce63-455d-b335-49cd79082791)


K-Nearest Neighbors provides the strongest precision score when predicting values that fall under the "Rock" genre compared to the other tested models, so we'll work with this model and improve its precision even more in predicting values under the "Rock" label.


***Hyperparameter Tuning***

![image](https://github.com/user-attachments/assets/e2575a02-504b-4d48-99c2-95e6d0233a60)

Setting our n_neighbor parameter to 4 we get the results below

![image](https://github.com/user-attachments/assets/b346ce93-82af-4972-b61b-cd792d2002d8)

![image](https://github.com/user-attachments/assets/9893b484-2189-49b6-9c93-6bbe90b355ab)


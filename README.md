# Capstone-Project---EDA-on-Play-Store-App-Review-Analysis 
![google_play_logo](https://user-images.githubusercontent.com/110918770/221432304-001f9693-d955-48b6-b3b5-52f2dd483ba6.png)

In this project we are trying to perform Exploratory Data Analysis on Playstore App Reviews (Previously known as Android Market) as a requirement of "Full Stack Data 
Science Program" of AlmaBetter as Capstone Project-1 of Module-1 (Python for Data Science).

## Problem Statement:
1. What is the distribution of Paid and Free Apps in google Playstore?
2. Which categories are having most number of listed Apps and which among these categories are most popluar amont users?
3. Who is the Target Audience of existing app makers on Google Playstore?
4. Which is the most popular Genre among the users?
5. Are customers willing to play for the App?
6. Are customers happy with the services of Google Play Store?
7. Which are the Top 10 most popular apps on Google Plays Store?
8. What is the relation between Sentiment Polarity and popularity of App on Google Play Store?
9. If you are asked to Propose one category which will be most apt to Enter the App Business, which one would you suggest and why?

## Business Objective
* The business objective for this project is that our business is looking to enter mobile application bussiness and want to figure out which type of Apps (Category, Genre, Target Audience) are most popluar among users so that it can decide which segment to target.

## Brief summarization of steps of our project is as follows:
1. At first we imported necessary libraries like Pandas, Numpy, Matplotlib & Seaborn etc.

2. Loaded the dataset and saved it in the form of Pandas Dataframe and named it play_store_main_df & user_review_main_df.

3. Made a copy of our original dataset so that original data is not altered by mistake.

4. The play_store_df contains 13 Columns and 10841 Rows and the user_review_df contains 5 Columns and 64295 Rows.

5. During the Data Cleaning Process we checked both the dataframes for Duplicated and NULL values and found that play_Store_df contained 1181 duplicated rows and 1475 Null values.

    * Null Values in Ratings column were replaced with the mean or average of ratings.

    * As there is only one null value in column Type, we replaced it with 'Free'

    * We replaced the single null value of 'Content Rating' column to 'Everyone'.

    * As we will not be using the data present in the columns named "Current Ver" and "Android Ver", so we will replace the null values with the column's last valid observation.

    * In User_review_df The column containing the null values are totally worthless as they do not provide any information about user review or sentiment in any way. Hence we will drop columns containing null values altogether.

6. After cleaning the data, we had the indexes reset and now the remaining number or rows are 9659 in our play_store_df and 37427 number of rows in the user_review_df After checking the data info we found that the Data Type of many numerical columns was also categorized as Dtype Object

    * Data in "Rating" & "Size" columns are showing to be object Dtype whereas actually they should be Float.

    * Data in "Reviews" and "Installs" columns are also object Dtype whereas it should be Integer(Int) Type.

    * Converting columns "Rating" and "Reviews" is easy but, not so easy in Columns "Size" and "Installs".

    * In column "Size" we have converted all sizes to a single unit i.e. Mb and the we have removed the string part "Mb", "Kb" etc from the values.

    * In "Installs" column we removed the "+" object from the number and have kept only the numebers as the values.

7. We then processed these columns in such a way that Dataset now shows correct Data Types against all the columns.

8. We then dropped the columns which were irrelevant for the purpose of our project namely Last Updated, Current Ver, Android Ver.

9. After that we checked the unique values of each of the columns of both dataset in order to get and overview of our data.

10. During the Data Wrangling part we merged both our datasets using an Inner Join on the column "App" in order to create a third dataframe named Combined_df .

11. In newly created combined_df there is data belonging to only 816 unique Apps. Which means that out of 9659 unique apps in play_store_df, only 816 application's matching data is present in user_review_df.

12. In the final step of Data Visualization and Story telling we have plotted around 17 different charts in order to get valuable insights from the data and have tried to describe them in simple words.

13. Finally we tried to answer all problem statements with the help of newly found insights and given our recommendations in **Solution to Business Objective** section of this notebook.

### Please see Google Colab notebook (File with the extension ".ipynb" in the repository to check out the whole project 

### Thanks and Special Mentions:
1. At first I would like to show my sincere gratitude to the awesome mentors and moderators of AlmaBetter including Hardik Gupta, Rochit Jain, Puroshotam Singh, Smruti Ranjan Pradhan, Shafil Ahmed and many more. 
2. A very big 👍to amazing educators on youtube channels like Krish Naik (https://www.youtube.com/@krishnaik06) and Code With Harry (https://www.youtube.com/@CodeWithHarry/featured).
3. And last but not the least 🙏 to the amazing community at https://stackoverflow.com/

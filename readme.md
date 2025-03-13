# Project Overview

This project performs Bivariate and Multivariate Analysis on a Music Streaming dataset to explore relationships between categorical and numerical variables. Various visualization techniques are used to understand the impact of factors like age group,country etc on listening time, music platform, subscriptions etc. This is a part of the assignment given in the course DAI-101.

# Dataset

The dataset contains the following columns:

- User_ID: Unique ID of the user
- Age: Age of the user
- Country: Country of the user
- Streaming Platform: Platform used by the user for streaming music
- Top Genre: Genre of music listened to by the user
- Minutes Streamed Per Day: Number of minutes the user streams music per day
- Number of Songs Liked: Number of songs liked by the user
- Most Played Artist: Artist most played by the user
- Subscription Type: Type of subscription of the user
- Listening Time (Morning/Afternoon/Night): Time of the day the user listens to music
- Discover Weekly Engagement (%): Engagement with the Discover Weekly playlist
- Repeat Song Rate (%): Rate of repeating songs
- Age Group: Age group of the user (This column was created based on the 'Age' column by me)

### Feature analysis - Categorical or Numerical

- Categorical Columns: Country, Streaming Platform, Top Genre, Most Played Artist, Subscription Type, Listening Time (Morning/Afternoon/Night), Age Group
- Numerical Columns: Age, Minutes Streamed Per Day, Number of Songs Liked, Discover Weekly Engagement (%), Repeat Song Rate (%)

# EDA

### Univariate Analysis

- Histograms and Boxplots for numerical columns
- Countplots for categorical columns
- Mean, Median, Mode, Standard Deviation, etc. for numerical columns
- Mode, Frequency, etc. for categorical columns
- Distribution of data in each column

### Bivariate Analysis

- Correlation matrix to identify relationships between numerical variables
- Scatter plots for continuous variable relationships
- Bar plots, violin plots, and box plots to compare categorical and numerical variables

### Multivariate Analysis

- Pair plots to analyze multiple relationships simultaneously
- Heatmaps to visualize correlations among multiple variables

### Group Comparisons - Very Important for Music Industry Companies

- Comparing listening time, platform, subscription, etc based on country and age group
- Understanding the preferences of users based on their country and age group

# Project : FLow of code

1. Read the csv file and store it in a dataframe.
2. Missing values check and handled by different techniques like dropping the rows, filling the missing values with mean (for numerical columns) and mode (for categorical columns).

3. New columns are created based on the existing columns like 'Age Group' based on the 'Age' column to get better insights from the data.

4. Some advanced techniques are also used for filling the missing values :
   - For numerical columns, I grouped data based on Country and Age group and filled the missing values with the mean of the respective group to get better results
   - For categorical columns also, I grouped data based on Country and Age group and filled the missing values with the mode of the respective group to get better results
5. Also, I have handled the invalid values like negative values in the Age column, Age greater than 100, percentage greater than 100, negative percentage, etc.
6. I have also removed the duplicate rows from the dataset.
7. Then removed outliers which were visualized using boxplot.
8. Then I have fixed incosistencies in the data like 'Bharat' and 'India' are same, 'YT' and 'YouTube' are same, etc.
9. Also for categorical columns, I have removed very rare ones, so data cleaning is done.
10. EDA is done to understand the data better.
11. Univariant analysis is done to understand the distribution of the data.
    - For numerical columns, I have plotted the histogram and boxplot to understand the distribution of the data and printed the mean, median, mode, standard deviation, etc.
    - For categorical columns, I have plotted the countplot to understand the distribution of the data and printed the mode, frequency, etc.
12. Bivariant analysis is done to understand the relationship between the columns.

    - Correlation matrix to identify relationships between numerical variables.
    - Scatter plots for continuous variable relationships.
    - Bar plots, violin plots, and box plots to compare categorical and numerical variables.

13. Multivariant analysis is done to understand the relationship between multiple columns.

    - Pair plots to analyze multiple relationships simultaneously.
    - Heatmaps to visualize correlations among multiple variables.

14. MOST IMPORTANT ONE: Group Comparisons are done , so that music industry companies understand the preferences of the users based on their country and age group.
    - That's why i have compared listening time,platform, subscription, etc based on country and age group.
    - This helps companies realy well to target the audience based on their preferences.
15. Finally, I have saved the cleaned data in a new csv file.

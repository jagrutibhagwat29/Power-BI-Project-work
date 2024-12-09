# Netflix TV show and Movie Analysis
The project aims to provide insights into the distribution of Netflix content across regions. Dynamic Visuals helped compare the popularity, ratings and IDBM score of movies versus web series, and explore trends in viewer preferences. 

## Dataset:

## Analysis Process:
-	Data Collection from a source containing dataset with Netflix content and then importing the same dataset through ‘Get Data’ feature
-	Data Cleaning involves handling of missing values, removing duplicates and error correction
-	Transformed data by using DAX (Data Analysis Expressions) to create new columns for additional metrics
-	Data Visualization includes creating visuals with various visualization tools to create charts and graphs that highlight key insights. 
-	Dashboard Creation: Arrange the visualizations on a dashboard to create a cohesive and informative layout.
-	Analysis and Insights
   
## Dashboard content:
-	Runtime (hour): 7513
-	Movie: 3759
-	Tv show:2047
-	IDBMscore:5.94
-	Netflix content by release year, Subscribes across the, Top Netflix genres, Count of Netflix content

  ![Netflix dashboard](https://github.com/user-attachments/assets/04c5bde8-e626-4a66-acca-5f3a17a701dd)


## DAX Expression
-  Avg IMDB = AVERAGE(titles[imdb_score])
- Runtime Hour = DIVIDE(SUM(titles[runtime]),60,0)
- Total Content = COUNT(titles[type])
- Total Movies = COUNTX(titles,IF(titles[type]="MOVIE",0))
- TV Show = COUNTX(titles,IF(titles[type]="SHOW",0))

##  Technical insights:
- At 407, comedy had the highest Total Movies and was 421.79% higher than drama', 'comedy, which had the lowest Total Movies at 78. 
- Total Movies and total TV Show are positively correlated with each other.
- Total Movies and TV Show diverged the most when the genres was comedy, when Total Movies were 304 higher than TV Show.  
- Across all 5 genres, Total Movies ranged from 78 to 407 and TV Show ranged from 50 to 110.

# Restaurant Business' Status Classifier
## Objective
Starting and running a successful business is a fulfilling yet incredibly challenging endeavor. According to the U.S. Bureau of Labor Statistics (BLS), roughly 45% of businesses fail within the first 5 years after its inception. Businesses fail due to various reasons; for instance, lack of market knowledge, bad location, little financing, bad service, and etc. With that being said, I decided to create a classification model that predicts whether the restaurant will close or remain open with given information (revenue, lifespan, review ratings, etc.).

## Target Audience
Target audience are lenders/investors who want to gain better insight about restaurants' business health through data and help determine whether to invest in any specific restaurants. Through this restaurant business status classifier, it contributes lenders/investors in making sound decision and minimize potential financial loss.

## Dataset
Yelp dataset is used for this project in building business' status classifier. Below are the yelp dataset's volume as of 8/14/2020.
- 8,021,122 reviews
- 209,393 businesses
- 200,000 pictures
- 10 metropolitan areas
- 1,320,751 tips (user recommendations)
- Over 1.4 million business attributes like hours, parking, availability, and ambience

## Executive Summary
Cleaned and performed data analysis through visualizations and statistical methods for data insights and performed several machine learning algorithms using finalized features that were deemed suitable in classifying restaurants' business status.

### Key findings
- Opened restaurants have higher averages values across the board compared to closed restaurants. For instance, in the scale of 1-5, average star rating (restaurant popularity) for opened restaurants were 3.59 (damped mean average) while closed restaurants had 3.47. Opened restaurants have average of 77.5 review counts (business traffic) compared to closed restaurants' review count of 39.32. General dining cost (scaled between 1-5) for closed restaurants was more expensive at 1.78 to opened restaurant's 1.75.
- Majority of the restaurants failed within 3 years, notably closed restaurant had downward trend in closure rate; majority closing within first 3 years. Open restaurants had higher average lifespan and less volatile fluctuations in closure rate.
- Closed restaurants had downward trend in revenue as restaurants remained opened over last 15 years; while opened restaurants had similar downward trend but experienced hike in revenues between 8th to 12th year. It is important to note that opened restaurant had considerable high lifespan average compared to closed restaurants.
- Opened restaurants had higher review count with high character count per review at 107.24 compared to negative review at 99.33 character count. Furthermore, opened restaurants generally had higher positive sentiment scores compared to closed restaurants.
- The popular cuisines were American (modern and traditional) followed by Chinese, Italian, Mexican, and Japanese. Popular venues other than restaurants are bars, cafes, bakeries, and pubs.
- Through ANOVA hypothesis test - restaurants' lifespan and its status were strongly associated with low p-value well below 0.05.
- According Pearson Correlation - general positive sentiments and revenues had very minor positive linear relationship at correlation coefficient at 0.08 but not significant enough that one quantitative variable affects the other.

### Classification Performance
Utilized three different machine learning algorithms in solving classification problem.
- **Random Forest** (Bagging approach) - Used Randomize Search Cross Validation in finding most appropriate parameters for random forest model which resulted precision score of **85%** and recall of **66%** with overall F1-score of **80.1%**
- **AdaBoost** (Sampling distribution) - Yielded F1-score of **77%**, lower than random forest's accuracy but it provided lower false positives at **40.5%**, decrease from Random Forest's false positives at **42%**
- **Gradient Boosting** (Learning through residual error) - Using GridSearchCV, it yielded overall accurarcy result at **79.9%** with false positives at **36.9%**.

Random forest and Gradient Boosting algorithm gave the best outcome in classifying restaurants as open or closed, although random forest had the highest accuracy rate; gradient boosting model is ideal for this particular classification problem because it had the lowest false positive rate as we don't want lenders to misclassify financially unhealthy restaurants as healthy restaurants.

## Further Readings
[Full Report](https://github.com/Suykim21/capstone_one_business_status_classifier/blob/main/reports/consolidated_report.ipynb)

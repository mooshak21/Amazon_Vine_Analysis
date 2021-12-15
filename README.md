# **Amazon Vine Analysis**

## **Overview**
> For this project we are looking at a dataset of Amazon reviews for sports data. These reviews are written by people within the Amazon Vine program which requires a paid subscription. The Amazon Vine program allows manufacturers and publishers to acquire reviews for their products. Our goal is to analyze the data to see if the positive or negative reviews are affected by the reviewers status of being in the program or not. We will be completing this analysis using PySpark since we are dealing with large datasets. In Google Colab, we will perform the ETL process to get the specific data we need for tables in our SQL database which we have imported a schema for. We will use AWS functionalities like RDS to create a database instance which will connect to our SQL database locally. 
---

## **ETL Process**

Full Reviews Table Data with columns of interest
![](https://github.com/mooshak21/Amazon_Vine_Analysis/blob/main/Resources/VineTable.png)

Dataframe with helpful votes > 20 to avoid divide by 0 errors
![](https://github.com/mooshak21/Amazon_Vine_Analysis/blob/main/Resources/GreaterThan20.png)

Further filtered dataframe with helpful vote percentage > 50%
![](https://github.com/mooshak21/Amazon_Vine_Analysis/blob/main/Resources/HelpfulVotesPercent.png)

Full Reviews Table Data with columns of interest
![](https://github.com/mooshak21/Amazon_Vine_Analysis/blob/main/Resources/VineTable.png)

Dataframe including Vine members
![](https://github.com/mooshak21/Amazon_Vine_Analysis/blob/main/Resources/PartOfVine.png)

Dataframe including Non-Vine members
![](https://github.com/mooshak21/Amazon_Vine_Analysis/blob/main/Resources/NotPartOfVine.png)

---

## **Results** 
* How many Vine reviews and non-Vine reviews were there?

    Vine Reviews
    
    * There were only 94 reviews by members of the paid Amazon Vine program.

    non-Vine Reviews
    
    * There were 40471 reviews from non-Vine members.

* How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars? What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

    5 Star Vine Reviews

    
    * There were only 48 five star reviews by members of the paid Amazon Vine program. Which makes up 51.06% of the five star reviews.


    5 Star non-Vine Reviews

    
    
    * There were 15663 five star reviews from non-Vine members. Which makes up 38.7% of the five star reviews.


**One Star Reviews**


---

## **Summary** 
Based on the results of our Vine review analysis, we can see that the factor of being paid or not may have an impact on Amazon members leaving positive reviews on video games. While majority of the reviews came from non-Vine members, of the portion of reviews that came from Vine members only one gave a one star review and about 51% of these members gave five star reviews. As for the non-Vine members, only about 38% of these customers gave a five star review and about 25% of them gave a one star review. These results should be considered when determining how well a video game actually did, since it seems there is a slight bias when a customer leaves a review and is apart of the Vine program but, these members were only a small proportion of these reviews so we can say that most of these reviews were genuine in terms of the game's performance.
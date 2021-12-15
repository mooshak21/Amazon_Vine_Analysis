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

**Vine members full summary**
![](https://github.com/mooshak21/Amazon_Vine_Analysis/blob/main/Resources/InkedVineFullSummary.jpg)

**Non-Vine members full summary**
![](https://github.com/mooshak21/Amazon_Vine_Analysis/blob/main/Resources/InkedNonVineFullSummary.jpg)

* How many Vine reviews and non-Vine reviews were there?
    * Indicated in the red circles on both images, there are 334 and 61614 reviews for Vine and Non-Vine members respectively.

* How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars? 
    * Indicated in the blue circles on both images, there are 139 and 32665 5-star reviews for Vine and Non-Vine members respectively.
  
* What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
    * Indicated in the green circles on both images, percentage of 5-star reviews are 41.62% and 53.02% for Vine and Non-Vine members respectively.
---

## **Summary** 
Based on our results, we can see that there isn't much of a positivity bias with reviews coming from Vine members. Being a paid member of the program seems to give a lower percentage of 5-star ratings so I am assuming that members that in this group give a harsher and more critical review of the products.

One additional analysis that we could do is to include all data rather than focusing on data with a helpful_vote percentage > 0.5. There was no real reason to be focusing on that data, so if we ran a report on all vote data, it might give more insight into the biases of being within this program. 

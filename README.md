# Amazon_Vine_Analysis_Challenge

Analyze Amazon reviews of toys for an interested client using PySpark to extract the data, transform it, and load the data into pgAdmin. Then analyze the data to determine if there is any bias towards favorable reviews from Vine members. Amazon Vine members recieve products from companies and then are required to publish reviews. Customers who purchase items and can then choose to write testimonials based on their experiences on their own volition. This excersise will determine if the number of 5-star reviews is impacted by paid reviews from Vine members. For this trial, the reviews for toys are being tested for bias.   

## Pre-Analysis Work
Before the reviews could be analyzed for bias, the data from Amazon had to be extracted and transformed. To do so, the data was formed into a dataframe which was then used to extract tables of extracted data that were then queried in PGAdmin. Below are examples of the data from deliverable 1 being extracted, transformed, and loaded in PGAdmin.

### Dataframe Creation

![Deliverable_1_Dataframe](https://user-images.githubusercontent.com/88064181/143669878-b1342952-0447-4a0a-acd3-78584ed94973.png)

### Tables being Transformed
![Deliverable_1_Customers_table](https://user-images.githubusercontent.com/88064181/143669881-98d357b5-b871-4a67-8de1-75596929f1f5.png)
![Deliverable_1_Products_Table](https://user-images.githubusercontent.com/88064181/143669886-552108e6-cdfa-4ebb-b261-1499786c0eb8.png)
![Deliverable_1_Vine_table](https://user-images.githubusercontent.com/88064181/143669891-1a8e28eb-b3ff-4f9c-af4a-ec41ead8d603.png)

![Deliverable_1_Review_table](https://user-images.githubusercontent.com/88064181/143669888-b8f98abb-73ec-4109-9528-f010124ebc94.png)

### Data being Loaded
[Deliverable_1_PgAdmin_tables](https://user-images.githubusercontent.com/88064181/143669896-1991a487-e75d-463f-9a32-cd72b960c064.png)


## Results

The data was parsed down to limit the pool of reviews that were being checked for bias. First, the data was analyzed to figure out how many reviews had 20 or more votes on whether is was helpful or not. While this is a good way to sort the data, it does not really tell us the type of bias. Next the reviews were sorted down to only those where 50% of people reading the reviews or more said if the review was helpful. 

![Deliverable_2_20_or_more_votes](https://user-images.githubusercontent.com/88064181/143669903-f81feb24-eb31-453b-b273-5831872bd293.png)

![Deliverable_2_Dataframe](https://user-images.githubusercontent.com/88064181/143669905-89d97db1-c15f-4983-9db0-f2cafeb812bc.png)

### Vine Reviews vs Non-Vine Reviews (50% or more said helpful) 

In total, 63294 reviews had 50% or more people say it was helpful. Of those reviews, 1266 were paid vine reviews. The other 62028 were unpaid reviews. 
![Deliverable_2_50%_helpful](https://user-images.githubusercontent.com/88064181/143669909-a01ad72d-5975-44aa-af36-19d8246f0e61.png)

![Deliverable_2_50%_helpful_paid_vine_review](https://user-images.githubusercontent.com/88064181/143669910-d9324916-04b8-4653-9b55-0eb64563b432.png)
![Deliverable_2_50%_helpful_unpaid_review](https://user-images.githubusercontent.com/88064181/143669912-ea6f5a81-5eb6-4578-801e-66982d8093b8.png)

### 5-Star Reviews Totals

To further look into bias, the reviews were then parsed down to the total number of 5-star reviews which was 30414 reviews in total. Of these 5-star reviews, 432 were paid vine reviews and 29982 were unpaid reviews. 


### Breakdown of 5-Start Reviews 

When looking into the breakdown of paid vs unpaid 5 star reviews, only 1.42% of the 5-star reviews were paid vine reviews. The majority of reviews, alomst 99% were unpaid. 

## Summary

I do not believe there is any bias for reviews in the Vine program based on the toy reviews analyzed. Almost 99% of 5-star reviews are unpaid and unsponsored. This is a very strong case that the toys are excellent, and people just want to write positive reviews on that. Of course, in terms of Big Data, about 30,000 5-star reviews is a relatively small data set. The sample size is too constricted to accurately compare paid vs unpaid reviews. Not only that, but limiting the type of product will limit the audience who is doing the reviews. If one were to look into beauty products, they may see much more bias based upon free samples given by companies, for example. There is always the chance of coincidence, but the more datasets that are analyzed, the more positive the bias could be. 

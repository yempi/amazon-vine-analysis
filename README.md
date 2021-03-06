# amazon-vine-analysis

## Overview
Analyzing Amazon reviews generated by the paid Amazon Vine Program to compare the quality of a review generated by a member of this program or an external review. We need to see if this paid program is affecting the review of the member, therefore, the comparison.

By identifying the percentage of 5-star rating between vine members and non-members, in this case I chose a dataset pertaining the beauty category reviews which can be found [here](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Beauty_v1_00.tsv.gz).

## Results
This dataset has 5m entries, after filtering out the less helpful reviews by sorting out the total of votes greater than 20 and percent of helpful_votes equal or greater than 50% there were only 153k entries to work with.

By coming up with this final dataset, we end up with this table:
<img width="524" alt="Screen Shot 2022-05-01 at 10 55 59 AM" src="https://user-images.githubusercontent.com/83614893/166153932-2a79e490-b3a7-422b-b43d-622404bd854f.png">

This table sorts out all the entries for the refined dataset which allows to answer important questions about whether or not the Amazon Vine Program is influential in the generation of product reviews:
- How many Vine reviews and non-Vine reviews were there?
  - We end up with 647 Vine reviews, and 74,055 non-vine reviews.
    
- How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
  - 229 out of 647 for vine reviews and 43,179 out of 74,055 for non-vine. 
  
- What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
  - A total of 35% are 5-star vine-reviews, whereas 58% of non-vine reviews are 5-star rated.

## Summary
Based on this numbers, there is no apparent bias for ratings coming from the Vine Review Program in the Beauty Category. We can conclude this by seeing the percentage of 5-star reviews that this program is producing which is 23% less than those of the non-vine members. Further analysis can be conducted in a significant amount of databases to further prove this result or refute it.

## Resources
- Google Colab
- AWS RDS
- PySpark
- Postgres/PgAdmin
- Pandas
- SQL

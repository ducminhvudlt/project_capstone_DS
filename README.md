# Capstone-Starbucks

## Project
This is a capstone project for course.

This data set contains simulated data that mimics customer behavior on the Starbucks app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks.
   
You can find the blog post link here at [viblo blog](https://viblo.asia/p/starbucks-capstone-018J2Mx14YK)
## Table Of Contents  
* <a href="#obj">Objective</a>
* <a href="#summary">Summary</a>
* <a href="#lib">Libraries</a>
* <a href="#files">Files Used </a>
* <a href="#ack">Acknowledgement</a>


<a name="obj"></a>

## Objective
Find the characteristics of customers that lead to the greatest chance of an offer being completed.

<a name="summary"></a>

## Summary of Results
* Duration of offer, income of customer and age of customer are the biggest predictors of whether a customer completes an offer. 
* The customer gender and the distribution method of the offer do not have any predictive power of whether a customer completes an offer.

From this, if we wanted to maximize the chance an offer is completed, it is best to target those with the largest incomes and older ages with offer durations that last a long time.     

<a name="lib"></a>

## Libraries
To be able to run this notebook, you need to install these libraries:
- [Pandas](https://github.com/pandas-dev/pandas)
- [Numpy](https://github.com/numpy/numpy)
- [Matplotlib](https://github.com/matplotlib/matplotlib)
- [Sklearn](https://github.com/scikit-learn/scikit-learn)

<a name="files"></a>

## Files Used

##### profile.json
Rewards program users (17000 users x 5 fields)

* gender: (categorical) M, F, O, or null
* age: (numeric) missing value encoded as 118
* id: (string/hash)
* became_member_on: (date) format YYYYMMDD
* income: (numeric)

##### portfolio.json
Offers sent during 30-day test period (10 offers x 6 fields)

* reward: (numeric) money awarded for the amount spent
* channels: (list) web, email, mobile, social
* difficulty: (numeric) money required to be spent to receive reward
* duration: (numeric) time for offer to be open, in days
* offer_type: (string) bogo, discount, informational
* id: (string/hash)


##### transcript.json
Event log (306648 events x 4 fields)

* person: (string/hash)
* event: (string) offer received, offer viewed, transaction, offer completed
* value: (dictionary) different values depending on event type
    * offer id: (string/hash) not associated with any "transaction"
    * amount: (numeric) money spent in "transaction"
    * reward: (numeric) money gained from "offer completed"
* time: (numeric) hours after start of test

<a name="ack"></a>

## Acknowledgement
I would like to thank Udacity for providing the data.

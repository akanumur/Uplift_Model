# Uplift_Model
Maximizing the incremental return of your marketing campaigns

It is very important to understand bringing the maximum return for a given budget/time/effort.

The main aim in any promotional campaign is to understand which segment of customers we should target. Do we need to target all customers.

No the reason being there are 4 main types of customer segments:
1. Customers who are going to buy you your product even without any promotional campaign. (Control Responders)
2. Customers that will not purchase if they don’t receive an offer (Control Non Responders)
3. Customers who won't purchase irrespective of the offer (Treatment Non Responsders)
4. Customers that will purchase only if they receive an offer (Treatment Responsders)

The target customers is obvious from above segments. Our target should be the Treatment Responsders as they need a nudge to buy the product.

There is one last simple thing to do. We need to identify which customers fall into which buckets. The answer is Uplift Modeling. It has two simple steps:

1- Predict the probabilities of being in each group for all customers: we are going to build a multi-classification model for that.
2- We will calculate the uplift score. Uplift score formula is:
(C:\Users\kanum\Desktop\Akshata\mini_projects\Uplift_Model\uplift_formula.png)

We will sum up the probability of being TR and CN and subtract the probability of falling into other buckets. The higher score means higher uplift.

###About the data###

we have the data of customers who received Discount and Buy One Get One offers and how they reacted. We also have a control group that didn’t receive anything.
Column descriptions are as follows:
recency: months since last purchase
history: $value of the historical purchases
used_discount/used_bogo: indicates if the customer used a discount or buy one get one before
zip_code: class of the zip code as Suburban/Urban/Rural
is_referral: indicates if the customer was acquired from referral channel
channel: channels that the customer using, Phone/Web/Multichannel
offer: the offers sent to the customers, Discount/But One Get One/No Offer
Before building the model, let’s apply our calc_uplift function to see the current uplift of this campaign as a benchmark:

###We are creating a target variable as follows :
In this example, the mapping of the classes are below:
- 0 -> Control Non-Responders
- 1 -> Control Responders
- 2 -> Treatment Non-Responders
- 3 -> Treatment Responders

By using this model, we can easily make our campaign more efficient by:
- Targeting specific segments based on the uplift score
- Trying different offers based on customer’s uplift score

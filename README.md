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
(C:\Users\kanum\Desktop\Akshata\mini_projects\Uplift Model\uplift formula.png)



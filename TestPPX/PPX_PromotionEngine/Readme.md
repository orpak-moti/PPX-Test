

# PromotionEngine 

PromotionEngine is an API that receives a list of items 
and returns for each item its new price (after discounts calculation).

## Description

The promotionEngine currently uses two 3rd parties providers (external reference as API) - Visa and Loyalty.
Each one of the promotion providers gets the item with its original price and returns the discount.


Each one of the providers expose two methods :

1. __*GetItemDiscount*__ - Gets the item and its original price and returns its discount.

2. __*GetDiscountableItemIds*__ - Returns the ids of items that have discount (each call will return the same ids)


#### Catalog:

1. The catalog of items that are supported is from ids 1-13.
2. Discount for item can be calculated by one provider/all providers/none of them
3. The item total discount is the sum of all the calculated discounts  
4. In case of failure/connection issue/any error from the provider = no discount on the item.
5. Items with the same id will get the same discount from the provider
6. The new price returned value should be original price - total item discounts (in case of no discount it should be the original price)


## Expectations

*	Current implementation contains a few bugs and performance issues that should be fixed 
*	The code should be production ready
*	The code should be changed to be more extensible in order to allow us easily to connect to more providers 
	in the future  

  
Good Luck!
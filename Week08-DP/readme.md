# 433B - Kuriyama mirai's stones


The solution to this problem can be found by making a cummulative list for both scenarios. Then using the list we can find the sum within the boundary by subtracting cummulative sum at the right boundary by the cummulative sum before the left boundary(Sum[r]-Sum[l-1]). This is because Sum[l-1] contains the sum before(beyond) the boundary exclusively, while Sum[r] contains both the sum before the boundary and within the boundary. Subtracting Sum[r] by Sum[l-1] eliminates the like term which is the sum before the boundary and therefore resulting in only sum within the boundary.


http://codeforces.com/contest/433/submission/44937748





# 913C - Party Lemonade


The solution to this problem can be found by first making an optimal list from the given list. If the price of 2 1L bottles is cheaper than 1 2L bottle, then it is optimal to buy 2 1L bottles instead, hence we will change the price of c[i] to c[i-1]. After doing so, we then realize that the price at the end will be the most bang for your buck, regardless of whether it is made up of smaller bottles or 1 bottle. Naturally, we may think that we just need to grab the bottle with the most bang for your buck then, however that may not be the case. It is possible that we may find cheaper alternatives with enough L of lemonade for our needs, and so we will compare the previous price and the current price to find the cheaper price. Current price can be calculated by adding sum(previous sum + bottles needed x price) + L(liter of lemonade needed left after subtracting L of bottles needed) x price. Bottles needed is the maximum amount of bottles i we can use to cover as much L of lemonade that is left, but not more than L. This will go on until we finally have our cheapest combination.


https://codeforces.com/contest/913/submission/44937988

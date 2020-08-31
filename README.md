# 121.-Best-Time-to-Buy-and-Sell-Stock


```C#
  public class Solution {
    public int MaxProfit(int[] prices) {
        int minBuyPrice = Int32.MaxValue;
        int maxProfit = 0;
        
        foreach(var p in prices){
            if(p < minBuyPrice)
                minBuyPrice = p;
            else  if(p - minBuyPrice > maxProfit)
                maxProfit = p - minBuyPrice;
        }
        
        return maxProfit;
    }
}
```

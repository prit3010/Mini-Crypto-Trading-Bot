# Mini-Crypto-Trading-Bot
This is a very small trading bot that I created just to start learning the basics of applying technical analysis using Python 
and understanding the functions in the **ta** library

## **Technical Analysis**<br />

Buying Condition:
  1. For Stochastics, both the K&D line above 20 and below 80 after the K&D line both hit below 20
  2. RSI above 50
  3. MACD line crosses the Signal Line (Difference must be positive)
  
 Selling Condition:
 1. For Stochastics, both the K&D line above 20 and below 80 after the K&D line both hit above 80
2. RSI below 50
3. Signal line crosses the MACD Line (Difference must be negative)

## **Rationale** <br />
### **Stochastics** <br />
Stochastics is useful in showing when a stock has gone into the overbought or oversold region.

Formula for the K line:<br />
$$K = 100 \times \dfrac{CP - L14}{H14 - L14}$$

where:<br />
CP = Most recent closing price <br />
L14 = Lowest price of the 14 previous trading sessions <br />
H14 = Highest price of the same 14 previous trading sessions <br />

Formula for the D line:<br />
$$D = 100 \times \dfrac{H3}{L3}$$

where:<br />
L14 = Lowest price of the 3 previous trading sessions <br />
H14 = Highest price of the same 3 previous trading sessions <br />

When K & D goes over the 80 line, it is overbought and has to be sold and likewise if it goes below 20, it is oversold and hence needs to be bought.

Hence, once it hits **below 20 or above 80**, there is a trigger to either buy or sell.

### **RSI** <br />
RSI is a momentum indicator that measures magnitude of recent price change to see if it is overbought or oversold.

### **MACD** <br />
Moving Average Convergence Divergence(MACD) is a trend-following momentum indicator showing the relationship between two moving averages of a security's prices. 
There are two lines. One would be the Signal line and the other would be the MACD line. In this algorithim, we are looking for the 2 instances when MACD > Signal to BUY as 
this indicates a bullish movement and MACD < Signal to SELL as it indicates a bearish movement


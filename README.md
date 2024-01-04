# Fed-Sentiment-and-Interest-Rates
Using Sentiment Analysis to Understand Future Federal Funds Rate Changes. 

![image](https://github.com/CSomers3/Fed-Sentiment-and-Interest-Rates/assets/88598207/aa932fd7-1ebc-44d0-9423-7ff030cb4aa6)

This was my undergraduate thesis in Economics. I have included both the final write-up and the code.

## Abstract

This study investigates the information value of the Federal Open Market Committee (FOMC)
meeting minutes and their potential to provide systematic indications for future policy decisions.
I apply Natural Language Processing techniques to the meeting minutes to identify information
that is not apparent through traditional quantitative measures. I then estimate a Taylor-Rule
model that incorporates the sentiment of the meetings to analyse Fed Funds Rate changes
between March 1996 to February 2023. My findings suggest that this information can explain
future interest rate changes beyond what is explained by traditional macroeconomic variables. 

## Code Overview:

**1. Scraper** - Employs multi-threading to find the Fed minutes release dates and the subsequent releases (publically available [here](https://www.federalreserve.gov/monetarypolicy/fomc_historical_year.htm)). This method downloads all historic & recent minutes and adds paragraph labels for later cleaning. Relies heavily on the work of [JonnyFLDN](https://github.com/JonnyFLDN) with only some minor adjustments.

**2. Preprocessing** - This program removes punctuation, tokenises, tags & lemmatizes the entire content. 

**3. Quant Analysis** - Final cleaning, removing junk text. Performance of basic sentiment analysis using the dictionary method. Finally, estimating an ordered probit model with robustness tests (macroeconomic specifications (i.e Taylor Rule comparisons), Alternative Sentiment Measurements (FinBERT), and Shifts in Textual Sample over Time (ZLB exclusion)). 

---
date: 2023-06
entities: 
- Huobi
- HT
- TRX
- DOGE
title: "Uncovering Wash Trading and Market Manipulation on Huobi"
---

## Summary
1. Recent data reveals a **surge in manipulative practices** and **liquidity issues** within Huobi's trading volume since June 2023.
2. **Trade Size Analysis:** Increased activity from volume-generating trading algorithms was detected, preceding public concerns about exchange solvency.
3. **Token Manipulation:** Huobi's founder and exchange-linked tokens (HT, TRX) were subject to manipulation, resulting in inflated trade volumes and token prices via transaction size adjustments.
4. **Wash Trading Criteria:** Synchronized fluctuations in volume distribution skewness and fitting estimates have been observed across multiple spot markets (COMP, SOL, LINK, SUI, DOGE).
5. **Retail Transaction Clustering:** The absence of retail transaction clustering highlights Huobi's artificial trading volume and indicates a clear lack of genuine retail presence.
6. **Potential Market Manipulation:** Insights into Huobi's order book reveal potential manipulation of its native token (HT), emphasizing the need for user caution.

## Metrics used

### Abnormal activity indicator - Average transaction size

Buyers and sellers generate numerous transactions across various crypto market platforms every minute. The transaction size is a critical parameter that offers insights into market participants, such as liquidity providers, retail traders, and exchanges.

![doge-usdt volume metrics](img/huobi-investigation/tx-size-doge.png)
![ht-usdt volume metrics](img/huobi-investigation/tx-size-ht.png)
![sol-usdt volume metrics](img/huobi-investigation/tx-size-sol.png)
![sui-usdt volume metrics](img/huobi-investigation/tx-size-sui.png)

<p style="text-align: center;">Average transaction size, volume, and trade count on multiple Huobi spot market over time, June - July 2023</p>

The primary sign of abnormal activity is significant spikes in average transaction size, which ordinarily exhibits inherent volatility. Low standard deviation values found across multiple Huobi's spot markets, coupled with substantial fluctuations in average transaction size, strongly indicate dominant artificial trading activity in tokens like DOGE, HT, SOL, SUI.

![doge-usdt avg tx size comparison across multiple exchanges](img/huobi-investigation/doge-avg-tx-huobi-coinbase-binance-okx.jpg)
<p style="text-align: center;">Average transaction size on DOGE/USDT spot market across multiple exchanges, May - July 2023</p>

### Order printing bots - Volume distribution tail and skewness

Further volume analysis uncovers intriguing patterns. Ideally, trading volume should follow a [power law](https://en.wikipedia.org/wiki/Power_law) heavy tail distribution, where small trades are common, and large trades are rare.

![comp-usdt distribution comparison](img/huobi-investigation/comp-distribution-binance-huobi.png)
![comp-usdt distribution comparison](img/huobi-investigation/sol-distribution-binance-huobi.png)
<p style="text-align: center;">Trade volume distribution samples comparison, COMP and SOL tokens on Huobi and Binance, July 2023</p>

A tail exponent less than 3 is expected in traditional financial markets.

![ht-usdt exponent](img/huobi-investigation/exponent-ht.png)
<p style="text-align: center;">Volume distribution fitting indicator, HT/USDT spot market on Huobi, July 2023</p>

The tail exponent here cannot be viewed in isolation but does spotlight individual traders placing high-volume orders and trading bots executing trades of identical sizes.

![comp-usdt exponent comparison between huobi and binance](img/huobi-investigation/exponent-comp-binance-huobi.png)
![doge-usdt exponent comparison between huobi and binance](img/huobi-investigation/exponent-doge-binance-huobi.png)
![sol-usdt exponent comparison between huobi and binance](img/huobi-investigation/exponent-sol-binance-huobi.png)

<p style="text-align: center;">Volume distribution fitting indicator, various spot markets on Huobi and Binance over time, July 2023 </p>

Typical volume distribution in traditional markets is asymmetrical, with more small-size trades, implying skewness greater than 1. The observed data from Huobi does not follow this pattern, suggesting manipulation.

![skewness parameter of different markets](img/huobi-investigation/skewness-huobi.jpg)
<p style="text-align: center;">Skewness of trade volume distribution for different Huobi spot markets over time, June - July 2023 </p>

![trx-usdt skewness comparison between huobi and binance](img/huobi-investigation/skewness_binance_huobi.png)
<p style="text-align: center;">Skewness comparison between Huobi and Binance for TRX/USDT spot market over time, May - July 2023 </p>

Below zero skewness values can be spotted visually. They indicate volume manipulation practicies.


### Real users presence - Spotting round-size trades

Recently published [research](https://twitter.com/adamscochran/status/1687959096316542976) hints at Huobi's insufficient funds to cover user obligations, leading to wash trading and manipulation. Matching real retail users to reported volumes can be achieved in several ways.

![clustering student test with 100x rounding](img/huobi-investigation/sui-clustering-test-huobi-coinbase.png)
<p style="text-align: center;">Student's clustering test for 100x rounding, sui-usdt spot market, comparison between Huobi and Coinbase, July 2023</p>

Assuming that retail investors often use round values for trading, the retail clustering indicator compares the frequency of round volumes (100, 200, etc.) with the frequency of use of other trade sizes. A higher value of this metric represents a higher probability of the presence of real users. In Huobi's case, this metric shows extremely low values.


### Huobi Token - Unveiling Huobi's controlled price dynamics

An exchange's native token, like Huobi's HT, is often seen as an unofficial health indicator. Since exchanges aim to boost their affiliated tokens to attract customer attention, the token's price may be subject to manipulation.
 

![ht-usdt buy/sell volume ratio comparison](img/huobi-investigation/ht-usdt-buy-sell-volume-multiple-exchange-comparison.jpg)

<p style="text-align: center;">Buy/sell ratio of Huobi Token on Huobi, Poloniex and Gate.io, May - July 2023  </p>

The ratio of "buy" volume to "sell" volume determines price behavior and its future movements. In normal conditions, this metric is very volatile and appears random (see Gate.io). On the contrary, Huobi Token demonstrates abnormal buy-sell ratio stability that fluctuates within a narrow range.

This suggests potential manipulation, as Huobi may seek to exert control over token price movements. Notably, Huobi's possession of user order data further raises concerns about market manipulation, impacting its users.
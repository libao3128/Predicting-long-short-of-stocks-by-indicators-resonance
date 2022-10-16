## Appendix
### Table
**Table 1.** 
| Indicator                                    | Formulas                                                                      |
| -------------------------------------------- | ----------------------------------------------------------------------------- |
| Simple Moving Average(SMA)                   | $\frac{C_t+C_{t-1}+...+C_{t-n}}{n}$                                           |
| Weighted Moving Average(WMA)                 | $\frac{nC_t+(n-1)C_{t-1}+...+C_{t-9}}{n+(n-1)+...1}$                          |
| Exponential Moving Average(EMA)               | $EMA(k)_t=EMA(k)_{t-1}+\alpha\times(C_t-EMA(k)_{t-1}), \alpha=\frac{2}{k+1}$  |
| Stochastic K%                                | $\frac{C_t-LL_{t-(n-1)}}{HH_{t-(n-1)}-LL_{t-(n-1)}}\times100$                 |
| Stochastic D%                                | $\frac{\sum_{i=0}^{n-1}K_{t-i}}{10}%$                                         |
| Moving Average Convergence Divergence (MACD) | $MACD(n)_{t-1}+\frac{2}{n+1}\times(DIFF_t-MACD(n)_{t-1})$                     |
| CCI (Commodity Channel Index)                | $\frac{M_t-SM_t}{0.015D_t}$                                                   |
| A/D (Accumulation/Distribution) Oscillator   | $\frac{H_t-C_{t-1}}{H_t-Lt}$                                                  |
| Larry William’s R%                           | $\frac{H_n-C_t}{H_n}-L_n \times100$                                           |
| Relative Strength Index (RSI)                | $100-\frac{100}{1+(\sum_{i=0}^{n-1}UP_{t-i}/n)/(\sum_{i=0}^{n-1}DW_{t-i}/n)}$ |
| Momentum                                     | $C_t-C_{t-9}$                                                                 |


$C_t$ is the closing price, $L_t$ is the low price and $H_t$ is the high price at time $t$.
$LL_t$ and $HH_t$ implies lowest low and highest high in the last t days, respectively.$DIFF_t=EMA(12)_t-EMA(26)_t$, where $EMA$ is the exponential moving average. $M_t=\frac{H_t+L_t+C_t}{3}, SM_t=\frac{\sum_{i=1}^{n}M_{t-i+1}}{n}, D_t=\frac{\sum_{i=1}^{n}|M_{t-i+1-SMt}|}{n}.$
$UP_t$ is upward price change while $DW_t$ is downward price change at time $t$. 

**Table 2.**
| Indicator                                    | True if | False if    |
| -------------------------------------------- | ---- | --- |
| Simple Moving Average(SMA)                   | $C_t>SMA(10)_t$     |$C_t\leq SMA(10)_t$      |
| Weighted Moving Average(WMA)                 | $C_t>WMA(10)_t$     | $C_t\leq WMA(10)_t$    |
| Exponential Moving Average(EMA)               | $C_t>EMA(10)_t$     | $C_t\leq EMA(10)_t$    |
| Stochastic K%                                | $K(10)_t>K(10)_{t-1}$     | $K(10)_t\leq K(10)_{t-1}$    |
| Stochastic D%                                |$D(10)_t>D(10)_{t-1}$      | $D(10)_t\leq D(10)_{t-1}$    |
| Moving Average Convergence Divergence (MACD) |$MACD(10)_t>MACD(10)_{t-1}$      | $MACD(10)_t\leq MACD(10)_{t-1}$ |
| CCI (Commodity Channel Index)                |$CCI(10)_t<200$ or$-200\leq CCI(10)_t\leq200$ and $CCI(10)_t>CCI(10)_{t-1}$      | $CCI(10)_t>-200$ or$-200\leq CCI(10)_t\leq200$ and $CCI(10)_t\leq CCI(10)_{t-1}$    |
| A/D (Accumulation/Distribution) Oscillator   |$AD(10)_t>AD(10)_{t-1}$      | $AD(10)_t\leq AD(10)_{t-1}$    |
| Larry William’s R%                           | $R(10)_t>R(10)_{t-1}$      | $R(10)_t\leq R(10)_{t-1}$    |
| Relative Strength Index (RSI)                |$RSI(10)_t<30$ or$30\leq RSI(10)_t\leq70$ and $RSI(10)_t>RSI(10)_{t-1}$      | $RSI(10)_t>70$ or$30\leq RSI(10)_t\leq70$ and $RSI(10)_t<RSI(10)_{t-1}$    |
| Momentum                                     |$MOM(10)_t>0$      | $MOM(10)_t\leq0$    |
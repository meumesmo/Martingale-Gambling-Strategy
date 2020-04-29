# Martingale Gambling Stategy

## Introduction
In this report, we discuss the Martingale gambling strategy applied to the game of roulette. The essence of this strategy lies in the bettor starting every session by placing a bet on black (or red, however, this must remain consistent, since red and black are even money bets). If the bettor loses, they double the bet for the next spin, until he/she wins. At this point the bettor would be in profit of one bet, and would start over again.
It would be pragmatic to assume that this strategy is flawed, since the casinos of the world are still in business. However, on giving it a more critical thought, reveals two main limitations of this gambling strategy:
1.	Limitation of initial funds
2.	Limitation of maximum bet size
Based on our experiments below, we will discuss the first limitation in greater detail.

## Experiment 1 – Infinite Funds

The approach we will adopt is called the Monte Carlo simulation where the idea is to run a simulator over and over again with randomized inputs and observe the aggregate results.
To begin, we run the simulation 10 times and track the winnings. On starting from $0 and plotting all the winnings, we notice the following trend:

Figure 1. In this figure, we observe a sample of 10 runs 
for the gambling simulation for experiment 1.

It is observed that some of the runs show a very heavy deviation from the target of $80 in winnings initially. However, eventually, with enough bets (>175) the winnings converge at the target of $80. This chart portrays an ideal strategy to winning with a probability of 100% over an extended number of bets and infinite funds. In order to better understand this phenomenon, we calculate the mean of the winnings over 1,000 runs and 1,000 subsequent bets for each run.
 
Figure 2. In this figure, we observe the mean of winnings and upper and lower bounds 
(+/- 1 standard deviation) of 1,000 runs of the martingale gambling strategy for experiment 1.

On plotting the mean of the winnings of over 1,000 runs of the martingale gambling strategy with an upper and lower bound set at +/- one standard deviation ($18.1), we observe that the estimated expected value of our winnings is $71.2, which means that on an average the bettor would win ~90% of their target goal by employing this gambling strategy. This estimated expected value is derived by aggregating the mean across the 1,000 simulations. The probability of winning $80 within 1,000 sequential bets is 100%, since all the simulations eventually converge to the target. The standard deviation (upper and lower bound) of the winnings shows a volatile nature, however, it eventually converges as the number of bets increases. This is on the account of high probability of the simulations reaching the target of $80 in winnings. Since the betting stops once the target is achieved, the standard deviation tends to converge. 
 
Figure 3. In this figure, we observe the median of winnings and upper and lower bounds 
(+/- 1 standard deviation) of 1,000 runs of the martingale gambling strategy for experiment 1.
Furthermore, on plotting the median of the winnings over 1,000 simulations, we notice a steady increase in the median value of the winnings, until the target is achieved. The aggregated median value is $80, even though there is an observed volatility with the upper and lower bounds of standard deviation. This signifies that holding the conditions of infinite funds and infinite bet size, this strategy can effectively converge to a 100%-win probability.

## Experiment 2 – Finite Funds
The above strategy works really well. One of the primary reasons for this is we are allowing the gambler to use an unlimited bank roll. On simulating a more realistic scenario in which the gambler has an allocated maximum bank roll of $256, a number of interesting observations are made.

 
Figure 4. In this figure, we observe the mean of winnings and upper and lower bounds 
(+/- 1 standard deviation) of 1,000 runs of the martingale gambling strategy for experiment 1.

On plotting the results of 1,000 simulations with a fixed bank roll of $256, the probability of achieving the target is observed to be 50.3%. This probability is derived by looking at the proportion of simulations that achieved the target of winning $80. The estimated expected value of our winnings can be derived from the aggregated mean of the winnings. This value comes out to be -$78.6. This value is negative as a good proportion of larger bets gives negative returns. This skewed set of observations can be further explained by an observed standard deviation to $166.7 from the mean. The standard deviation tends to reach a maximum value and then stabilizes instead of converging. This can be attributed to the fact that there is only a slightly better than even chance of this strategy succeeded on a limited bank roll of $256.
 
Figure 5. In this figure, we observe the median of winnings and upper and lower bounds 
(+/- 1 standard deviation) of 1,000 runs of the martingale gambling strategy for experiment 2.

The median of the winnings for experiment 2 shows that the winnings increase steadily as the number of bets increases. Thus, the probability of winning gets better with more bets. However, this observed higher aggregated median as compared to the aggregated mean can be attributed to the observed winnings being skewed to the left with a lot more frequent and steeper losses as compared to wins. This in part can be explained by the strategy of resetting to the initial bet on winning a session.

## Conclusion
Thus, we have successfully simulated the martingale gambling strategy in roulette, and understood its performances / returns in an ideal environment with infinite funds, as compared to a realistic environment with finite funds.


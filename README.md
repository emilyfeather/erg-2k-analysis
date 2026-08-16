# erg-rankings-analysis
I extracted the 2,000 fastest 2k times for both female and male rowers from Concept2's 2026 official rankings and have performed some analysis to answer some of my own thoughts and questions.

I wondered whether this dataset would display bunching at times just below round numbers, where athletes had set goals and calculated precise splits to hold throughout the 2000m to beat specific 'goal times' (as I knew this was something I personally do!). It was pretty obvious at the 7 minute mark for the men, and for the 8 minute mark for women - bunching at times faster than this was slightly less obvious as a result of fewer athletes being able to achieve such fast times.

<img src="goal_bunching_by_sex.png" alt="2k times cluster under round-number barriers" width="600">

I performed a test on the bunching at faster times in order to determine whether they were likely to be statistically significant. I figured that the best way of doing this was to essentially zoom in on the data immediately either side of the barrier to determine what the general trend of the data was (which I approximated to be linear), and then use a binomial test to determine whether the fluctuation 2s below the round number was out of the trend.

# erg-2k-analysis
## Do rowers' 2km erg times bunch at round numbers? An analysis of 4,000 Concept2 2km scores

<img src="goal_bunching_by_sex.png" alt="2k times cluster under round-number barriers" width="600">

I scraped the 2,000 fastest 2k times for men and 2,000 for women from Concept2's
official 2025 rankings, and asked a question about my own behaviour: Do
athletes target round number goal times, calculate the exact splits, and hold
them? (I know I try to!)

## Findings
- Clear bunching just below 7:00 for men and 8:00 for women — 3× more
  athletes in the 5s below the barrier than the 5s above (p < 0.001,
  binomial test).
- Bunching at faster barriers was weaker — fewer athletes reach those times,
  so both the crowds and the statistical power shrink.
- Cube law finding: top-100 men average 64% more power than the top-100 women,
  so the speed gap is only 18%
- Athletes reach peak speed in their 20s (both men and women)

## Method
Scraped the public rankings with pandas (rate-limited), cleaned times to
seconds and converted to watts, queried with SQLite, plotted with Matplotlib.
To test bunching I estimated the local trend from data flanking each barrier
(approximately linear over ±15s), used it as the null proportion, and ran a
binomial test on the split across the barrier, Bonferroni-corrected for
multiple comparisons.

## Limitations
- Rankings are self-selected — athletes choose to rank, so slow tails are
  underrepresented.
- The scrape covers the top of each ranking; comparisons are made between groups of
  different depth (top-100 men contains a greater no. of elite athletes to the top-100
  women, so not mean vs mean).

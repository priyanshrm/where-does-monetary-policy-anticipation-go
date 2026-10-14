# Where Does Monetary Policy Anticipation Go?

**Overnight rate control and bank demand in RBI term liquidity auctions, India (2001–2025)**

Priyansh Mahendra · Ahmedabad University

---

## In one paragraph

When the Reserve Bank of India (RBI) changes the repo rate, the market sometimes sees it coming and sometimes doesn't. This project asks where that anticipation shows up. Using 25 years of RBI data, I find that the interbank (call money) rate follows expected and surprise changes about equally: there is no difference at monthly frequency, and only a one-day difference at daily frequency that does not survive a correction for testing several horizons. The RBI's own aggregate liquidity operations don't give a robust explanation either. The clearer pattern is on the bank side. In daily term auction data from October 2013 to March 2022, banks asked to borrow much less term money from the RBI, and offered much more of their spare cash for term placement, in the days around cuts the market expected. They did not do this around surprise cuts. The pattern is not mirrored before expected hikes and goes the wrong way in two of the three 2025 cuts, which turned out to be as interesting as the pattern itself. I read the result as consistent with a **maturity-based "pressure valve"**: the RBI's corridor anchors today's overnight rate, while term auctions give banks another place to express their view on where policy is going. I do not claim that term auctions *cause* the call rate to stay stable.

## Four things you might learn here

1. **Banks position on what they expect the central bank to do, and they do it at term.** An overnight loan matures before a decision a few days away; a 14-day one stretches across it. If a rate cut is coming, a bank with spare cash has a reason to place it for 14 days *today* rather than overnight. On ₹1,000 crore, a 0.25% cut is worth at most about ₹9.6 lakh over 14 days. This is an incentive, not a guaranteed gain: term auctions are variable-rate, so banks cannot count on receiving the old repo rate.
2. **The same question gives different answers at different frequencies.** Monthly call money data shows no difference between expected and surprise moves. Daily data shows a one-day difference that fades. Bank-level auction bids show a large, coherent difference.
3. **Accepted amounts are not a clean measure of what the central bank chose.** In variable-rate auctions the RBI sets the terms and available quantity, but banks choose how much to bid. In about 56.4% of variable-rate repo auctions (2013–March 2022), every submitted bid was accepted, so the quantity was set by bank demand.
4. **Patterns in financial markets can stop holding.** A behaviour that holds for every expected cut in 2015–2019 disappears in 2022–2025, and has no clear mirror for hikes. Testing a finding on new data is what tells you whether it is a rule or a feature of one period.

---

## The basics (if you're new to this)

Every day, some banks end up short of cash and others have extra. They sort this out by borrowing from each other or by dealing with the RBI.

| Term | What it means |
|---|---|
| **Repo rate** | The interest rate at which the RBI lends to banks, with government bonds as security. This is the "policy rate" in the news. |
| **Reverse repo / SDF** | The RBI *borrowing* from banks: banks park spare cash with the RBI and earn interest. Since April 2022 this is mainly done through the Standing Deposit Facility (SDF), which became the floor of the policy corridor. |
| **Call money rate (WACR)** | The rate banks charge *each other* for overnight loans. It is the RBI's operating target: liquidity management aims to keep it close to the repo rate. |
| **LAF** | Liquidity Adjustment Facility: the umbrella name for the RBI's repo and reverse repo operations. |
| **Overnight vs. term operations** | Overnight operations last one day. Term operations last longer, usually 7 or 14 days. Only a term operation stretches across a rate change, so only term operations can carry a position through a decision. |
| **Fixed-rate vs. variable-rate operations** | In fixed-rate operations the RBI sets the price. In variable-rate auctions banks bid both an amount and a rate, so expectations can show up in either. This project studies amounts. |
| **Bids vs. accepted amounts** | What banks *asked for* versus what the RBI *allotted*. Comparing the two separates bank demand from RBI allotment. |
| **Pass-through** | The change in the call money rate divided by the change in the repo rate (1.0 = it moved by exactly the same amount). |
| **Expected vs. surprise** | Before each RBI meeting, economists forecast the decision. If the RBI did what the forecast said, the move was *expected*; otherwise it was a *surprise*. Off-cycle moves count as surprises. |

**How the RBI's framework changed over the sample** (so one label doesn't mean the same thing throughout):

- **September 2014:** overnight fixed-rate repo access combined with 14-day variable-rate term repo auctions and fine-tuning operations.
- **February 2020:** a 14-day variable-rate repo or reverse repo operation became the main tool for frictional liquidity, supported by shorter fine-tuning and longer operations when needed.
- **April 2022:** the SDF replaced the fixed-rate reverse repo as the standing absorption facility.

---

## The questions

The project asks three questions in sequence, each motivated by the answer to the last.

| # | Question | Main answer |
|---|---|---|
| 1 | Does the call money rate follow expected and surprise repo changes differently? | No clear persistent difference |
| 2 | If not, is the RBI offsetting expected moves through its aggregate LAF operations? | Not robustly established |
| 3 | Do banks change the *maturity* of their liquidity demand around expected moves? | Yes, most clearly in term bids around expected cuts |
| – | Does the pattern reverse for hikes? | No clear mirror in the available sample |

---

## What I found

### 1. The call money rate does not follow expected moves differently

**Monthly.** Pass-through is the change from the month before a decision to the month after, divided by the repo change.

| | Expected | Surprise |
|---|---|---|
| Number of changes (2001–2025, clean events) | 15 | 39 |
| Mean pass-through after one month | 1.25 | 1.21 |
| Median pass-through after one month | 1.17 | 1.10 |
| Difference significant? | No (Mann–Whitney p = 0.73; Welch p = 0.91) | |

![Monthly pass-through](figures/monthly_passthrough.png)

**Daily.** Average pass-through over the 1, 3, 7, 11, 17 and 23 trading days after a decision, against the five trading days before it. In the cleaner forecast-based sample (2013–2025, 15 expected and 15 surprise events):

| Window (trading days) | Expected mean | Surprise mean | Welch p-value |
|---|---|---|---|
| 1 | 1.449 | 0.668 | 0.017 |
| 3 | 1.199 | 0.902 | 0.312 |
| 7 | 0.968 | 0.678 | 0.411 |
| 11 | 1.061 | 0.718 | 0.286 |
| 17 | 1.131 | 0.839 | 0.333 |
| 23 | 1.172 | 0.747 | 0.154 |

Expected moves pass through more strongly on the first trading day, but the gap is gone by day 3. With six horizons tested, a conservative Bonferroni correction lifts the day-1 p-value from 0.017 to about 0.10. In the broader 2005–2025 sample no horizon is significant (every p > 0.40). So anticipation may touch the very first day of adjustment, but there is no clear evidence of a persistent difference.

![Daily pass-through](figures/daily_passthrough.png)

### 2. The RBI's aggregate liquidity response is not a robust explanation

If anticipation doesn't move the call rate, perhaps the RBI offsets it through LAF. The evidence is mixed:

- **14-calendar-day design** (8 expected and 23 surprise cuts through March 2022): after expected cuts the median is about ₹19,910 crore *less* net injection per 0.25% cut, versus about ₹554 crore *more* after surprise cuts (Mann–Whitney p = 0.018; p = 0.016 excluding the 2020 cuts; Welch p = 0.095).
- **Alternative design** (5-trading-day baseline, several post-decision windows): no expected-versus-surprise difference for cuts or hikes (every p > 0.13).

Because the two designs disagree, the paper does not claim a systematic extra RBI response. There is also an identification problem: aggregate LAF quantities are outcomes of both RBI auction design and bank bidding.

Splitting the historical series by operation type points to the term side. The fixed-rate component (the closest available proxy for the overnight side) shows no clear difference for cuts (p = 0.132). The variable-rate component shows a large one (p = 0.001), but many surprise cuts happened before variable-rate term operations existed in the data, so that p-value is partly zeros by construction. It is a pointer, not evidence.

### 3. Around expected cuts, banks repositioned before the decision

Daily data from October 2013 to March 2022 (the period when term operations existed and the data is complete). Medians per 0.25% cut, 6 expected and 8 surprise cuts:

| | Expected cuts | Surprise cuts | p-value |
|---|---|---|---|
| Change in bids to **borrow** term money from the RBI | −₹31,646 crore | −₹508 crore | 0.020 |
| Change in bids to **park** term money with the RBI | +₹18,518 crore | −₹3,039 crore | 0.014 |
| Change in term repo **accepted** | −₹30,760 crore | −₹808 crore | 0.020 |
| Change in term reverse repo **accepted** | +₹16,893 crore | −₹2,808 crore | 0.010 |

Details that make this more than a correlation:

- **It starts before the decision.** Borrowing bids fall and parking bids rise from about 3–4 days before expected cuts. Parking peaks on decision day and fades over two weeks, as the 7–14 day deposits mature.
- **It's driven by banks, not the RBI.** Amounts the RBI accepted move almost one-for-one with what banks bid, the number of auctions held was similar for both groups, and in about 56.4% of variable-rate repo auctions every bid was accepted.
- **It appears only at term.** The overnight-side proxy shows no clear difference, because a one-day loan doesn't stretch across the rate change.
- **All four series move the same way.** With four related tests, a strict Bonferroni threshold is 0.0125, under which only term reverse repo accepted amounts pass on its own. The case rests on the coherent pattern, not on any single p-value.

![Bids and accepted amounts around rate cuts](https://github.com/priyanshrm/where-does-monetary-policy-anticipation-go/blob/main/fig4_bids_vs_accepted.png?raw=true)

**What a bank treasury might be doing** (an interpretation of aggregate behaviour, not an observation of any bank's motives):

- *Expected cut:* a bank that needs funds soon can delay or shorten term borrowing, since cheaper funding is coming. A bank with spare cash has more reason to place it at term before overnight returns fall.
- *Surprise cut:* nobody can reposition the days *before* an event they didn't expect, so the term bid shift is much smaller.
- *Expected hike:* the mirror (borrow early, delay placement) is costlier, because pre-funding uses collateral and balance sheet before the cash is needed.

### 4. The pattern doesn't hold everywhere

**Hikes (4 expected, 6 surprise).** Before an expected hike, banks should do the opposite (borrow more at the old low rate, park less). They don't:

| | Expected hikes | Surprise hikes | p-value |
|---|---|---|---|
| Change in borrowing bids | −₹1,683 crore | +₹1,239 crore | 0.746 |
| Change in parking bids | – | – | 0.748 |
| "Positioning score" (hikes) | ₹9,852 crore | ₹17,795 crore | 0.476 |
| "Positioning score" (cuts, for comparison) | ₹98,013 crore | ₹0 | 0.022 |

The positioning score is positive when banks move in the direction anticipation predicts: less borrowing and more parking for cuts, more borrowing and less parking for hikes.

Possible reasons the hike side shows nothing, none of them separated here:

1. The expected-hike sample is tiny, so power is weak.
2. A hike can be a surprise in *size* but not in *direction* (e.g. 50 bp when 25 bp was expected), so the binary label blurs the contrast.
3. Balance sheet costs are asymmetric: preparing for a cut can mean postponing borrowing, while preparing for a hike means early collateralised borrowing.
4. Banks may express a hike view through the *rate* they bid rather than the *amount*. This study only looks at amounts.
5. The framework changed in 2022 (the SDF), and the data doesn't allow a comparable post-2022 absorption measure.

**2025 cuts (beyond the paper).** Two of the three expected cuts in 2025 go the *wrong* way. Possible reasons, none tested here:

- since 2022 the SDF gives banks a flexible overnight place to park cash, and it isn't in this data;
- in 2025 banks were short of cash and needed to borrow regardless.

![Mirror test: cuts vs. hikes](https://github.com/priyanshrm/where-does-monetary-policy-anticipation-go/blob/main/fig5_mirror_test.png?raw=true)

So the cut-side pattern looks like a feature of 2015–2019 rather than a general rule, and the hike asymmetry is an open research problem.

---

## Interpretation and policy implications

The three results fit together as a **maturity-based pressure valve**. The current overnight rate is anchored by the corridor, standing facilities and fine-tuning operations. Term operations let banks adjust over horizons that span a future decision, so anticipation can show up in term demand without today's overnight rate having to carry all of it. The phrase is an institutional reading, not a causal estimate: nothing here shows that removing term auctions would make the call rate deviate more.

Three implications, all conditional:

1. Separating the overnight implementation problem from the market's view of the future path helps keep the overnight rate tied to the current policy rate.
2. Auction design matters. Expectations can appear in bid quantity *and* bid price, so bids, accepted amounts, cutoff rates and the distribution of bid rates should be studied together.
3. The easing result should not be assumed to work symmetrically in tightening. If the hike asymmetry survives better data, the RBI may need to rely more on active fine-tuning when liquidity becomes unexpectedly tight.

---

## What this does *not* show

- **Small samples.** The key comparisons rest on 6 expected and 8 surprise cuts; the hike test on 4 and 6.
- **Many tests.** Several horizons and related outcomes were tested. The day-1 call money result does not survive a six-test correction, and some term-bid p-values do not survive a four-test correction. Individual p-values between 0.01 and 0.05 should be read with caution.
- **No causality.** The study shows *where* the expected-versus-surprise difference appears, not what would happen without term auctions. That would need an instrument or natural experiment affecting access to term operations.
- **Quantities only.** Bid rates and cutoff rates in variable-rate auctions are not analysed, so a price response can't be separated from a quantity response.
- **Incomplete picture of liquidity.** Bond purchases (OMOs), foreign-exchange swaps and the SDF also move liquidity, as do government cash balances, tax dates, reserve maintenance, quarter-end effects and currency demand. None are controlled for.
- **Changing regimes.** The operating framework changes materially over the sample, and the effect is not interacted with regime indicators.
- **Imperfect labels.** Market forecasts exist only from 2013. Forecast-based labels are the cleanest sample. For earlier scheduled decisions the daily analysis relies on news-based judgement of whether direction and size were anticipated, and the monthly analysis codes anything without a forecast as a surprise, even though many were probably expected. Direction-versus-size surprises are not separated.

This is an exploratory study, not a final answer. **Natural next steps:** a continuous surprise measure from OIS, bid-rate and cutoff-rate analysis, regime interactions, controls for autonomous liquidity, and exact or randomisation inference for the small samples.

---

# Data Sources

| Dataset | Period | Source |
|---|---|---|
| RBI repo rate decisions, with market consensus forecasts | 2000–2026 | [Moneycontrol economic calendar](https://www.moneycontrol.com/economic-calendar/india-rbi-interest-rate-decision/4870699) |
| Weighted average call money rate (monthly) | 1991–2026 | [RBI DBIE](https://dbie.rbihub.in/tables/weighted-average-call-money-rates) |
| Daily LAF operations: bids, amounts accepted, rates, tenors | April 2001–2026 | [RBI Database on Indian Economy](https://data.rbi.org.in/BOE/OpenDocument/2409211437/OpenDocument/opendoc/openDocument.jsp?logonSuccessful=true&shareId=1) |
| Daily weighted average call/notice money rates | 2005–2026 | [RBI DBIE – Markets](https://dbie.rbihub.in/markets?table=financial_markets.r50_daily_weighted_average_call_notice_money_rates) |

**Cleaning steps worth knowing about:**

- **Mixed units.** Repo rates appear as both percentages (8.25) and decimals (0.055); they were put on one scale.
- **Duplicate rows.** Two overlapping sources repeat 2013–2015 decisions; duplicates were dropped.
- **Missing moves.** Eight RBI moves between October 2006 and November 2008 are missing from the repo file and were added from RBI records.
- **Name swap.** Before 29 October 2004, the RBI used "repo" and "reverse repo" with the *opposite* meanings. The LAF data was corrected for this, and a November 2004 jump in the repo file caused by the renaming (not a policy move) was dropped.
- **Outstanding amounts.** Each LAF operation is counted as outstanding until it matures, so one 14-day operation isn't treated like fourteen overnight ones. Repo operations count as liquidity injection and reverse repo as absorption. The same logic is used to rebuild outstanding term bids and accepted amounts.

---

## Method

A simple **event study**: for each RBI decision, compare what happened just before it with what happened just after, then compare expected decisions with surprise ones.

- **Monthly call money rate:** the change from the month before a decision to the month after, divided by the size of the repo change. Only "clean" events are used (no other repo change in the following month).
- **Daily call money rate:** average over the 1, 3, 7, 11, 17 and 23 trading days after a decision minus the average of the five trading days before it, divided by the repo change. Decision day is excluded because announcements happen during the day. Events are kept only if no other repo change falls in the 23-day window, and observations where the call rate moves by more than five times the repo change are dropped.
- **Aggregate liquidity:** two designs. (1) Average amount outstanding over the 14 calendar days after each decision minus the 14 days before, scaled per 0.25% move. (2) A five-trading-day baseline against post-decision windows of 1, 3, 5, 7, 11, 17 and 23 trading days.
- **Bank demand:** the same 14-day design applied to outstanding term repo bids, term repo accepted, term reverse repo bids and term reverse repo accepted, to separate what banks asked for from what the RBI allotted.
- **Statistics:** medians and the Mann–Whitney U test, which compares groups by rank and isn't thrown off by a few extreme events. Welch t-tests are reported alongside, and Bonferroni corrections are used to judge results across several horizons or outcomes.

---

## Repository contents

```
├── main.ipynb      # full analysis: data cleaning, tests and plots
├── name.tex        # the paper (LaTeX)
├── figures/        # plots used in the paper
└── README.md
```

## Reproducing the results

1. Download the datasets from the links above (the daily call money file is needed for the daily pass-through analysis).
2. Install the Python packages:
   ```
   pip install pandas numpy scipy matplotlib openpyxl
   ```
3. Set the file paths at the top of `main.ipynb` (`REPO_FILE`, `CALL_FILE`, `LAF_FILE`) and run all cells from the top.

---

## Related work

**Central bank auctions and policy expectations**

- Ayuso, J. and Repullo, R. (2001). Why did the banks overbid? An empirical model of the fixed rate tenders of the European Central Bank. *Journal of International Money and Finance*, 20(6), 857–870.
- Linzert, T., Nautz, D. and Breitung, J. (2003). Bidder behavior in repo auctions without minimum bid rate: Evidence from the Bundesbank. Deutsche Bundesbank Discussion Paper 13/2003.
- Bindseil, U. (2002). Equilibrium bidding in the Eurosystem's open market operations. ECB Working Paper 137.
- Bindseil, U., Nyborg, K. G. and Strebulaev, I. A. (2002). Bidding and performance in repo auctions: Evidence from ECB open market operations. ECB Working Paper 157.
- Carpenter, S. B. and Demiralp, S. (2006). Anticipation of monetary policy and open market operations. *International Journal of Central Banking*, 2(2), 25–63.
- European Central Bank (2001). The liquidity management of the ECB. *Monthly Bulletin*, October.

**Pass-through, liquidity and expectations in India**

- Sander, H. and Kleimeier, S. (2006). Expected versus unexpected monetary policy impulses and interest rate pass-through in euro-zone retail banking markets. *Journal of Banking & Finance*, 30(7), 1839–1870.
- Goyal, A. and Agarwal, D. K. (2020). Policy transmission in Indian money markets: The role of liquidity. *The Journal of Economic Asymmetries*, 21.
- Charmal, V. and Goyal, A. (2021). Liquidity management and monetary transmission: empirical analysis for India. *Journal of Economic Studies*, 49(5), 850–875.
- Goyal, A. and Parab, P. (2021). Effectiveness of expectations channel of monetary policy transmission: Evidence from India. IGIDR Working Paper 2021-011.
- Lakdawala, A. and Sengupta, R. (2025). Measuring monetary policy shocks in emerging economies: Evidence from India. *Journal of Money, Credit and Banking*, 57(2–3), 407–437.
- Lakdawala, A. and Sengupta, R. How do RBI's actions and words affect financial markets? *Ideas for India*.
- Gupta, M., Pawar, A., Kumar, S., Borad, A. and Seet, S. K. (2024). Equity markets and monetary policy surprises. RBI Working Paper 03/2024.

**RBI framework documents**

- Reserve Bank of India (2016). *Operating Procedures and Liquidity Management Framework of the RBI*.
- Reserve Bank of India (2020). *Annual Report 2019–20*, Chapter III, Monetary Policy Operations.
- Reserve Bank of India (2022). *Statement on Developmental and Regulatory Policies*, April 8 (introduction of the SDF).

**What's new here.** The European Central Bank saw a similar pattern in its own auctions in the early 2000s: banks bid less when cuts were expected and more when hikes were expected. Liquidity conditions and policy expectations are each well studied for India. The contribution of this project is to trace one sequence for India: whether expected and surprise changes differ in call rate pass-through, whether any similarity can be attributed to a different aggregate RBI response, and whether the remaining adjustment appears in bank demand across overnight and term facilities.

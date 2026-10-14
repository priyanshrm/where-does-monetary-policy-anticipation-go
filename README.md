# Do Banks Position for Expected RBI Rate Moves?

**Call money pass-through and LAF liquidity around expected and surprise repo rate changes in India (2001–2025)**

Priyansh Mahendra · Ahmedabad University

---

## In one paragraph

When the Reserve Bank of India (RBI) changes the repo rate, the market sometimes sees it coming and sometimes doesn't. This project asks whether that makes a difference. Using 25 years of RBI data, I find that the interbank interest rate follows both kinds of change equally within a month. But daily data on banks' borrowing from and lending to the RBI tells a different story: in 2015–2019, a few days before rate cuts the market expected, banks stopped borrowing short-term money from the RBI and rushed to lend it their spare cash for one to two weeks, locking in the old, higher interest rate before it fell. The pattern is clear in that period, but it does not reverse before rate hikes and does not repeat in 2025, which turned out to be as interesting as the pattern itself.

## Three things you might learn here

1. **Banks trade on what they expect the central bank to do.** If a rate cut is coming next week, a bank with spare cash can lend it to the RBI for 14 days *today* and earn the old, higher rate for all 14 days. On ₹100 crore, a 0.25% cut is worth about ₹9.6 lakh to get ahead of.
2. **Monthly data can hide what daily data shows.** Monthly interest rates show no difference between expected and surprise moves. Daily auction data shows banks clearly repositioning in the days just before expected cuts.
3. **Patterns in financial markets can stop holding.** A behaviour that holds for every expected cut in 2015–2019 disappears in 2022–2025. Testing a finding on new data is what tells you whether it is a rule or a feature of one period.

---

## The basics (if you're new to this)

Every day, some banks end up short of cash and others have extra. They sort this out by borrowing from each other or by dealing with the RBI.

| Term | What it means |
|---|---|
| **Repo rate** | The interest rate at which the RBI lends to banks, with government bonds as security. This is the "policy rate" in the news. |
| **Reverse repo / SDF** | The RBI *borrowing* from banks: banks park spare cash with the RBI and earn interest. Since April 2022 this is mainly done through the Standing Deposit Facility (SDF). |
| **Call money rate (WACR)** | The rate banks charge *each other* for overnight loans. The RBI aims to keep it close to the repo rate. |
| **LAF** | Liquidity Adjustment Facility: the umbrella name for the RBI's repo and reverse repo operations. |
| **Overnight vs. term operations** | Overnight operations last one day. Term operations last longer, usually 7 or 14 days. Only a term operation stretches across a rate change, so only term operations can lock in a rate. |
| **Expected vs. surprise** | Before each RBI meeting, economists forecast the decision. If the RBI did what the forecast said, the move was *expected*; otherwise it was a *surprise*. |

---

## The question

> Does the money market respond differently to repo rate changes the market expected than to those that surprised it?

I look in two places:

1. **The call money rate.** Does it follow expected and surprise changes differently?
2. **Banks' dealings with the RBI.** Do banks borrow and park money differently around expected and surprise decisions?

---

## What I found

### 1. The call money rate follows both kinds of change fully within a month

Pass-through is the change in the call money rate divided by the change in the repo rate (1.0 = it moved by exactly the same amount).

| | Expected | Surprise |
|---|---|---|
| Number of changes (2001–2025, clean events) | 15 | 39 |
| Median pass-through after one month | 1.17 | 1.10 |
| Difference significant? | No (p = 0.73) | |

Monthly data is too coarse to see any difference in *speed*.

### 2. Around expected rate cuts, banks repositioned before the decision

Daily data from October 2013 to March 2022 (the period when term operations existed and the data is complete), per 0.25% cut:

| | Expected cuts | Surprise cuts | p-value |
|---|---|---|---|
| Change in bids to **borrow** term money from the RBI | −₹31,600 crore | −₹500 crore | 0.020 |
| Change in bids to **park** term money with the RBI | +₹18,500 crore | −₹3,000 crore | 0.014 |

Three details make this more than a correlation:

- **It starts before the decision.** Borrowing bids fall and parking bids rise from about 3–4 days before expected cuts. Parking peaks on decision day and fades over two weeks, as the 7–14 day deposits mature.
- **It's driven by banks, not the RBI.** Amounts the RBI accepted move almost one-for-one with what banks bid, and the number of auctions held was similar for both groups.
- **It appears only in term operations.** Overnight operations show no difference, because a one-day loan doesn't stretch across the rate change.

![Bids and accepted amounts around rate cuts](https://github.com/priyanshrm/bank_positionsing_before_rate_cuts/blob/main/fig4_bids_vs_accepted.png)

### 3. The pattern doesn't hold everywhere

- **Hikes:** before an expected hike, banks should do the opposite (borrow more at the old low rate, park less). They don't (p = 0.48).
- **2025 cuts:** two of the three expected cuts in 2025 go the *wrong* way.

So this looks like a feature of 2015–2019, not a general rule. Possible reasons, none of them tested here:
- since 2022 the SDF gives banks a flexible overnight place to park cash, and it isn't in this data;
- in 2025 banks were short of cash and needed to borrow regardless;
- some 2022 "surprise" hikes were surprises only in size, not direction.

![Mirror test: cuts vs. hikes](https://github.com/priyanshrm/bank_positionsing_before_rate_cuts/blob/main/fig5_mirror_test.png)

---

## What this does *not* show

- **Small samples.** The key comparisons rest on 6 expected and 8 surprise cuts.
- **Many tests.** Across the project many comparisons were run, so individual p-values between 0.01 and 0.05 should be read with caution.
- **Incomplete picture of liquidity.** Bond purchases (OMOs), foreign-exchange swaps and the SDF also move liquidity and aren't in the data.
- **Imperfect labels.** Market forecasts exist only from 2013. Earlier changes without a forecast are treated as surprises, even though many were probably expected.

This is an exploratory study, not a final answer.

---

## Data

| Dataset | Period | Source |
|---|---|---|
| RBI repo rate decisions, with market consensus forecasts | 2000–2026 | [Moneycontrol economic calendar](https://www.moneycontrol.com/economic-calendar/india-rbi-interest-rate-decision/4870699) |
| Weighted average call money rate (monthly) | 1991–2026 | [RBI DBIE](https://dbie.rbihub.in/tables/weighted-average-call-money-rates) |
| Daily LAF operations: bids, amounts accepted, rates, tenors | April 2001–2026 | [RBI Database on Indian Economy](https://data.rbi.org.in/BOE/OpenDocument/2409211437/OpenDocument/opendoc/openDocument.jsp?logonSuccessful=true&shareId=1) |

**Cleaning steps worth knowing about:**

- **Mixed units.** Repo rates appear as both percentages (8.25) and decimals (0.055); they were put on one scale.
- **Duplicate rows.** Two overlapping sources repeat 2013–2015 decisions; duplicates were dropped.
- **Missing moves.** Eight RBI moves between October 2006 and November 2008 are missing from the repo file and were added from RBI records.
- **Name swap.** Before 29 October 2004, the RBI used "repo" and "reverse repo" with the *opposite* meanings. The LAF data was corrected for this, and a November 2004 jump in the repo file caused by the renaming (not a policy move) was dropped.
- **Outstanding amounts.** Each LAF operation is counted as outstanding until it matures, so one 14-day operation isn't treated like fourteen overnight ones.

---

## Method

A simple **event study**: for each RBI decision, compare what happened just before it with what happened just after, then compare expected decisions with surprise ones.

- **Call money rate:** the change from the month before a decision to the month after, divided by the size of the repo change.
- **Liquidity:** average amounts outstanding over the 14 days after each decision minus the 14 days before, scaled per 0.25% move.
- **Statistics:** medians and the Mann–Whitney U test, which compares groups by rank and isn't thrown off by a few extreme events. Welch t-tests are reported alongside.

---

## Repository contents

```
├── main.ipynb      # full analysis: data cleaning, tests and plots
├── name.tex        # the paper (LaTeX)
├── figures/        # plots used in the paper
└── README.md
```

## Reproducing the results

1. Download the three datasets from the links above.
2. Install the Python packages:
   ```
   pip install pandas numpy scipy matplotlib openpyxl
   ```
3. Set the three file paths at the top of `main.ipynb` (`REPO_FILE`, `CALL_FILE`, `LAF_FILE`) and run all cells from the top.

---

## Related work

- Ayuso, J. and Repullo, R. (2001). Why did the banks overbid? An empirical model of the fixed rate tenders of the European Central Bank. *Journal of International Money and Finance*, 20(6), 857–870.
- Linzert, T., Nautz, D. and Breitung, J. (2003). Bidder behavior in repo auctions without minimum bid rate: Evidence from the Bundesbank. Deutsche Bundesbank Discussion Paper 13/2003.
- Sander, H. and Kleimeier, S. (2006). Expected versus unexpected monetary policy impulses and interest rate pass-through in euro-zone retail banking markets. *Journal of Banking & Finance*, 30(7), 1839–1870.
- Lakdawala, A. and Sengupta, R. How do RBI's actions and words affect financial markets? *Ideas for India*.

The European Central Bank saw a similar pattern in its own auctions in the early 2000s: banks bid less when cuts were expected and more when hikes were expected. This project looks for the same behaviour in India's LAF.

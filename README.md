# Customizing Emily’s Superannuation Plan: Strategic Analysis and Recommendations for Achieving a Comfortable Retirement 
This report presents a comprehensive assessment of Emily's current superannuation strategy and its alignment with her long-term retirement goals.

The report is structured into four main sections. 
- Section 1 evaluates the current fund allocation and assesses its risk-return profile.
- Section 2 examines the sufficiency of Emily's contributions based on her projected income, taxation, and superannuation inputs.
- Section 3 presents the projection methodology used to estimate the future value of Emily's superannuation fund under uncertainty.
- Section 4 applies multi-scenario analysis to evaluate how different career paths and income shocks may impact Emily's retirement outcome and recommends fund allocation adjustments to strengthen financial resilience.

The superannuation portfolio is diversified across three funds: 
- 40% in the conservative HarbourSafe Bonds Fund.
- 30% in the Balanced Horizon Mix Fund.
- 30% in the growth-oriented SkyHigh Equity Growth Fund.

The methodology uses salary projections and expected fund performance; the analysis estimates her total contributions and portfolio growth until age 65. Additional projections for government pension and annual living costs from 30 to 90 were also conducted to estimate whether the remaining money is sufficient for the retirement goal.

The original and best-case projection result shows that Emily can meet her retirement goal with the significant remaining money. On the other hand, the projected superannuation balance may fall short of supporting her envisioned retirement lifestyle in the worst case, in which she might lose her job during her working years. Therefore, the report recommends reallocation using an optimization model to increase Emily's assets.

In conclusion, while Emily's current strategy is sufficient for her long-term goal, adjustments in contribution and investment strategy are necessary to ensure financial security and flexibility in retirement.

# Section 1: Emily’s Current Investment Allocation and Risk-Return Assessment
The primary objective of the part is to evaluate Emily’s current investment allocations and assess the balance between risk and return. Based on each fund’s historic ten-year average growth rate (see Table 1), volatility measures, and allocation proportions, the analysis provides an initial evaluation of whether the current allocations can meet her needs.
## Fund Characteristics
![Table 1](Images/Table%201)

*Note: Fund growth rates of HarbourSafe are calculated using the formula =NORM.INV(RAND(), 3.75%, 5.00%) is similar to Horizon and SkyHigh.*

As shown in Figure 1, the HarbourSafe Fund shows steady growth, with returns ranging from -5% to 15%, reflecting low volatility and a focus on capital preservation. This makes it suitable for investors seeking consistent returns with minimal market fluctuations for its low-risk characteristics.


![Figure 1](Images/Figure%201)

The Horizon Fund demonstrates moderate volatility, with returns between -16% and 30% (see Figure 2). It suits investors targeting higher long-term growth while managing short-term fluctuations, reflecting a balanced growth strategy.

![Figure 2](Images/Figure%202)

The SkyHigh Fund displays the widest volatility, from -40% to 58% (see Figure 3), representing high-risk, high-return characteristics. While offering strong potential growth in favorable markets, it carries significant downside risk.

![Figure 3](Images/Figure%203)

## Initial Evaluation of Emily’s Current Asset Allocation
Emily’s allocation: 70% in low-to-moderate risk funds and 30% in high-risk assets, represents a moderate risk profile that balances stability with growth potential. Given her age (30), Emily has time to tolerate greater volatility for long-term growth. As the CFA Institute (2020) notes, mixing different risk levels can balance portfolio volatility while supporting long-term performance. A slightly more growth-oriented allocation may better align with her retirement goals while managing long-term inflation and rising costs.

# Section 2: Contribution Sufficiency Assessment
This section evaluates whether Emily’s current and projected contributions are sufficient to meet her retirement goals. Following section 2 requirements, calculations here focus solely on the sum of fund contributions and exclude investment returns. 
## Total Income and Contribution Projection
A 5,000-iteration Monte Carlo simulation was conducted to project Emily’s total income over her 35-year career, starting with an annual salary of $70,000. Salary growth was modeled using a normal distribution with a mean of 3.5% and a standard deviation of 0.7% (see Table 2). After applying New Zealand income tax and ACC levies (1%–2%) (IRD, 2025), net income was calculated annually.

![Table 2](Images/Table%202)

Superannuation contributions included 3% from Emily’s salary and a 3% employer match, both adjusted for Employer Superannuation Contribution Tax (ESCT) (see Table 3), which ranged from 30% to 39% depending on the salary band. The simulation projects an average total income of NZD 3,412,661, with a 95% interval of NZD 3,268,159 to NZD 3,573,413 (see Table 4).

![Table 3](Images/Table%203)

![Table 4](Images/Table%204)

Based on these income streams, total fund contributions were calculated, producing an average contribution of NZD 245,257 by age 65, with a 95% interval of NZD 233,896 to NZD 257,336 (see Table 5).

![Table 5](Images/Table%205)

### Defining the Retirement Goal
Emily’s retirement goal targets a 'Choices' lifestyle, estimated at NZD 39,975 annually in 2024 values. To account for future inflation, a beta distribution was fitted using New Zealand inflation data from 1990 to 2025 (Stats NZ, 2025), as shown in Figure 4.

![Figure 4](Images/Figure%204)

Assuming Emily lives to age 90, simulated living costs were projected for both pre-retirement (ages 30–65) and retirement (ages 66–90). The average total living costs over her lifetime are estimated at NZD 2,349,193 and NZD 3,269,951, respectively (see Table 6).

![Table 6](Images/Table%206)

## Sufficiency Assessment
The primary funding sources considered are:
- Inflation-adjusted New Zealand Government Superannuation (NZ Super) (see Table 7) is estimated to provide NZD 2,233,952 on average over the 25-year retirement period. It is forecasted using historical NZ Super growth data (2015–2075) through simulation.
- The average total fund balance available at age 65 is projected at NZD 517,998.
- Total average income throughout career, projected at NZD 3,414,470.
The three sources provide a total available value of NZD 6,166,420. When subtracting from the NZD 5,618,875 retirement sum required, the remaining money that Emily has is NZD 547,622. The initial analysis suggests that her desired retirement lifestyle is satisfied when money relies solely on superannuation contributions, total fund contributions, and her income, adjusted for inflation.

![Table 7](Images/Table%207)

# Section 3: Superannuation Fund Projection Methodology
## Model Overview
This section presents the methodology used to project the future value of Emily’s superannuation fund by the time she retires at age 65. Based on the net contributions already calculated in Task 2, this task focuses on how uncertainties in salary growth and investment returns are modeled to estimate the accumulated fund balance under real-world variability.
### Uncertainty Drivers in Fund Projection
**1)	Salary Growth Variability**
- Emily’s salary growth was modeled as a random variable following a normal distribution. Each year, a new growth rate was drawn based on historical averages and variability assumptions (see Section 2). This allows annual superannuation contributions to fluctuate, as salary growth directly influences contribution amounts.

**2)	Net Contributions to Fund**
- As salary growth fluctuates, Emily’s annual salary determines her applicable ESCT rate, based on IRD’s 2025 thresholds. Although ESCT brackets remain fixed, salary changes create variability in employer contributions after ESCT deductions.

**3)	Superannuation Fund Return Variability**
- Investment returns were projected based on Emily’s portfolio allocation across HarbourSafe, Horizon, and SkyHigh. Each fund’s return was modeled using the historical mean and standard deviation. In each trial, fund returns were independently drawn from normal distributions, with portfolio returns calculated as weighted averages (see Table 1).

**4)	PIR Adjustment**
- Fund returns were adjusted using Emily’s Prescribed Investor Rate (PIR), ensuring all projections reflect after-tax investment growth and accurately estimate the fund balance at retirement.
### Year-by-Year Projection Structure
For clear instructions about how the projection table was created in Excel, a sample table was provided below. (See Table 8 for the detailed formula)

**Table 8**

*The formula for the fund projection table*
| Variables | Formula |
|:-------|:------:|
Personal Contribution (PC) |	= Salary * 3%
Employer Contribution (EC) |	= Salary * 3%
ESCT |	= IFS((Salary+EC) >= 216001, 39%, (Salary+EC) >= 93721, 33%, (Salary+EC) >= 70000, 30%)
Net Contribution (NC) |	= PC + EC * ESCT
PIR rate |	= 28%
Contribution to HabourSafe at year 0 |	= NC * 40%
Annual Growth Rate for Habour Safe |	= NORM.INV(RAND(), 3.75%, 5%)
Annual Growth for Habour Safe |	= NC * 40% * NORM.INV(RAND(), 3.75%, 5%)
Growth after PIR (HabourSafe) |	= IF(Annual Growth > 0, Annual Growth * (1 - PIR))
Fund balance in HabourSafe at year 0 |	= Contribution to HabourSafe at year 0 + Growth after PIR(HabourSafe)
Contribution to HabourSafe at year 1 |	= NC of year 1 * 40% + Fund balance in HabourSafe at year 0
Contribution to Horizon at year 0 |	= NC * 30%
Annual Growth Rate for Horizon |	= NORM.INV(RAND(), 6.5%, 10.5%)
Annual Growth for Horizon |	= NC * 30% * NORM.INV(RAND(), 6.5%, 10.5%)
Growth after PIR (Horizon) |	= IF(Annual Growth > 0, Annual Growth * (1 - PIR))
Contribution to Horizon at year 0 |	= contribution to Horizon at year 0 + Growth after PIR(Horizon)
Contribution to Horizon at year 1 |	= NC of year 1 * 30% + Fund balance in Horizon at year 0
Contribution to SkyHigh at year 0 |	= NC * 30%
Annual Growth Rate for SkyHigh |	= NORM.INV(RAND(), 10.25%, 20.75%)
Annual Growth for SkyHigh |	= NC * 30% * NORM.INV(RAND(), 10.25%, 20.75%)
Growth after PIR (SkyHigh) |	= IF(Annual Growth > 0, Annual Growth * (1 - PIR))
Contribution to SkyHigh at year 0 |	= Contribution to SkyHigh at year 0 + Growth after PIR(SkyHigh)
Contribution to SkyHigh at year 1 |	= NC of year 1 * 30% + Fund balance in SkyHigh at year 0

*Note: The model is built in the attached Excel file.*

This year-by-year simulation allows the model to capture compounding effects that fixed-rate models cannot represent, providing a more realistic estimate of Emily’s fund balance variability at retirement.

## Monte Carlo Simulation Framework
The result of the projection model was executed using a Monte Carlo simulation to capture the combined effects of salary growth and fund return variability across the entire accumulation period. The simulation was conducted as follows:
Projection horizon: 35 years (Emily’s age 30–65)
- Simulation trials: 5,000 independent runs.
- Random draws: Annual salary growth rates and fund returns varied independently each year.
- Fund balance: Contributions and returns accumulated year-by-year, reflecting both varying income and market conditions.
See Table 9 for detailed simulation results

**Table 9**

*Statistics of 5,000 Simulation of compounded funds balance after 35 years*
| Summary statistics | HabourSafe | Horizon	| Skyhigh	| Funds Total |
|:-------|:------:|:------:|:------:|:------:|
Count |	5000	| 5000|	5000|	5000
Minimum|	$93,802|	$45,000|	$20,436|	$246,593|
Maximum|	$212,494|	$388,726|	$1,726,031|	$2,330,699
Mean|	$146,647|	$149,470|	$220,310|	$517,998
Standard deviation|	$19,820|	$45,345|	$141,258|	$169,111
95% C.I. on mean total income (lower)|	$146,097|	$147,360|	$216,394|	$513,309
95% C.I. on mean total income (upper)	|$147,196|	$149,841	|$224,226	|$522,686
95% P.I. on total income (lower)|	$111,824	|$80,492	|$56,155	|$313,172
95% P.I. on total income (upper)|	$187,475	|$254,014	|$631,536	|$970,159

## Model Limitations
This model assumes stable tax policies, no correlation between fund returns, and relies on historical data to estimate salary growth and fund return variability. While the inflation simulation (discussed in Section 2) was fitted using a Beta distribution, more advanced methods such as bootstrapping may further improve precision in modeling future inflation uncertainty.

# Section 4: Emily’s Superannuation Future Value Multi-Scenario Projection Evaluation
This section presents the application of the superannuation projection model described in Section 3, using Monte Carlo simulation to estimate Emily’s superannuation fund value at retirement under multiple scenarios. The model incorporates key financial variables previously established, including contributions (net of ESCT), fund allocations, growth rates, and volatilities.
## Simulating the Future Value of Emily’s Superannuation Fund
Emily’s superannuation fund projection was conducted in two primary stages:

**Stage 1: Contributions and Fund Inputs**
- Total annual contributions (both employee and employer, adjusted for ESCT) were derived from the income and tax modelling in Section 2.
  Fund allocation proportions, growth rates, and volatilities were applied based on historical fund performance.
  
**Stage 2: Monte Carlo Simulation**
- Across 5,000 simulation trials, random annual salary growth and fund returns were generated for each year over the 35-year projection period.
- In each trial, yearly fund balances were updated by adding contributions, applying portfolio allocation, calculating gross returns, deducting PIR tax to obtain net returns, and compounding forward.
- The process continued through to Emily’s retirement at age 65, producing a distribution of projected fund values across scenarios.

## Emily’s Retirement Planning: Scenario Analysis
### Base-Case Scenario: Original Plan
![Figure 5](Images/Figure%205)

The base-case scenario presents Emily’s retirement projection using the data outlined in the case background. As detailed in Figure 5, Emily is projected to meet and slightly exceed her comfortable retirement lifestyle needs, with a financial surplus that provides both economic comfort and a buffer. The 95% prediction intervals (see Figure 5) confirm a positive outlook, even under less favorable outcomes. 

### Best-Case Scenario: Optimal Career Trajectory
In this scenario, Emily achieves rapid career growth. Her salary reaches NZD 100,000 at age 35, NZD 145,000 at age 40 (Careers New Zealand, 2024), and NZD 245,000 at age 50, aligning with CTO remuneration levels (SEEK, 2025). The promotion path is based on accelerated progression strategies (Tang, 2022).
The projections (see Table 10) show that, under these assumptions, Emily comfortably exceeds her retirement target. Her personal superannuation fund, combined with NZ pension, fully covers projected retirement expenses, even under lower-return conditions. This surplus allows for greater flexibility, including earlier retirement or lifestyle upgrades.

![Table 10](Images/Table%2010)

### Worst-Case Scenario: Early Job Loss
This scenario assumes Emily loses her job at age 50. From age 51 onward, contributions stop entirely. The projections (see Table 10) reveal that early job loss substantially reduces her superannuation balance, creating a financial gap that leaves her unable to fully meet retirement expenses unless significant adjustments are made. She may need to reduce post-retirement living costs or pursue additional income sources. Even the upper bound of the 95% prediction interval remains insufficient to fully close the gap (see Table 10).
It should be noted that this scenario does not include any potential unemployment subsidies, severance payments, or other government support, as these benefits may vary based on circumstances and were excluded to maintain conservative modelling assumptions.
### Optimization Model Application
Under the worst-case scenario, an optimization model was developed to strengthen Emily’s financial resilience while respecting her limited superannuation investment scope. The model, built using Excel Solver, maximizes expected after-tax return while capping portfolio volatility at 10% standard deviation. This reallocation improves growth potential within controlled risk boundaries, helping mitigate the adverse impacts of early job loss.

# Conclusion
This report provided a comprehensive analysis of Emily's current superannuation strategy, assessing its capability to meet her ‘comfortable’ retirement lifestyle needs. The evaluation mainly used a Monte Carlo simulation to forecast total income, total fund contributions, and portfolio growth until age 65.

Findings indicate that Emily’s current portfolio is projected to meet her retirement goals in the base-case and best-case scenarios (get a promotion). At the same time, Inflation-adjusted New Zealand Government Superannuation plays an important role and accounts for the bulk of overall retirement capital. However, her personal superannuation balance could not suffice if she loses her job early.

To address potential shortfalls and enhance the ability to resist risks, the report recommended reallocating investments using an optimization model. Emily's current strategy, when considering the New Zealand Government Superannuation, shows a reasonable foundation.

However, making some strategic adjustments to her fund allocations is advisable to ensure financial security and flexibility.

---
**Collaboration in this project** *: Ken Xia, Johnson Shan, Quynh Chi Le*

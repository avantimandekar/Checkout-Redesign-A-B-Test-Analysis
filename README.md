# Checkout Redesign A/B Test Analysis
An A/B testing project to evaluate the business impact of a redesigned checkout page using customer conversion and revenue data. The goal is to identify which checkout experience delivers better results and recommend an appropriate rollout strategy based on statistical evidence.

Business Problem -
Should the business launch the redesigned checkout for all customers, roll it out only to specific customer segments, or continue using the existing checkout page?

Key Findings -
1) Overall Conversion Performance -
| **Metric** | **Control** | **Treatment** |
| Users | 15,490 | 15,510 |
| Conversions | 1,119 | 1,200 |
| Conversion Rate | 7.22% | 7.74% |
- Absolute conversion lift: +0.51 percentage points
- Relative conversion lift: +7.10%
- P-value: 0.0861
- 95% confidence interval: −0.07 to +1.10 percentage points
Insight: The redesigned checkout showed a positive conversion lift, but the result was not statistically significant at the 5% level. Therefore, an overall conversion improvement cannot be confidently established.

2) Device-Level Performance - 
| **Device** | **Control** | **Treatment** | **Difference** |
| Desktop | 7.54% | 10.13% | +2.59 pp |
| Mobile | 7.00% | 5.45% | −1.55 pp |
| Tablet | 6.55% | 5.13% | −1.42 pp |
- Desktop showed a statistically significant conversion improvement.
- Mobile showed a statistically significant conversion decline.
- Tablet showed no statistically significant difference.
- A direct comparison of desktop against mobile and tablet also indicated treatment-effect heterogeneity (p < 0.001).
Insight: The redesign does not perform equally across devices. Desktop users responded positively, while mobile users experienced lower conversion.

3) Visitor-Type Analysis -
- New visitors showed a positive conversion difference of approximately 0.20 percentage points.
- Returning visitors showed a positive difference of approximately 1.07 percentage points.
- Neither comparison was statistically significant after Bonferroni correction.
Insight: Visitor type may be worth monitoring, but the results do not support separate rollout decisions for new and returning visitors.

4) Revenue Impact -
| **Metric** | **Control** | **Treatment** |
| Revenue per User | $5.12 | $5.56 |
| Average Order Value | $63.56 | $64.51 |
- Revenue per user increase: Approximately 8.67%
- Bootstrap 95% confidence interval: −$0.03 to +$0.92
- AOV comparison p-value: 0.356
Insight: Revenue metrics showed positive estimates, but the evidence was insufficient to establish a statistically reliable improvement.

5) Rollout Scenario Analysis -
The rollout scenarios were compared using the observed device distribution and conversion rates for each device.
| **Rollout Strategy** | **Projected Conversion** |
| Existing checkout for all users | 7.23% |
| New checkout for all users | 7.71% |
| New checkout for desktop only | 8.49% |
Insight: The desktop-only rollout showed the highest projected conversion rate across all evaluated scenarios.

Tools - 
- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- SciPy
- Statsmodels
- Jupyter Notebook

Conclusion -
The new checkout had a positive overall uplift of 7.10%, however this was not statistically significant. There was an increase in revenue per user. When looking at device type, the results show different conversions depending on the treatment. The desktop users saw an improvement whereas mobile users saw a decrease. There was no statistically significant results between different types of visitors. Overall the highest projected conversion was seen when using the desktop only scenario at 8.49%. This indicates the new checkout can have differing effects based on device type with desktop users seeing a more positive effect.

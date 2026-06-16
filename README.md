# Ultramarathon Runner Age vs. Performance
## Overview
This project analyzes how age impacts finish-time performance in ultramarathon races using
publicly-available race result data. The goal is to determine whether ultramarathon performance
follows the traditional early-twenties peak model seen in most sports or whether it reflects
a distinct age curve unique to endurance events.

The analysis focuses on two key objectives:
- Visualizing how median finish times vary across age groups for both elite and general finishers
- Identifying the age profile of elite ultramarathon performers (top 10% by finish time)

---
## Methodology
### Data
- Source: TidyTuesday Ultra Trail Running Dataset (October 26, 2021)
- Filters: 100 km+ races, ages 18–80, positive finish times, binary gender (M/W)
- Dataset: 111,146 performances across 1,207 races (2012–2021)

---
### Feature Engineering
Derived variables included:
- Finish time: hours (continuous outcome) and H:MM:SS (display)
- Age group: 18–24, 25–29, 30–34, 35–39, 40–44, 45–49, 50–54, 55–59, 60–64, 65+
- Elite-tier flag: top 10% of finishers by finish time within each race × gender combination

---
### Analysis Approach
The analysis is descriptive and visual, structured around four figures:
1. Median finish time by age group — all finishers, both genders
2. Elite vs. all-finisher performance curves — side-by-side by gender
3. Age distribution of elite finishers — histogram with mean and median overlays
4. Finisher count by age group over time — stacked area chart by year

Summary statistics (median hours, mean hours, and elite percentage) were computed by age group and gender.

---
## Key Findings
- Among all finishers, the 18–24 bracket shows the fastest median times, but this group is small and highly self-selected
- Among elite finishers, performance peaks in the 30–39 age window
- The median age of an elite ultramarathon finisher is 42 for both men and women
- The 40–44 age group has the highest raw finisher count across all years
- Performance decline is gradual, becoming meaningful after age 49 for men and after 54 for women

These results suggest that ultramarathon performance does not follow the early-twenties peak model of most sports, and that physiological traits favorable to ultra-endurance, such as fat oxidation efficiency, slow-twitch fiber development, and pain tolerance, continue to develop well into the 40s.

---
## Practical Implications
### For Athletes
- Runners in their 30s and early 40s should not view age as a barrier to peak performance
- Young runners (18–24) entering 100 km+ races are underrepresented and face high variance in outcomes

### For Coaches and Sports Scientists
- Training periodization models from sprint and power sports should not be applied to ultra-endurance athletes
- Fatigue-sensitive declines are most critical to monitor after age 50 for men and 55 for women

---
## Limitations
- The dataset does not include training load, injury history, or experience level
- The 18–24 age group is too small for reliable median estimation
- External factors (course difficulty, weather, and race prestige) are not controlled for

---
## Future Work
- Apply regression analysis to formally identify age-related decline thresholds
- Incorporate experience level (number of prior ultras) as a covariate
- Extend analysis to specific race distances (100 km vs. 100 mi vs. 200+ mi)
- Develop athlete-level longitudinal models for runners with multiple race appearances

---
## Repository Structure
- `ultramarathon_copy.qmd` — Quarto file containing full analysis code and narrative
- `ultramarathon_copy.html` — Rendered HTML file with output

---
## References
- "Does Age Matter in Ultramarathon?" *Runners Connect*.
  runnersconnect.net/does-age-matter-in-ultramarathon/. Accessed 13 June 2026.
- Knechtle, Beat, et al. "Age-Related Changes in 100-km Ultra-Marathon Running Performance."
  *Age*, vol. 35, no. 3, 2013, pp. 1063–1083.
  pmc.ncbi.nlm.nih.gov/articles/PMC3682063/.
- McDougall, Christopher. *Born to Run*. Knopf, 2009.
- "Ultra Trail Running Dataset." *TidyTuesday*, 26 Oct. 2021.
  github.com/rfordatascience/tidytuesday/tree/master/data/2021/2021-10-26.
- "Why Do Ultra-Endurance Athletes Get Better with Age?" *Born on the Trail*.
  bornonthetrail.substack.com/p/why-do-ultra-endurance-athletes-get-better-with-age.
  Accessed 13 June 2026.

---
## Conclusion
This project establishes a descriptive framework for understanding the relationship between age and ultramarathon performance. The results consistently support the view that ultra-endurance athletes peak later and decline more gradually than athletes in most other sports, with elite performance centered around age 42 for both men and women.

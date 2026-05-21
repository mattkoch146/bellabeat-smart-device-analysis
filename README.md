# Bellabeat Smart Device Analysis
## Google Data Analytics Certificate — Case Study 2

---

## Business Task

Analyze smart device usage data to identify trends in how consumers use non-Bellabeat devices, and apply those insights to inform Bellabeat's marketing strategy for the **Bellabeat app**.

---

## Data Sources

- **Source:** FitBit Fitness Tracker Data provided by Mobius via Kaggle
- **License:** CC0 Public Domain
- **Link:** https://www.kaggle.com/datasets/arashnic/fitbit
- **Date Range:** April 12, 2016 – May 12, 2016 (31 days)
- **Participants:** 33 unique users
- **Tool Used:** Google Sheets for data cleaning and analysis. Power BI for visualizations.

### Files Used
| File | Users | Description |
|---|---|---|
| dailyActivity_merged | 33 | Daily steps, distance, active minutes, calories |
| sleepDay_merged | 24 | Daily sleep duration and time in bed |
| hourlySteps_merged | 33 | Steps recorded per hour |
| hourlyCalories_merged | 33 | Calories burned per hour |

### Data Limitations
- Only 33 users — too small a sample to be fully representative
- Only 31 days of data — too short to identify long-term trends
- Weight data had only 8 users — not used in analysis
- Data is from 2016 — user behavior may have changed since then

---

## Data Cleaning & Processing

Cleaning was performed in Google Sheets:

- Checked for and removed **3 duplicate rows** in `sleepDay_merged`
- No duplicates found in `dailyActivity_merged`
- Identified **77 rows with zero steps** in `dailyActivity_merged` — likely days devices were not worn, kept in dataset but noted as a limitation
- Verified date range: April 12, 2016 to May 12, 2016
- Extracted **hour of day** from `ActivityHour` column in hourly files using `=HOUR()` formula
- Calculated **average restless minutes** as the difference between average time in bed and average time asleep

---

## Analysis Summary

### 1. Daily Activity
| Metric | Value |
|---|---|
| Avg Daily Steps | 7,638 |
| Avg Calories Burned | 2,304 |
| Avg Very Active Minutes | 21 |
| Avg Fairly Active Minutes | 13 |
| Avg Lightly Active Minutes | 193 |
| Avg Sedentary Minutes | 991 |

Users average only 7,638 steps per day — below the commonly recommended 10,000. They spend over 16 hours per day sedentary, which accounts for 81% of their tracked time. Very active minutes average just 21 per day, below the CDC recommended 30 minutes of vigorous activity.

### 2. Sleep
| Metric | Value |
|---|---|
| Avg Minutes Asleep | 419 (7 hours) |
| Avg Time In Bed | 458 (7.6 hours) |
| Avg Restless Minutes | 39 |

Users get roughly 7 hours of sleep which is within the healthy range. However they spend nearly 40 minutes in bed before falling asleep, suggesting restlessness or difficulty winding down.

### 3. Hourly Activity Patterns
Peak activity hours are between **5pm and 7pm**, indicating users are most active after work. Both steps and calories burned correlate directly during these hours.

---

## Visualizations

View the full dashboard in the `Bellabeat_Dashboard.pdf` file in this repository.

Charts included:
- Daily Activity Minutes Breakdown (Pie Chart)
- Average Steps and Calories by Hour of Day (Dual Axis Combo Chart)
- Average Sleep vs Time in Bed (Bar Chart)
- Average Daily Steps vs Recommended Goal (Bar Chart)

---

## Top 3 Recommendations

**1. Hourly Movement Reminders**
Since users are sedentary 81% of the time, the Bellabeat app should send smart hourly reminders to move throughout the day. Positioning Bellabeat as a personal wellness coach that actively nudges users toward healthier habits could be a key differentiator in marketing campaigns.

**2. Pre-Peak Activity Notifications**
Since users are most active between 5-7pm, Bellabeat should send motivational push notifications around 4-5pm to encourage users to maximize their most active window of the day. Marketing messaging around "make the most of your evening" could resonate strongly with the target audience.

**3. Sleep Optimization Coaching**
Since users spend an average of 39 minutes in bed before falling asleep, Bellabeat should introduce a guided wind-down feature with breathing exercises or mindfulness prompts to help users fall asleep faster. This directly leverages Bellabeat's existing stress and mindfulness tracking capabilities and could be highlighted in marketing as a unique wellness benefit.

---

## Tools Used
- Google Sheets — data cleaning and analysis
- Power BI — data visualization
- GitHub — portfolio documentation

---

## Files in This Repository
- `README.md` — full project documentation
- [Dashboard PDF](Bellabeat_Dashboard.pdf) - Power BI dashboard export

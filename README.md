# digital-distraction-academic-performance

## Business Problem
What actually predicts whether a student thrives — their habits, their 
circumstances, or their devices?

## Dataset
15,000 synthetic student records across 18 variables (Kaggle, "Digital 
Distraction vs Academic Performance" by Neurocipher), covering study habits, 
digital behavior, sleep, mental health, and socioeconomic background. 
Synthetic data was computationally generated to mimic realistic student 
behavioral patterns, including noise and non-linear relationships.

## Notebook
`eda_models_digital_distraction.ipynb` — exploratory analysis (tier comparisons, 
quadrant breakdowns, correlation checks) and a multiple linear regression 
controlling for all 12 key variables simultaneously.

## Methodology
1. Compared performance across study-hour tiers, phone-usage tiers, and 
   study/assignment quadrants to identify candidate performance drivers
2. Tested independence between behaviors (e.g., study hours vs. assignment 
   completion) using correlation analysis
3. Built a multiple linear regression model across all 12 variables to validate 
   which factors independently predict exam scores once confounding is controlled for

## Key Findings
- Study hours are the dominant predictor (r = 0.64, regression coefficient +11.58) 
  — nearly 3× the next-highest variable; a 37-point score gap exists between 
  students studying under 2 hrs/day vs. 6+ hrs/day
- The phone is a tax, not a punishment: heavy phone use costs high-studying 
  students only 2.2 points, but costs low-studying students 6.4 points
- Social media showed almost no independent effect (coefficient −0.09) once 
  smartphone use and gaming were controlled for separately — the actual harm 
  came from those two specifically (−2.58 and −1.81)
- Mental health sets a 17-point baseline penalty before a student studies at all, 
  but doesn't change the rate of improvement from studying (second-strongest 
  predictor, coefficient +4.02)
- Assignment completion is a fully independent lever from study hours (r = 0.007) 
  — students who did both scored 25.2 points higher than those who did neither
- Internet quality and gender showed negligible effects (a 0.2-point gap across 
  the full internet-quality range), disproving an assumed digital-equity gap
- Full regression model explained 58.2% of score variance (R² = 0.582)

## Tools
Python (pandas, statsmodels, seaborn), Power BI

## How to Run
Open the notebook in Google Colab or Jupyter. Requires: pandas, statsmodels, 
numpy, matplotlib/seaborn.

## Full Case Study
[Read the full write-up on my portfolio →](your-framer-link.com/projects/digital-distraction)

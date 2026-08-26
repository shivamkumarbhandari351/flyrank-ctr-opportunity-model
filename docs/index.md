# Identifying Under-Capturing Pages: A CTR Opportunity Model

## Abstract
We investigated which search results underperform their expected click-through rate. We trained a Random Forest model on FlyRank search data to predict expected clicks based on ranking position and impressions. Comparing actual clicks to predicted clicks revealed a subset of high-visibility, low-engagement pages. The model successfully identified pages that require immediate metadata optimization. This framework allows content teams to prioritize updates based on missed traffic potential.

## Introduction / Problem Statement
Many pages rank well on search engines but fail to capture user clicks. This research builds a decision-support system to identify these pages automatically, allowing teams to update titles and meta descriptions to improve CTR.

## Data
Data was sourced from the FlyRank ML Internship dataset via Hugging Face. We utilized the core performance tables. To protect client confidentiality, all URLs and queries were anonymized. Pages with fewer than 100 impressions were excluded.

## Methodology
- **Features:** Average position, total impressions, and search volume.
- **Label:** Actual clicks.
- **Model:** Random Forest Regressor.
- **Validation:** 80/20 train-test split ensuring no data leakage. 

## Results
The model successfully flagged pages with the highest difference between predicted and actual clicks. (Insert your Python chart images here later).

## Limitations
This model provides *directional* decision support, not causal proof. We cannot guarantee that updating a title will definitively increase clicks.

## Ranked Recommendations
1. **High Priority (Top 100 missed clicks):** Immediate rewrite of Title Tags and Meta Descriptions.
2. **Monitor:** Pages performing exactly as expected.

## Reproducibility
- Code Repository: [Add your GitHub Repo Link Here]

## Acknowledgments & Data Credit
Built on the FlyRank ML Internship dataset. Data sourced from [FlyRank](https://flyrank.ai).

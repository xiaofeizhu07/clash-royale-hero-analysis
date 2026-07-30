# Hero Deck Dominance and Community Sentiment in Clash Royale

## Overview
This project analyzes the competitive impact of the hero mechanic introduced in Clash Royale in December 2025, examining whether hero-containing decks demonstrate statistically significant win rate advantages over non-hero decks across five competitive seasons (December 2025 – May 2026).

## Research Questions
1. Do hero-containing decks demonstrate statistically significant competitive advantages over non-hero decks at top ladder?
2. Does community sentiment among competitive players align with periods of statistically measured hero dominance?

## Data
- **Battle data:** 4.5 million top 1,000 ladder games scraped daily from RoyaleAPI (December 2025 – May 2026)
- **Leaderboard data:** Top 100 seasonal finisher deck compositions manually compiled from RoyaleAPI blog posts across 6 seasons
- **Sentiment data:** 3,499 filtered tweets from 11 active competitive Clash Royale players collected via Apify

## Methodology
- Hero deck detection using card ID and evolution level indicators
- Two-sample independent t-tests comparing hero vs non-hero deck win rates
- Analysis conducted at both population level (top 1,000) and elite level (top 100 finishers)
- VADER sentiment analysis with per-player baseline normalization
- Keyword frequency analysis across P2W, frustration, and quit term categories

## Key Findings
- Hero decks were statistically dominant over non-hero decks in 4 of 5 seasons examined
- Hero advantage was more pronounced among elite top 100 players than across the broader top 1,000 population
- Season 4 marked peak dominance with a 95% hero adoption rate among top 100 finishers
- Community sentiment did not linearly track hero dominance — the most statistically dominant season paradoxically showed the most positive sentiment

## Repository Structure

```
├── Code.ipynb                          # Battle data analysis pipeline
├── Sentiment Analysis.ipynb            # Sentiment analysis pipeline
├── hero_winrate_results.csv            # Population level win rate results
├── elite_winrate_results.csv           # Elite level win rate results
├── hero_usage_results.csv              # Hero usage rates by season
├── individual_hero_winrates.csv        # Individual hero win rates by season
├── sentiment_by_season.csv             # Seasonal sentiment scores
├── winrate_with_ci.csv                 # Win rates with confidence intervals
├── elite_winrate_with_ci.csv           # Elite win rates with confidence intervals
├── hero_winrate_analysis.png           # Figure 1
├── hero_usage_analysis.png             # Figure 2
├── elite_vs_population_comparison.png  # Figure 3
└── sentiment_analysis.png              # Figure 4
```


## Tools and Libraries
- Python (pandas, numpy, scipy, matplotlib, seaborn)
- VADER Sentiment Analysis
- Apify Advanced X Twitter Profile Scraper

## Author
Alex Song — Rising Sophomore, Purdue University  
Triple major: Economics, Statistics, and Philosophy

# Airbnb Bookings Analysis (EDA) - Capstone Project

![Airbnb Logo](https://img.shields.io/badge/Airbnb-Analysis-blue?style=flat&logo=airbnb) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/) [![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)

## Table of Contents
- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Business Objective](#business-objective)
- [Dataset](#dataset)
- [Installation and Setup](#installation-and-setup)
- [Usage](#usage)
- [Key Findings](#key-findings)
  - [Affordable Segment ($10–$334)](#affordable-segment-10–334)
  - [Luxury Segment ($335–$10,000)](#luxury-segment-335–10000)
- [Proposed Solutions](#proposed-solutions)
  - [Affordable Segment](#affordable-segment)
  - [Luxury Segment](#luxury-segment)
- [Conclusion](#conclusion)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

## Project Overview
This capstone project conducts an in-depth Exploratory Data Analysis (EDA) on the Airbnb NYC 2019 dataset. The analysis identifies trends in pricing, availability, room types, geographical distribution, host behaviors, and customer reviews across affordable and luxury segments. Insights are derived from 20 targeted questions (Q1–Q20) to guide strategies for improving listing performance, increasing bookings, and boosting revenue.

- **Project Type**: Individual EDA Capstone.
- **Focus**: Affordable ($10–$334) and Luxury ($335–$10,000) listings in NYC.
- **Methodology**: Data cleaning, statistical analysis, visualizations (histograms, box plots, heatmaps, pair plots), and correlation studies.

## Problem Statement
Analyze factors affecting Airbnb listing performance in NYC, emphasizing affordable and luxury segments, to optimize pricing, availability, and host management.

## Business Objective
Use data-driven insights to enhance listing appeal, elevate booking rates, and maximize revenue for Airbnb's affordable and luxury markets.

## Dataset
- **File**: `Airbnb NYC 2019.csv` (attached in the repository).
- **Source**: Public dataset (e.g., from Kaggle), capturing NYC Airbnb listings as of 2019.
- **Dimensions**: 48,895 rows × 16 columns.
- **Key Features**:
  - Identifiers: `id`, `name`, `host_id`, `host_name`.
  - Location: `neighbourhood_group` (e.g., Manhattan, Brooklyn), `neighbourhood`, `latitude`, `longitude`.
  - Listing Details: `room_type` (Entire home/apt, Private room, Shared room), `price`, `minimum_nights`, `availability_365`.
  - Engagement: `number_of_reviews`, `reviews_per_month`, `last_review`.
  - Host Metrics: `calculated_host_listings_count`.
- **Preprocessing Steps**: Handling nulls (e.g., reviews), outlier detection, categorical encoding—detailed in the notebook.

## Installation and Setup
1. Clone the repository:
   ```
   git clone https://github.com/yourusername/airbnb-bookings-analysis.git
   cd airbnb-bookings-analysis
   ```
2. Install required Python packages (via `requirements.txt`):
   ```
   pip install -r requirements.txt
   ```
   **requirements.txt**:
   ```
   pandas
   numpy
   matplotlib
   seaborn
   jupyter
   ```
3. Launch Jupyter Notebook:
   ```
   jupyter notebook "Airbnb Bookings Analysis (EDA).ipynb"
   ```

## Usage
- Open the `.ipynb` file in Jupyter.
- Execute cells step-by-step: Load data → Clean → Explore (summaries, distributions) → Visualize → Derive insights.
- Customize: Modify queries or visualizations for deeper dives (e.g., specific neighborhoods).
- Outputs: Charts, tables, and correlation heatmaps exported as images or displayed inline.

## Key Findings
Analysis based on 20 questions (Q1–Q20) reveals segment-specific trends.

### Affordable Segment ($10–$334)
- **Geographical Dominance**: Brooklyn (46.58% reviews) and Manhattan (42.17%); top neighborhoods: Williamsburg, Bedford-Stuyvesant.
- **Room Types**: Private rooms (46.39% listings, median $60) and entire homes (44.44%, median $125) lead; shared rooms lag (9.03% reviews, median $40).
- **Availability & Nights**: 36.8% listings unavailable year-round; short stays (1–3 nights) common (63.6%).
- **Host Insights**: 76.79% hosts manage 1 listing; professionals like Sonder control multiples.
- **Engagement**: High reviews in Manhattan (up to 14/month); correlations show weak price-review link (-0.04) but strong host concentration (0.66).
- **Risks**: Inactive listings (36.8%), shared room underperformance, new listing visibility issues.

### Luxury Segment ($335–$10,000)
- **Geographical Dominance**: Manhattan (66.20%) and Brooklyn (26.43%); hotspots: Midtown, Hell’s Kitchen.
- **Room Types**: Entire homes dominate (95.72% reviews, avg. $542–$1,130); private/shared rooms niche with high availability (low demand).
- **Availability & Nights**: 23.2% zero availability; long minimums rare (<0.3%).
- **Host Insights**: 67.31% single-listing hosts; operators like Blueground manage 27.3% of top listings.
- **Engagement**: Manhattan/Brooklyn = 92.63% reviews; correlations: review consistency (0.45), newer listings struggle (-0.31).
- **Risks**: Over-concentration, ghost listings (23.2%), overpricing ($10,000 outliers with 300+ days available).

## Proposed Solutions
Actionable strategies with estimated impacts.

### Affordable Segment
1. **Dynamic Pricing for Shared Rooms**: Cap at $40 median; +10% bookings ($500K fees).
2. **Reactivate Ghost Listings**: Target 36.8% in Brooklyn/Manhattan; +15% supply ($750K fees).
3. **Reposition Shared Rooms**: Convert to private; +500 listings ($500K fees).
4. **Boost New Listings**: Spotlight for 0–5 reviews; +10% engagement ($200K fees).
5. **Expand in Queens**: Recruit private room hosts; +5,000 bookings ($500K fees).
   - **Total Impact**: 10–15% growth, $2–$3M annual fees.

### Luxury Segment
1. **Focus on Core Areas**: 90% marketing for Manhattan/Brooklyn entire homes; +10% bookings ($1–$1.5M fees).
2. **Reactivate Listings**: Campaign for 23.2% inactive; +1,000 bookings ($1M fees).
3. **Reposition Rooms**: Convert private/shared to entire homes; +1,000 bookings ($1M fees).
4. **Enhance Visibility**: Program for low-review listings; +188 bookings ($188K fees).
5. **Optimize Pricing**: Cap long-stay at $1,100–$1,700; +15% occupancy ($450K fees).
   - **Total Impact**: 10–15% growth, $2.6–$3.6M annual fees.

## Conclusion
- **Affordable**: Thrives in Brooklyn/Manhattan with private/entire homes but hampered by inactivity and shared rooms. Solutions could yield $2–$3M in fees.
- **Luxury**: Concentrated in entire homes but risks overpricing and low niche engagement. Strategies may add $2.6–$3.6M in fees.
This EDA provides a foundation for data-informed decisions to strengthen Airbnb's NYC presence.

## Technologies Used
- **Programming**: Python (Pandas, NumPy).
- **Visualization**: Matplotlib, Seaborn.
- **Environment**: Jupyter Notebook, Google Colab.

## Contributing
Contributions welcome! Fork the repo, create a branch, and submit a pull request. For major changes, open an issue first.

## License
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## Author
- **Kunal Patel**
- **GitHub**: [kunalpatel]([https://github.com/yourusername](https://github.com/Kunalpatel-08)
- **Contact**: kunalpatel1538@gmail.com


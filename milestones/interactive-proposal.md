# Seiya Matsumoto

## Description

**Project Title: If America Had 100 Coins**

What if all household wealth in the United States were represented by just 100 coins?

This project aims to visualize how wealth is distributed among different groups of American households through an interactive, animated visualization.

Users will be able to select different categories, such as:

- **Wealth group:** Top 1%, Next 9%, Middle 40%, Bottom 50%
- **Race and ethnicity:** White, Black, Hispanic, Asian, and Other
- **Age:** Different age groups
- **Region:** Northeast, Midwest, South, and West
- **City:** Top 10 Cities, others

When users select a category, 100 coins will move and reorganize into groups based on their share of total U.S. household wealth. For example, if a group owns 30% of total wealth, 30 coins will move into that group's section.

The visualization will also display the population share of each group, allowing users to compare the proportion of people with the proportion of wealth they own.

The goal is to make complex wealth inequality statistics easier to understand through a simple visual metaphor and engaging interactions.

## Technical Plan re: Option A/B/C/D

**Option A: Large Interactive**

I plan to create a single interactive visualization using **D3.js, JavaScript, HTML, and CSS**.

The main feature will be the animated movement of 100 coins. Users will select a category, and the coins will transition smoothly between groups based on the underlying wealth distribution data.

I plan to use D3.js for data binding, positioning, and animated transitions. The dataset will be cleaned and aggregated using Python before being converted into CSV or JSON files for the visualization.

The main interactions will include:

- Switching between different classifications of households
- Animating the movement of coins based on wealth shares
- Displaying the percentage of population and wealth represented by each group

**Inspirations**

1. **Concept — If the World Were a Village of 100 People**

   This concept simplifies complex global statistics by imagining the world as a village of just 100 people. I would like to apply a similar approach to U.S. household wealth, using 100 coins to make the distribution intuitive and accessible.

2. **Interaction — [A Day in the Life of Americans — FlowingData](https://flowingdata.com/2015/12/15/a-day-in-the-life-of-americans/)**

   I was inspired by the way individual dots move dynamically between groups to represent people's activities. I would like to apply a similar animation technique to visualize the distribution of wealth.

## Mockup

Two mockups illustrate how the same 100 coins will be reorganized when users select different categories. The numbers shown are illustrative.

**Mockup 1: Wealth Distribution**

The first visual divides 100 coins into four wealth groups: Top 1%, Next 9%, Middle 40%, and Bottom 50%.

**Mockup 2: Generation (Age)**

The second visual shows the same 100 coins divided into four age groups: 0–20, 20–40, 40–60, and 60+. The coins will move between groups when users switch categories.

![Mockup of the proposed interactive visualization](images/sample.png)

## Data Sources

### Data Source 1: U.S. Census Bureau — Current Population Survey Annual Social and Economic Supplement (CPS ASEC)

URL: https://www.census.gov/data/datasets/time-series/demo/cps/cps-asec.html

Size: **134,729 rows and 831 columns** (2026 person-level CSV, `pppub26.csv`)

CPS ASEC provides detailed information on income, employment, and demographic characteristics. I previously used this dataset to analyze income differences across racial and ethnic groups. For this project, I plan to select relevant variables to explore economic differences across demographic groups.

### Data Source 2: Federal Reserve — Distributional Financial Accounts (DFA)

URL: https://www.federalreserve.gov/releases/z1/dataviz/dfa/

Size: **740 rows and 15 columns** (for each file:`dfa-networth-levels.csv` and `dfa-networth-shares.csv`)

The DFA provides estimates of U.S. household wealth by wealth group, age, and race/ethnicity. I used the files to analyze wealth distribution over time. For this project, I plan to use these data to calculate wealth shares and represent them as 100 coins.

## Questions

1. Is rounding wealth shares to 100 whole coins acceptable if exact percentages are also displayed?
2. Would animated transitions between different household classifications meet the expectations for Option A?

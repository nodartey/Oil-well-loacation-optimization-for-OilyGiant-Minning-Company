# Oil-well-loacation-optimization-for-OilyGiant-Minning-Company
Used linear regression to predict oil reserves across 3 regions. Selected the most profitable wells, calculated expected profit, and assessed risk using bootstrapping. Recommended the best region for oil well development based on profit and risk threshold.

This project helps **OilyGiant**, a mining company, determine the most profitable region to develop a new oil well. Using geological data from three regions, we build predictive models to estimate oil reserves, calculate profit potential, and assess risk through statistical bootstrapping.

## Project Goals

- Predict oil reserves in new wells using linear regression.
- Identify the top 200 most promising wells in each region.
- Calculate expected profit and quantify the risk of loss.
- Recommend the region with the highest profit and lowest risk.

## Dataset Description

Three datasets (one per region):

- `geo_data_0.csv`
- `geo_data_1.csv`
- `geo_data_2.csv`

Each file contains:
- `id`: unique oil well ID
- `f0`, `f1`, `f2`: features of each well
- `product`: oil reserves (in thousand barrels)

##  Methodology

1. **Data Preprocessing**
   - Loaded and cleaned the datasets.
   - Split each region's data into training (75%) and validation (25%) sets.

2. **Model Training**
   - Trained a linear regression model for each region.
   - Made predictions and evaluated performance using RMSE.

3. **Profit Calculation**
   - Selected the top 200 wells (from 500) with highest predicted reserves.
   - Calculated profit using:
     - Revenue per 1000 barrels: $4,500
     - Budget: $100 million for 200 wells
     - Break-even volume: calculated and compared to regional averages

4. **Risk Assessment (Bootstrapping)**
   - Used 1000 bootstrapped samples to estimate:
     - Average profit
     - 95% confidence interval
     - Risk of loss (probability of negative profit)

5. **Decision Criteria**
   - Selected only regions with risk < 2.5%
   - Chose region with the highest average profit among them

##  Key Assumptions

- Only linear regression is allowed for modeling.
- Development costs: $100M for 200 wells.
- Study size: 500 wells per region.
- Revenue: $4.5k per unit of product (in thousand barrels).

## Tools & Libraries

- `pandas`
- `numpy`
- `scikit-learn`
- `matplotlib`
- `seaborn`

##  Outcome

Using predictive modeling and risk analysis, we identified the most financially sound region for oil well development, balancing profitability with risk under strict investment constraints.

---




















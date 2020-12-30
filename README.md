# US Minimum Wage by State from 1968 to 2020

## The Basics
- **What is this?** In the United States, states and the federal government set minimum hourly pay that workers can receive to ensure that citizens experience a minimum quality of life. This [dataset](Minimum%20Wage%20Data.csv) provides the minimum wage data set by each state and the federal government from 1968 to 2020.

- **Why did you put this together?** While looking online for a clean dataset for minimum wage data by state, I was having trouble finding one. I decided to create one myself and provide it to the community.

- **Who do we thank for this data?** The United States Department of Labor compiles a table of this data on [their website](https://www.dol.gov/whd/state/stateMinWageHis.htm). I took the time to clean it up and provide it here for you. :)

## The Goods
This repository contains 3 primary items:
- [`Minimum Wage Data.csv`](Minimum%20Wage%20Data.csv): A cleaned dataset of US state and federal minimum wages from 1968 to 2020 (including 2020 equivalency values). The data was scraped from the [United States Department of Labor's table of minimum wage by state](https://www.dol.gov/whd/state/stateMinWageHis.htm). 
- [`1808 - Minimum Wage by State from 1968 to 2017 - R Code.Rmd`](1808%20-%20Minimum%20Wage%20by%20State%20from%201968%20to%202017%20-%20R%20Code.Rmd): The code used to clean the data
- [`CPI 1913 - 2018.csv`](CPI%201913%20-%202018.csv): A dataset containing the Consumer Price Index (CPI) values used to calculate 2020 equivalent wages. I kept the values in here so that other equivalent dollars could easily be calculated without needing to bring in a separate dataset.
 
## Description of Data
The values in the [dataset](Minimum%20Wage%20Data.csv) are as follows:
- **Year**: The year of the data. All minimum wage values are as of January 1 except 1968 and 1969, which are as of February 1.
- **State**: The state or territory of the data.
- **State.Minimum.Wage:** The actual State's minimum wage on January 1 of Year.
- **State.Minimum.Wage.2020.Dollars**: The State.Minimum.Wage in 2020 dollars.
- **Federal.Minimum.Wage**: The federal minimum wage on January 1 of Year.
- **Federal.Minimum.Wage.2020.Dollars**: The Federal.Minimum.Wage in 2020 dollars.
- **Effective.Minimum.Wage**: The minimum wage that is enforced in State on January 1 of Year. Because the federal minimum wage takes effect if the State's minimum wage is lower than the federal minimum wage, this is the higher of the two.
- **Effective.Minimum.Wage.2020.Dollars**: The Effective.Minimum.Wage in 2020 dollars.
- **CPI.Average**: The average value of the [Consumer Price Index](https://www.investopedia.com/terms/c/consumerpriceindex.asp) in Year. When I pulled the data from the [Bureau of Labor Statistics](https://www.bls.gov/cpi/home.htm), I selected the dataset with "all items in U.S. city average, all urban consumers, not seasonally adjusted".
- **Department.Of.Labor.Uncleaned.Data**: The unclean, scraped value from the [Department of Labor's website](https://www.dol.gov/whd/state/stateMinWageHis.htm).
- **Department.Of.Labor.Cleaned.Low.Value**: The State's lowest enforced minimum wage on January 1 of Year. If there is only one minimum wage, this and the value for Department.Of.Labor.Cleaned.High.Value are identical. (Some states enforce different minimum wage laws depending on the size of the business. In states where this is the case, generally, smaller businesses have slightly lower minimum wage requirements.)
- **Department.Of.Labor.Cleaned.Low.Value.2020.Dollars**: The Department.Of.Labor.Cleaned.Low.Value in 2020 dollars.
- **Department.Of.Labor.Cleaned.High.Value**: The State's higher enforced minimum wage on January 1 of Year. If there is only one minimum wage, this and the value for Department.Of.Labor.Cleaned.Low.Value are identical.
- **Department.Of.Labor.Cleaned.High.Value.2020.Dollars**: The Department.Of.Labor.Cleaned.High.Value in 2020 dollars.
- **Footnote**: The footnote provided on the [Department of Labor's website](https://www.dol.gov/whd/state/stateMinWageHis.htm). [See more below](README.md#data-footnotes).

### Data Footnotes
As laws differ significantly from territory to territory, especially relating to whom is protected by minimum wage laws, the following footnotes are located throughout the data in Footnote to add more context to the minimum wage. [The original footnotes can be found here.](https://www.dol.gov/whd/state/stateMinWageHis.htm)

(b) - For the years indicated, the laws in Arizona, Arkansas, California, Colorado, Kentucky, Minnesota, Ohio, Utah, and Wisconsin applied only to women and minors.

[c] - Rates applicable to employers of four or more.

(d) - Rates applicable to employers of six or more. In West Virginia, applicable to employers of six or more in one location.

(e) - Rates applicable to employers of two or more.

(f) - For the years 1988 to 1990, Minnesota had a two tier schedule with the higher rate applicable to employers covered by the FLSA and the lower rate to employers not covered by the FLSA.

(g) - Minnesota sets a lower rate for enterprises with annual receipts of less than $500,000 ($4.90, January 1, 1998-January 1, 2005). The dollar amount prior to September 1, 1997 was $362,500 ($4.00 - January 1, 1991-January 1, 1997); Montana sets a lower rate for businesses with gross annual sales of $110,000 or less ($4.00 - January 1, 1992-January 1, 2005); Ohio sets a lower rate for employers with gross annual sales from $150,000 to $500,000 ($3.35 - January 1, 1991-January 1, 2005) and for employers with gross annual sales under $150,000 ($2.50 - January 1, 1991-January 1, 2005); Oklahoma sets a lower rate for employers of fewer than 10 full-time employees at any one location and for those with annual gross sales of less than $100,000 ($2.00, January 1, 1991-January 1, 2005); and the U.S. Virgin Islands sets a lower rate for businesses with gross annual receipts of less than $150,000 ($4.30, January 1, 1991-January 1, 2005).

(h) - In the District of Columbia, wage orders were replaced by a statutory minimum wage on October 1, 1993. A $5.45 minimum rate remained in effect for the laundry and dry cleaning industry as the result of the grandfather clause.

(i) - In Puerto Rico, separate minimum rates are in effect for almost 350 non-farm occupations by industry Mandatory Decrees. Rates are higher than those in the range listed in effect in a few specific occupations.
(i2) - The rate is 5.08/hour for those employees not covered by the Fair Labor Standards Act.

(j) - In the U.S. Virgin Islands, implementation of an indexed rate, which was to have started January 1, 1991, was delayed.

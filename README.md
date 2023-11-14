# Mixed-Integer-Programming-for-Portfolio-Construction
Code for the Python (with Gurobi solver) implementation of the MIP model presented in the paper: "Portfolio Construction Through Mixed-Integer Programming at Grantham, Mayo, Van Otterloo and Company"

The project is composed of two parts: the Python code and the parameter data, which is editable on the Excel wortksheets. The data used comprises 20 stocks in the Hang Seng index over the period 1st January 2015 - 31st December 2018.

The Excel file called DATA contains all of the computation done on the 20 stocks that can be chosen as part of a portfolio. The calculation of the parameters has been done in the following way: 

GENERAL (Sheet):
* N = number of securities considered
* S = number of sectors these securities comprise, the data was taken Yahoo Finance
* L = weights used by the author in the paper cited above to modify the objective function to the specific needs of a company or an individual, the ones present in the code are for reference only.
* LQ = liquidity associated to each and every security, this is calculated using the difference in ask and bid price in the beginning of November 2023, since all securities are stocks the liquidity is similar for all assets.
* M = Indicator function for the sector in which every company operates

VOLUME (Sheet):
- Contains all the stocks volume indexes, calculated at the beginning of every month using as volume index the average of the last 10 days over the average over the whole period of three years. 

alpha (Sheet):
- Contains all the stock average returns in the last 20 days the period of interest, only for the first day of each month.

WT in time (Sheet):
- The terget portfolio wanted in the paper where the model is described. We used the market portfolio we would have if the Hang Seng comprised only the 20 stocks considered, updated for every month in the period considered.

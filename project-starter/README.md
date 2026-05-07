Mine Waste in the United States
================
by Indigo Sterud

## **Summary**

Roughly 50 million gallons of contaminated waste water flows daily from US 
mining sites into groundwater, rivers, and ponds (*Associated Press*),
contaminating waterways with toxic leachate solutions. I decided to run a 
statistical analysis on National Mine Waste Inventory (NMWI) data because I was 
interested on discovering if specific minerals or states displayed relationships 
with the volume of waste produced at mining sites. The main questions I wanted to 
address were: are there differences in waste production across states? And, do 
certain mineral commodities produce more waste than others? 

## Results
Overall, my results found 
that using log-scaling was important in creating more honest comparisons between 
groups, and there was a significant difference in waste volumes between at least 
one of the 10 states with others, as well as between commodity minerals via ANOVA 
testing. Gold, copper, silver and molybdenum had the most observations between 
all commodities. Copper and gold had no significant differences in waste volume, 
while copper and molybdenum displayed a significant difference in volumes. Only 
19% of commodity-to-commodity mineral comparisons displayed a p-value of <0.05,
therefore there is no evidence to significantly state that mean site waste 
volumes differ between mineral commodities.

## Limitations
It is also crucial to disclose that the data used from the NMWI is a giant 
compilation of publicly available mining data across 10 different US states. 
This dataset does not represent the whole of all states or mineral commodities, 
and is limited further by the lack of publicly released information by private 
mining companies.

## Methods and Discussion
To begin, two .csv files from the NMWI, named Waste_Geology and Waste_Resources 
were first combined to form mining_clean, where the main variables observed 
included state_abbr (abbreviated state name), Calc_Vol (the volume of waste at the 
site in standardized metric units m^3), and Commodity (economically beneficial 
minerals). Most waste volume quantities were reported between 1e05 and 1e07. 
However, some sites in AZ and UT reported abnormally high waste volumes between 
1e09 and 1e10 which create a right skew to the data if not log-transformed. 
Since different states contained different observation counts, a bootstrapped 
state-grouped comparison, replicated 500 times, helped to avoid assumptions of 
normality across states, providing a more accurate and robust comparison. The 
bootstrapping uncovered that Arizona had the highest median waste volume sites, 
followed closely by New Mexico. Concurrently, an ANOVA test comparing the mean 
logarithmic waste volumes outputted a p-value of <2e16 which explains that at 
least one state of the 10 differs extremely significantly from the others since 
p <0.05. This approves the hypothesis that mean mine-waste volume outputs differ 
between states, which can provide further implications into the concept of how 
different states contaminate waterways to different extents.

Commodity minerals reported at mining sites also had a relationship with waste
volumes, depending on the commodity. Tellurium, selenium, rhenium, platinum,
and palladium were often harvested from mines with larger waste volumes, seen 
with higher median amounts. Interestingly though, these 5 commodities had a 
greatly reduced amount of observations within the data compared to silver, 
molybdenum, copper, and gold. Out of *these* 4 minerals, copper was observed the 
most amount of times within the data, and silver the least. All 4 of these 
minerals average around the same mean waste volume and share a similar histogram 
shape, being left-skewed, and peaking at 1.5e07 m^3. Using a T-test for gold and 
copper, there was no significant difference in the average log-transformed 
mine-waste volumes, having a p-value of 0.29. But for copper and molybdenum, 
a p = 1.531e-05 shows a highly significant difference between copper and 
molybdenum average waste volume amounts.

When comparing all 49 commodity minerals through by performing an ANOVA test, a 
Pr(<F) of <2e-16 shows that the difference in means between at least one commodity
and the others is extremely statistically significant, meaning that at least one
commodity has a significant difference in means compared to the rest- although 
they may be found at the same sites. Concurrently, an F-value of 21.93 shows that 
the variation between commodity mineral means is significantly larger than the 
variation within the commodity distributions themselves. This ANOVA test is 
obviously a very broad comparison since 49 minerals are involved, therefore the 
implications of these results should be proceeded with caution. To further 
identify the discrete commodity-to-commodity mean waste comparisons more 
closely, a TukeyHSD test can be facilitated to the anova_model using 
TukeyHSD(anova_model). To sum this test, 229 out of 1225 dual commodity-mineral 
comparisons displayed p-values of <0.05, which can provide insight into how 
calculated waste-volumes at the site the commodity mineral was reported at does 
not differ significantly between commodities.


## Presentation

My presentation can be found [here](presentation/presentation.html).

## Data

United States Geological Survey. (2026). National Mine Waste Inventory 
[Data set]. Geology, Geophysics, and Geochemistry Science Center. 
https://doi.org/10.5066/P148EEUA 

## References

*Associated Press*, Matthew Brown. "U.S. mining sites dump 50 million gallons of 
fouled wastewater daily", PBS News Feb 20, 2019 12:51 PM EDT.


# NSW Data Centre Electricity Demand: Growth Scenarios to FY2034

This is a look at how fast growing data centre electricity demand in New
South Wales, Australia could affect the state's grid over the next decade.
I built it as my individual contribution (Task 1, sections 2.1 to 2.5) to a
group consulting report for BUSA8031 (Business Analytics) at Macquarie
University.

## What's in here

- `Business_Project_Data_Coding.ipynb`, the full analysis: loading and
  cleaning AEMO's price and demand data, working out the current NSW demand
  baseline, modelling low/medium/high growth scenarios for data centre
  demand out to FY2034, and a sensitivity analysis on the key assumptions
- `NSW_Data_Demand_Baseline.pdf`, the final written report this notebook
  supports, with the full methodology, assumptions and sources

## What I did

I started by pulling together the current NSW electricity demand baseline
for FY2023/24, using AEMO's public price and demand data, and looked at how
demand shifts across seasons and through the day. From there I modelled
three scenarios (low, medium and high growth) for how much extra demand data
centres could add by FY2034, based on AEMO's national forecasts scaled down
to NSW's roughly 60% share of national data centre capacity. I sized each
scenario against NSW's total electricity baseline, then ran a sensitivity
analysis to see which assumptions the forecast is most sensitive to.

A lot of NSW's announced data centre pipeline probably won't actually get
built. Oxford Economics Australia reckons about 6 in every 7 MW of
connection requests are "phantom demand" that never materialises, so rather
than adding up announced projects, I started from AEMO's national demand
forecasts and scaled them to NSW's estimated share of national data centre
capacity. From there I worked out facility load assuming the data centres
run continuously, and varied the efficiency and utilisation assumptions by
scenario to reflect the mix of older facilities and new hyperscale builds
each growth path implies. The growth curve ramps up quickly at first and
tapers off over time, rather than growing in a straight line, since that's
closer to how these builds actually tend to play out.

All the detail, assumptions and sources are in
[NSW_Data_Demand_Baseline.pdf](NSW_Data_Demand_Baseline.pdf).

## A quick note on scope

This was a group project, and what's here is only the part I wrote myself:
the demand baseline, the scenario modelling and the sensitivity analysis.
The table of announced NSW data centre projects in the report was compiled
from public announcements rather than calculated, so that one's not part of
the notebook.

## Tools

Built with Python (pandas, numpy, matplotlib). I used Claude along the way
as a coding and analysis assistant.

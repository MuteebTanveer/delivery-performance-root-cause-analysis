# delivery-performance-root-cause-analysis
# Delivery Performance: Root Cause Analysis and Capability Assessment

An e-commerce company wants 95% of orders delivered on time. In January it was close at 91.5%. By June it had dropped to 77.9%. This project finds out why, checks which parts of the business are not ready for the growth, and sets out a plan to close the 17 point gap.

The dataset is a case study (sample orders, warehouse process timings, monthly KPIs and stakeholder interviews). Targets in the data are illustrative.

![On time delivery trend]
<img width="849" height="290" alt="image" src="https://github.com/user-attachments/assets/a8ecb86f-fc87-4406-8aca-49e9a810c9fa" />

## Questions

1. Why did on time delivery fall from 91.5% to 77.9% in six months?
2. Which capabilities are furthest from where they need to be?
3. How well do the organisation's parts fit together, using the McKinsey 7S and Nadler Tushman models?
4. What should be fixed first to get back to 95%?

## Data

| Table | Rows | What it holds |
|---|---|---|
| Monthly_KPIs | 6 | On time %, orders, backlog, cost, complaints, satisfaction and targets, Jan to Jun 2026 |
| Orders | 1,800 | Sampled orders with warehouse, shift, carrier, staff tenure, step times, promise days and late flag |
| Process_Timings | 500 | Minutes for each warehouse step plus system downtime per shift |
| Capability_Assessment | 10 | Current and target maturity scores (1 to 5) with stakeholder priority |
| McKinsey_7S, Nadler_Tushman | 7, 5 | Evidence for each framework element |
| Stakeholder_Interviews | 7 | Notes from warehouse, IT, carrier, HR, finance and operations leads |

## Approach

1. Defined the problem as a gap: 77.9% against a 95% target.
2. Found when it started. The decline sped up from April, when orders passed 9,800 a month.
3. Found where it happens by splitting late orders by carrier, promise days, shift, warehouse and staff tenure.
4. Listed every possible cause in a fishbone diagram, then checked each one against the data.
5. Used a Pareto chart to rank the causes and a five whys chain to reach the root.
6. Scored capabilities and ran the 7S and Nadler Tushman reviews to explain why the causes were not caught.
7. Built an action plan with owners, timing and a success measure for each step.

![Fishbone diagram]
<img width="649" height="356" alt="image" src="https://github.com/user-attachments/assets/04a7c9e8-308f-41c0-b1d1-3a54d9c3ca50" />


## Key findings

Orders grew faster than capacity. Orders went up 39% (8,200 to 11,400 a month) while staffing was still planned from last quarter's average. The day end backlog grew five times, from 120 to 610 orders.

Promises are shorter than the trip. 37% of sampled orders were promised in 2 days, but average transit alone is 2.9 days. 80% of 2 day orders were late, against 33% of 4 day orders.

Carrier C is the slowest. It takes 3.6 days in transit against 2.7 for Carrier A, and 79% of its orders were late against 57%. The gap is the same in all three warehouses, so the problem is the carrier and not the site.

Orders wait too long inside the warehouse. The wait before picking starts averages 24.9 minutes and the queue before dispatch 21.9 minutes, against a 15 minute benchmark. Waiting makes up 56% of total warehouse time and is worst on the evening shift and in Lahore.

![Late rate by carrier and promise days]
<img width="663" height="247" alt="image" src="https://github.com/user-attachments/assets/4b7df0c1-d569-4d8b-99de-b9fd0b6ced96" />


![Pareto of extra late orders]
<img width="615" height="276" alt="image" src="https://github.com/user-attachments/assets/f8b60489-a9be-4909-b860-f990d3553112" />


## Root causes

1. The staffing plan is not linked to the order forecast.
2. Promise dates are set without looking at real carrier transit times.
3. Carrier performance is not measured, so Carrier C keeps a large share of orders.
4. Queues and downtime between warehouse steps are not controlled.
5. No one owns delivery from end to end, and reports are made by hand once a week, so problems are seen late.

## Capability assessment

All ten capabilities are below target. The four with the biggest gaps that stakeholders also rate as high priority are Inventory Visibility, Continuous Improvement, Workforce Planning and Warehouse Operations.

![Capability maturity]
<img width="571" height="279" alt="image" src="https://github.com/user-attachments/assets/c8ff1ca1-09a5-40b1-8307-7dc2d7630b2f" />


## McKinsey 7S and Nadler Tushman

The 7S review rates Structure, Systems, Staff and Shared Values as weak. The company chose growth, but the structure, systems and people that should carry that growth stayed the same. Daily huddles focus on volume instead of on time delivery.

The Nadler Tushman review finds low fit between the work and the formal organisation, the work and the people, and the formal and informal organisation. Every output is below target in June: on time 77.9%, cancellations 5.5%, cost per order PKR 229 and 43 complaints per 1,000 orders.

## Action plan

| Action | Owner | Estimated gain |
|---|---|---|
| Build shift rosters from the order forecast | Warehouse Managers, HR | +8.0 points |
| Set promise dates from real carrier transit times | Commercial Operations | +2.7 points |
| Weekly carrier scorecard and move volume from Carrier C | Carrier Coordinator | +1.8 points |
| Start picking within 15 minutes and cut evening downtime | Warehouse Managers, IT | +2.5 points |
| One end to end owner with a daily on time review | Operations Director | +2.1 points |

The gains are planning estimates based on the size of each gap, not measured results.

![Path to 95%]
<img width="591" height="264" alt="image" src="https://github.com/user-attachments/assets/d088f8ff-e490-4042-a0b3-c77e66fdf41c" />


## Files

| Path | What it is |
|---|---|
| `Delivery_RCA_7S_Nadler_Tushman.pdf` | Full 12 page report |
| `Delivery_Performance.pbix` | Power BI report with six pages: Overview, Root Cause Analysis, Capability Assessment, McKinsey 7S, Nadler Tushman, Action Plan |
| `images/` | Charts used in the report and this README |

## Tools

Power BI, Power Query, Python (pandas, matplotlib), ReportLab

## Limitations

The order sample flags 63.5% of orders as late, much higher than the 8.5% to 22.1% in the monthly KPIs. The sample seems to include more problem orders than normal, so it is used only to compare groups, not to measure the overall rate.

Capability scores are early stakeholder ratings and should be confirmed with a wider survey.

Some late orders have more than one cause, so the Pareto counts and the plan estimates overlap.

## Author

Hafiz Muteeb Ahmad
[Portfolio](https://muteebtanveerportfolio.vercel.app/) · [LinkedIn](https://www.linkedin.com/in/hafiz-muteeb-ahmad-bb6884389) · [GitHub](https://github.com/MuteebTanveer)

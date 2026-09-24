**Business Understanding: Demand Forecasting for FreshMart**

**1\. Business Problem Statement**

_Head of Supply Chain, FreshMart (a regional grocery chain with 60 stores):_  
"Our shelves are either overstocked or empty. We order fresh products based on last year's sales and store managers' intuition. This costs us money through waste and lost customers. I need reliable daily demand forecasts for each product in each store."

**2\. Definition of the Core Business Issue**

- Inaccurate demand estimates cause perishables to spoil and popular items to run out.
- Waste lowers our margins, and empty shelves send customers to competitors.
- **Why now:** Rising food and energy costs, thinner margins and new food-waste sustainability targets mean manual ordering is no longer good enough.

**3\. Goals and Success Criteria**

- Reduce forecast error (WAPE) by at least 20% compared with the current naïve method.
- Cut perishable waste by 15% within 12 months.
- Keep on-shelf availability at or above 97%.
- Store managers use the forecasts for at least 80% of orders.

**4\. Project Risks and Constraints**

- **Data limitations:** There are gaps in sales history. Stock-outs hide true demand, and new products have little history.
- **Privacy:** Loyalty-card data is personal data under the GDPR, so only aggregated, anonymised data may be used.
- **Technical:** There are thousands of product–store series, legacy POS/ERP systems, and forecasts must be retrained automatically every day.
- **Organisational:** Managers may distrust "black-box" forecasts. The company also has limited in-house data science skills and needs budget approval.

**5\. Translation into Data Science Terms**

- **Problem type:** Supervised time-series regression that predicts daily unit sales per product and store, 1–14 days ahead.
- **Inputs:** Historical POS sales, prices and promotions, holidays and calendar effects, weather forecasts, store attributes and stock levels.
- **Outputs:** Point forecasts with prediction intervals. These feed automated order recommendations and alerts for waste or stock-out risk.
- **Evaluation:** WAPE and bias on a hold-out period, compared against a seasonal naïve benchmark.

**6\. References**

- Hyndman, R. J., & Athanasopoulos, G. (2021). _Forecasting: Principles and practice_ (3rd ed.). OTexts. <https://otexts.com/fpp3/>
- Makridakis, S., Spiliotis, E., & Assimakopoulos, V. (2022). M5 accuracy competition: Results, findings, and conclusions. _International Journal of Forecasting, 38_(4), 1346–1364. <https://doi.org/10.1016/j.ijforecast.2021.11.013>
- McKinsey & Company. (2021). _Succeeding in the AI supply-chain revolution_. <https://www.mckinsey.com/industries/metals-and-mining/our-insights/succeeding-in-the-ai-supply-chain-revolution>
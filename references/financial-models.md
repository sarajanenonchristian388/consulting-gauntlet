# Financial Models Reference

See `agents/financial-analyst.md` for full model instructions.

## Model Selection Guide

| Engagement Type | Primary Model | Supporting |
|---|---|---|
| Company Valuation | DCF + Trading Comps | Precedent transactions |
| Market Entry / Business Case | 5-year P&L + Break-even | Unit economics |
| SaaS / Subscription business | Unit economics (LTV/CAC) + ARR model | DCF |
| M&A | DCF + Synergy model + Accretion/Dilution | Trading comps, precedents |
| Infrastructure / CapEx | NPV / IRR analysis | Payback period |
| Startup / Early Stage | Unit economics + Funding runway | Revenue scenarios |
| Operational Turnaround | P&L bridge + Working capital model | Break-even |

## Key Formulas

**WACC**
= (E/V × Ke) + (D/V × Kd × (1-T))
- Ke = Risk-free rate + Beta × Equity Risk Premium (CAPM)
- Kd = Cost of debt (pre-tax)
- T = Marginal tax rate
- E/V = Equity weight; D/V = Debt weight

**DCF Terminal Value**
- Gordon Growth: TV = FCF_n × (1+g) / (WACC - g)
- Exit Multiple: TV = EBITDA_n × EV/EBITDA multiple (from comps)

**LTV (SaaS)**
= (ARPU × Gross Margin %) / Churn Rate
or = Average Contract Value × Gross Margin % × 1/Churn

**LTV:CAC** (healthy ratio: >3x; payback <18 months)

**Unit Economics Break-Even**
Break-even units = Fixed Costs / (Selling Price - Variable Cost per Unit)

**Real vs. Nominal**
Real Value = Nominal Value / (1 + inflation rate)^n
Real Growth Rate ≈ Nominal Growth Rate - Inflation Rate

## Macro Data Sources (always cite with year)
- CPI / Inflation: BLS.gov, Federal Reserve FRED
- GDP Growth: IMF WEO, World Bank
- Risk-Free Rate: US Treasury (treasury.gov)
- Equity Risk Premium: Damodaran Online (NYU Stern) — updated annually
- Beta: Bloomberg, CapIQ, or Damodaran industry betas
- Industry revenue benchmarks: IBISWorld, Statista (note methodology)

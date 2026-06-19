# FINTECH-LOAN-ANALYSIS

## FINTECH RISK ENGINE – Credit Risk & Loan Default Portfolio Engine## Table of Contents

* Project Overview
* Business Introduction
* Business Problem
* Business Objective
* Process Taken
* Database Engine Features
* Tools
* Key Insights
* Recommendations
* Conclusion

------------------------------
## Project Overview
This credit risk engine and portfolio analytics script transforms raw transactional lending data into structured PostgreSQL database profiles. Designed for financial analytics squads and risk engineering teams, it programmatically exposes default vulnerabilities, monitors subprime market concentrations, isolates high-risk consumer behaviors, and restores log-transformed income metrics into real-world currencies for database reporting.
------------------------------
## Business Introduction
The fintech organization operates a multi-tiered consumer lending platform across multiple credit policies and loan products. Managing capital allocation effectively requires constant programmatic surveillance of database metrics, borrower repayment mechanics, and evolving macroeconomic distress indicators stored within the core warehouse tables.
Management requires a centralized SQL risk engine to:

* Monitor active debt exposure across product purposes and borrower segments using raw queries.
* Track absolute default rates and identify structural risk pools via database triggers and expressions.
* Uncover compounding behavioral degradation flags like revolving over-utilization and credit hunting.
* Stress-test underwriting filters using active SQL policy simulation queries.

------------------------------
## Business Problem
The financial risk management division operated with several critical blind spots inside their raw datasets:

* Log-Obscured Income Profiles: Real-world cash flows and accurate asset allocations were obscured by log-transformed borrower income columns.
* Under-Hedged Risk Co-dependencies: Co-dependent default hazards—such as combining high interest rates with extreme borrower debt loads ("The Toxic Mix")—were not systematically quantified in queries.
* Delayed Behavioral Warning Flags: Revolving credit account over-utilization and frantic near-term inquiry behaviors were not isolated into predictable risk profiles at the database level.
* Static Credit Cutoff Invisibility: Underwriting units could not calculate the exact trade-off of volume loss versus default reduction when shifting target credit boundaries via relational logic.

------------------------------
## Business Objective

* Engineer a Structured PostgreSQL Data Warehouse Layer: Deploy clean relational architecture to process and audit credit parameters.
* Expose Subprime Vulnerabilities: Track exact loan volumes, debt-to-income (DTI) metrics, and default margins across subprime tiers using optimized query logic.
* Restore Real Currency Baselines: Mathematically reverse log transformations using mathematical functions to reconstruct absolute borrower incomes and portfolio cash flows.
* Develop Policy Simulation Scripts: Create clean, scalable SQL blocks that allow analysts to test minimum FICO score limits and measure portfolio risk impact.

------------------------------
## Process Taken## 1. Data Ingestion & Schema Engineering
Structured a core loan_portfolio PostgreSQL architecture mapping metrics including FICO, DTI, revolving balance, inquiry logs, interest rates, monthly installments, and historical default flags (not_fully_paid).
## 2. Advanced Data Quality Gates

* Deployed partition-based window functions (ROW_NUMBER()) across the entire column array to screen for data duplication, validating 0 duplicate records in the operational set.
* Leveraged PERCENT_RANK() metrics to isolate, audit, and analyze the top 10% highest leveraged borrower profiles to protect database baselines from data distortion.

## 3. Feature Engineering & Mathematical Inversions

* Executed exponential scaling (EXP(log_annual_inc)) inside the database core to return accurate currency figures.
* Engineered complex categorical CASE flags to segment multi-variable financial profiles ("The Toxic Mix") and consumer behaviors ("Credit Hunting & Over-Utilization").

## 4. Policy Stress Testing
Designed clean aggregation models using mathematical filters to simulate a hypothetical credit policy pivot, calculating the precise business volume drop-off versus the reduction in loan defaults by stripping away subprime tiers (FICO < 680).
------------------------------
## Database Engine Features## Core Schema Definition (loan_portfolio)
Provides a highly optimized PostgreSQL table structure containing exact numerical datatypes (NUMERIC(6,4), INT) to preserve decimal precision for financial rates and loan calculations.
## Key Analytical Code Blocks

| Script Focus | Database Performance Function |
|---|---|
| Windowed Deduplication | Employs ROW_NUMBER() OVER(PARTITION BY...) to verify absolute relational record unique constraints. |
| Outlier Percentile Ranking | Leverages PERCENT_RANK() OVER(ORDER BY dti DESC) to flag borrowers over-leveraged by debt. |
| FICO Risk Tracking | Aggregates portfolio loans and groups structural default trends directly by credit score. |
| Multi-Variable Profile Flags | Generates dynamic text categories by parsing compound conditional CASE filters. |
| Exponential Currency Inversion | Converts analytical fields into clean currency reporting lines using EXP(). |

------------------------------
## Tools

* PostgreSQL: Primary data extraction, feature engineering, and data pipeline calculation engine.
* Window Functions: Deployed ROW_NUMBER() for data auditing and PERCENT_RANK() for extreme leverage tracking.
* Mathematical Inversions: Utilized EXP() functions to restore financial transparency to logged data arrays.

------------------------------
## Key Insights## Product Allocation Volatility

* Small Business Risks: Small business lending represents the single highest risk sector. It exhibits a severe 27.79% default rate, despite these borrowers carrying high average incomes ($85,793.91). High personal income does not insulate business investments from structural default pressures.
* Debt Consolidation Dominance: Debt consolidation represents the massive bulk of portfolio concentration, holding 3,957 loans and 1,050 subprime borrowers. This concentration generates a high structural default rate of 15.24%, making it the largest absolute dollar-at-risk exposure.
* Major Purchase Resiliency: Major purchase loans function as the safest consumer credit segment, holding a low default rate of 11.21%.

## Behavioral & Pricing Risk Profiles

* The Desperation Trigger: High revolving credit card utilization ($\geq$75.00%) matched with near-term credit hunting ($\geq$3 inquiries) serves as an immediate leading indicator of insolvency, leading the database records with a 28.34% default rate.
* The Stability Baseline: Control groups maintaining low card utilization and 0 recent inquiries remain highly durable, yielding a minimal 9.06% default rate.
* The Leverage Trap: Combining high interest rates ($\geq$12%) with high customer debt burdens ($\geq$20.00 DTI) creates a compounding loss zone that outpaces standard interest-margin profitability.

------------------------------
## Recommendations## Capital Allocation Shifting
Divert a portion of available lending capital away from volatile small_business segments and reallocate it toward credit_card refinancing. This protects portfolio yield while cutting default exposure by more than half (11.57% vs 27.79%).
## Underwriting Floor Mandates
Impose a strict FICO floor of 660 on all debt_consolidation applications. This asset class contains the platform's highest subprime profile volume (1,050 accounts); establishing this boundary prevents systemic defaults before loan origination occurs.
## Dynamic Behavioral Limits
Deploy automated risk mitigators within the account management ecosystem. If an active borrower surpasses 3 hard credit inquiries within a rolling 6-month window while maintaining over 75% card utilization, trigger an automatic, temporary credit limit restriction.
## Margin Hedging
Eliminate or aggressively reprice new originations that match "The Toxic Mix" configuration (DTI $\geq$ 20.00 and Interest $\geq$ 12%). This ensures the portfolio is adequately capitalized against compounding risk factors.
------------------------------
## Conclusion
The Fintech Credit Risk Analytics Engine successfully exposes underlying vulnerabilities by parsing customer behaviors and stripping away complex data transformations through raw SQL execution. Running these optimized database queries provides the Chief Risk Officer (CRO) and risk engineering teams with the real-time visibility needed to protect capital reserves, optimize underwriting regulations, and maximize risk-adjusted yields across the whole database architecture.
------------------------------
## Database Footer

* Currency Base: All restored figures are processed in USD ($)
* Underwriting Standards: Credit classifications align with standard FICO and credit bureau risk tier parameters.
* Data Refresh Cadence: Automated SQL pipeline execution.

------------------------------
## How to Use This Analytics Engine

   1. Execute Ingestion Script: Run the initial table and data definition language blocks to prepare the database environment.
   2. Validate Data Integrity: Execute the windowed duplication gate to verify structural data hygiene.
   3. Run Inversion Core: Deploy the EXP() macro query to instantly recover absolute borrower income tables.
   4. Stress Test Underwriting Policies: Utilize the simplified policy simulation code block to forecast variations in risk thresholds before deploying new lending parameters.



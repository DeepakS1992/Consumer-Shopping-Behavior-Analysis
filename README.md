# Consumer Shopping Behavior Analysis

## Project Overview

This project analyzes a **Consumer Shopping Behavior Survey** containing
**500 responses** to understand how consumers shop, what influences
their purchase decisions, how they spend on non-essential items, which
payment methods they prefer, and how they perceive online shopping.

The project follows an end-to-end Power BI workflow: **data cleaning and
transformation in Power Query, exploratory data analysis (EDA), DAX
measure creation, and interactive dashboard development**.

> **Analysis note:** This is survey-based descriptive and exploratory
> analysis. The findings show patterns and associations within the
> sample and should not be interpreted as proof of causation.

------------------------------------------------------------------------

## Business Problem

Retailers operate across both online and physical channels, but consumer
preferences and purchase behavior can differ across demographic and
behavioral groups. The project was designed to answer questions such as:

-   What shopping channels do consumers prefer?
-   How frequently do consumers shop online?
-   Which factors are most important in purchase decisions?
-   Which payment methods are preferred?
-   How much do consumers report spending monthly on non-essential
    purchases?
-   Which categories receive the most spending?
-   How satisfied are consumers with online shopping, and how much do
    they trust online reviews?

------------------------------------------------------------------------

## Dataset

  -----------------------------------------------------------------------------------------------------------------------------------------------------
  Item                                Details
  ----------------------------------- -----------------------------------------------------------------------------------------------------------------
  Dataset Name                        Consumer Shopping Behavior & Buying Survey Dataset

  Dataset Source                      [Kaggle -- Consumer Shopping Behavior & Buying Survey
                                      Dataset](https://www.kaggle.com/datasets/harpartapsingh13/consumer-shopping-behavior-and-buying-survey-dataset)

  Dataset Author                      Harpartap Singh

  Responses                           500

  Original Columns                    30

  Data Type                           Consumer survey data

  Analysis Type                       Descriptive & Exploratory Analysis

  Main Tool                           Power BI

  Supporting Tools                    Power Query, DAX
  -----------------------------------------------------------------------------------------------------------------------------------------------------

The dataset covers five broad areas:

-   **Demographics:** age, gender, occupation, country/region, income
    range
-   **Shopping behavior:** shopping channel, online-shopping frequency,
    platform, device, spending category
-   **Purchase drivers:** reviews, social ads, price comparison,
    discounts, buying likelihood after ads, impulse purchasing
-   **Spending & payment:** non-essential spending, payment method, BNPL
    usage, shopping lists, returns
-   **Customer experience:** online satisfaction, review trust, purchase
    regret, and reasons for channel preference

------------------------------------------------------------------------

## Data Cleaning & Transformation

Data preparation was completed primarily in **Power Query**.

Key steps included:

-   Preserved the raw query and created a separate cleaned query.
-   Audited columns using quality, distribution, and profile tools.
-   Converted the timestamp field to a valid Date/Time type.
-   Cleaned the **Age** field by converting valid ages to whole numbers
    and replacing invalid text entries with null.
-   Created an **Age Group** field for demographic analysis.
-   Applied Trim/Clean transformations to text fields and standardized
    category labels.
-   Represented missing categorical responses as **Unknown** where
    appropriate.
-   Retained missing numerical survey scores as **null**, rather than
    incorrectly converting them to zero.
-   Validated score columns and converted them to appropriate numeric
    data types.
-   Created helper/sort fields for ordinal categories, income bands,
    spending bands, and age groups.
-   Checked duplicate rows and `Response_ID` uniqueness; no complete
    duplicate rows or duplicate IDs were identified.

------------------------------------------------------------------------

## Exploratory Data Analysis

EDA was organized into dedicated Power BI pages:

1.  **Consumer Profile**
2.  **Shopping Behaviour**
3.  **Purchase Drivers**
4.  **Spending & Payment**
5.  **Customer Experience**

Selected relationship analysis included:

-   **Likelihood to Buy After Ad vs. Social Ad Influence:** higher
    reported social-ad influence was associated with higher average
    buying likelihood after an advertisement.
-   **Price Comparison vs. Discount Importance:** price-comparison
    scores remained high across discount-importance levels, without a
    clear increasing pattern.
-   **Online Satisfaction vs. Review Trust:** satisfaction remained
    relatively stable across review-trust scores.
-   **Purchase Regret vs. Return Frequency:** regret scores were similar
    across return-frequency groups.

These comparisons helped distinguish meaningful patterns from
relationships that appeared relatively weak or flat.

------------------------------------------------------------------------

## Power BI Dashboard

The final dashboard summarizes the most useful findings from the EDA and
includes interactive demographic filters.

### KPI Cards

-   **Total Respondents:** 500
-   **Average Online Shopping Satisfaction:** 7.13 / 10
-   **Average Review Trust:** 6.16 / 10
-   **Average Purchase Regret:** 2.19 / 4

### Main Visuals

-   Shopping Preference
-   Average Purchase Driver Scores
-   Preferred Payment Method
-   Monthly Non-Essential Spending
-   Online Shopping Frequency
-   Top Spending Category

### Interactive Slicers

-   Gender
-   Age Group
-   Income Range
-   Country

> Add your exported dashboard image here after uploading it to the
> repository:
>
> `![Consumer Shopping Behavior Dashboard](images/dashboard.png)`

------------------------------------------------------------------------

## Key Insights

### 1. Consumers value both online and physical shopping

**248 respondents (49.6%)** prefer an equal mix of online and in-store
shopping. **165 (33.0%)** prefer online only, while **71 (14.2%)**
prefer in-store only.

This suggests that the surveyed consumers often value both digital
convenience and physical-store experiences.

### 2. Price-related factors are prominent purchase drivers

The strongest average purchase-driver scores were:

  Purchase Driver          Average Score
  ---------------------- ---------------
  Price Comparison              4.14 / 5
  Discount Importance           3.81 / 5
  Social Ads Influence          3.09 / 5
  Review Influence              3.04 / 5
  Likelihood After Ad           3.02 / 5
  Impulse Purchase              2.60 / 5

Price comparison and discount importance stand out relative to the other
measured drivers.

### 3. Occasional online shopping is the largest frequency group

**240 respondents (48.0%)** shop online occasionally. The remaining
reported groups include **132 often**, **58 rarely**, and **51 always**.

### 4. Digital wallets are the leading preferred payment method

Among displayed valid responses:

-   Digital Wallet --- **183**
-   Debit Card --- **129**
-   Credit Card --- **109**
-   Cash --- **64**

### 5. Non-essential spending is concentrated in lower bands

The largest spending groups are:

-   Under \$50 --- **179 respondents**
-   \$50--150 --- **144**
-   \$150--300 --- **95**
-   \$300--500 --- **42**
-   \$500+ --- **20**

### 6. Clothing is the most frequently reported top spending category

**179 respondents** selected clothing as their top spending category,
followed by **groceries (92)** and **electronics (76)**.

### 7. Satisfaction is stronger than review trust

Average online-shopping satisfaction is **7.13/10**, while average trust
in online reviews is **6.16/10**. The sample therefore reports
relatively positive online-shopping satisfaction alongside more moderate
trust in reviews.

------------------------------------------------------------------------

## Business Recommendations

Based on the survey patterns, businesses serving a similar audience
could consider:

-   Supporting an **omnichannel experience** with consistent product
    information, pricing, inventory visibility, and flexible
    fulfillment.
-   Emphasizing **competitive pricing and transparent value
    communication**, while testing targeted discounts.
-   Using loyalty benefits, personalized offers, and convenient checkout
    experiences to engage **occasional online shoppers**.
-   Making **digital-wallet checkout** simple and reliable while
    retaining alternative payment options.
-   Designing offers and bundles for the lower-to-mid spending bands
    while separately segmenting higher-spending customers.
-   Giving clothing appropriate merchandising attention for similar
    audiences, while validating category decisions using actual sales
    data.
-   Strengthening review credibility through verified-purchase
    indicators and transparent review practices.

These recommendations are **business hypotheses based on survey data**
and should be validated using transactional, profitability, campaign,
and experimental data before implementation.

------------------------------------------------------------------------

## Tools & Technologies

  ---------------------------------------------------------------------
  Tool / Skill                       Application
  ---------------------------------- ----------------------------------
  Power BI                           Dashboard development and
                                     visualization

  Power Query                        Data cleaning and transformation

  DAX                                KPI and analytical measure
                                     creation

  Microsoft Excel                    Source dataset

  Data Cleaning                      Missing values, invalid values,
                                     standardization

  EDA                                Distribution and relationship
                                     analysis

  Data Visualization                 Business-focused charts and
                                     dashboard design

  Business Analysis                  Converting analytical findings
                                     into decision-oriented insights
  ---------------------------------------------------------------------

------------------------------------------------------------------------

## Example DAX Measures

``` dax
Total Respondents =
DISTINCTCOUNT(Consumer_Survey_Cleaned[Response_ID])
```

``` dax
Avg Online Satisfaction =
AVERAGE(Consumer_Survey_Cleaned[Online_Shopping_Satisfaction_Score])
```

``` dax
Avg Review Trust =
AVERAGE(Consumer_Survey_Cleaned[Trust_In_Online_Reviews_Score])
```

Display measures were also created to present KPI values in
business-friendly formats such as `7.13 / 10`.

------------------------------------------------------------------------

## Limitations

-   The project uses a survey sample of 500 respondents and may not
    represent the wider consumer population.
-   Responses are self-reported and may contain recall or response bias.
-   Observed relationships are **associations, not causal effects**.
-   Non-essential spending is provided as ranges rather than exact
    amounts.
-   Some survey fields contain missing responses.
-   Recommendations should be validated using real transactional and
    business-performance data before implementation.

------------------------------------------------------------------------

## Conclusion

This project demonstrates an end-to-end **Power BI data analytics
workflow**, from raw survey data through data cleaning, transformation,
EDA, DAX, and interactive dashboard development.

The analysis indicates that the surveyed consumers frequently combine
online and in-store shopping, pay considerable attention to price
comparison and discounts, commonly shop online on an occasional basis,
and most often select digital wallets as their preferred payment method.
The project also demonstrates the importance of reporting weak or
inconclusive relationships rather than forcing every analysis to produce
a strong finding.

------------------------------------------------------------------------

## Repository Structure

``` text
Consumer-Shopping-Behavior-Analysis/
│
├── README.md
├── Consumer_Shopping_Behavior_Dashboard.pbix
├── data/
│   └── consumer_shopping_behavior.xlsx
├── images/
│   └── dashboard.png
└── report/
    └── Consumer_Shopping_Behavior_Analysis.pdf
```

------------------------------------------------------------------------

**Portfolio Project --- Consumer Shopping Behavior Analysis \| Power
BI**

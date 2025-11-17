# <h1 align="center"><b>Market Basket Analysis for Online Retail</b></h1>


## Project Overview

This project focuses on a Market Basket Analysis using the "Online Retail II" dataset. This dataset contains transaction data from a UK-based online retailer specializing in unique, all-occasion giftware. The primary goal of this analysis is to uncover relationships between different products sold by the retailer. By identifying which items are frequently purchased together, we can provide actionable insights for business strategies such as product placement, cross-selling campaigns, and personalized recommendations.


## Business Question

1. What items are most frequently bought together by our customers?
2. How do buying patterns change across different seasons?
3. Which products should be bundled or cross-promoted to maximize sales revenue?
4. How can we increase the number of items a customer buys in a single transaction?
   

## Dataset

The dataset used is the "Online Retail II" from the UCI Machine Learning Repository. It contains transaction data from a UK-based online retailer between 01/12/2009 and 09/12/2011.

**Variable Informations:**

- `InvoiceNo`: Invoice number. Nominal. A 6-digit integral number uniquely assigned to each transaction. If this code starts with the letter 'c', it indicates a cancellation.
- `StockCode`: Product (item) code. Nominal. A 5-digit integral number uniquely assigned to each distinct product.
- `Description`: Product (item) name. Nominal.
- `Quantity`: The quantities of each product (item) per transaction. Numeric.
- `InvoiceDate`: Invoice date and time. Numeric. The day and time when a transaction was generated.
- `UnitPrice`: Unit price. Numeric. Product price per unit in Pound Sterling (£).
- `CustomerID`: Customer number. Nominal. A 5-digit integral number uniquely assigned to each customer.
- `Country`: Country name. Nominal. The name of the country where a customer resides.

**Link Dataset:**

https://archive.ics.uci.edu/dataset/502/online+retail+ii


## Exploratory Data Analysis (EDA)

### 1. Total Sales by Month (2009-2011)

Sales exhibit a predictable, strong seasonal cycle, peaking massively in November (Holiday preparation, $\text{£}260,713.96$)—the critical sales period. Secondary peaks consistently align with the beginning of each season (Winter, Spring, Summer kickoff). The lowest sales period is confirmed as February 2010 ($\text{£}94,705.60$), marking the slowest post-holiday lull.

### 2. Total Quantity of Items Sold by Month (2009-2011)

The quantity of items sold follows the seasonal cycle, peaking with sheer volume in November 2010 (732,013 units), confirming the holiday season's focus on high unit purchases. The definitive volume slump occurs in July 2010 (358,783 units). A strong secondary peak in March (530,651 units) indicates customers stock up heavily for the Spring season. Crucially, June's revenue increase was not volume-driven; lower quantity sold than in May confirms the increase was due to a shift in the product mix toward fewer, higher-priced items.

### 3. Total Unique Items Sold by Month (2009-2011)

The highest product variety is required during the holiday shopping season (Dec 2009 and Nov 2010, $\sim$3,000+ unique items), confirming customer demand for a broad assortment of gifts. A strong secondary variety peak in March (2,889 unique items) suggests the start of Spring requires a diverse selection of new seasonal goods alongside high volume. Variety is lowest during the winter and summer lulls (February and July, $\sim$2,600 unique items). Notably, June 2010 had a moderate variety (2,727 unique items), supporting the finding that high June sales revenue was driven by customers selecting fewer units from a diverse, high-value assortment.

## Strategic Market Basket Analysis (MBA) Segmentation

Considering the results of the Exploratory Data Analysis (EDA), the Market Basket Analysis (MBA) will be run separately on four strategic time segments to extract actionable and non-overlapping insights into customer purchasing behavior.

1. Ultimate Peak MBA (Volume & Variety Driver)
    - Focus: November 2010.
    - EDA Rationale: This month registered the highest Sales, Highest Quantity, and High Variety.
    - Strategic Goal: Identify high-volume gifting and holiday bundles to maximize units sold during the critical holiday build-up.

2. High-Value Discrepancy MBA (Revenue Driver)
    - Focus: June 2010.
    - EDA Rationale: This period showed High Sales, but Low Quantity with Moderate Variety (compared to May).
    - Strategic Goal: Identify high-margin, high-value bundles to inform upselling strategies and premium product placement.

3. Seasonal Transition MBA (New Product Bundling)
    - Focus: March 2010 (Spring Kickoff).
    - EDA Rationale: This month demonstrated significant peaks in Sales, Quantity, and Variety, marking the start of a new buying pattern.
    - Strategic Goal: Discover rules involving new seasonal products for timely cross-selling at the start of the season.

4. Trough Season MBA (Core Business Staples)
    - Focus: February 2010 (Lowest Sales) and July 2010 (Lowest Quantity).
    - EDA Rationale: These months represent the lowest overall performance, indicating a reliance on core, evergreen products.
    - Strategic Goal: Identify highly frequent, basic item associations to guide minimum inventory levels and stable product placement during slow periods.

## Recommendation

**1. The Ultimate Peak MBA (Volume and Variety Driver)**

The analysis confirms that the November sales peak is driven by high-volume gifting and project-based multi-buying. The core strategy must focus on formalizing these bundles to maximize the Units Per Transaction (UPT).

a. Formalize the Hand Warmer Multi-Buy as a Gifting Strategy
  - Implement "Mix & Match" Promotions: Do not sell Hand Warmers as single units. Offer a structured promotion (e.g., "Buy 3, Get the 4th Free" or "4 Hand Warmers for a Set Price") to encourage customers to complete the multi-design purchase necessary for gifting.
  - Optimize Placement: Create dedicated, high-visibility displays labeled "Stocking Stuffers" or "Secret Santa Gifts" where all Hand Warmer designs are grouped together, ensuring immediate visual access to the full variety.

b. Bundle Seasonal Decoration Projects
- Create Project Bundles: Formally bundle the associated decoration items. Offer the "Vintage Paper Chain Duo" at a slight discount compared to buying the two kits separately.
- Cross-Merchandise with Utility: Place the Paper Chain Kits next to complementary craft items (e.g., scissors, tape, or other small novelty Christmas decorations) to inspire a larger project-based purchase.

**Goal: Convert the high-volume demand into guaranteed set sales, thereby maximizing revenue during the most critical period.**

---

**2. The High-Value Discrepancy MBA (Revenue Driver)**

The June analysis shows that revenue is driven by a strategy of selling fewer units at a higher average value, achieved by selling complementary sets. The core recommendation is to formally mandate these multi-buys.

a. Mandate Decorative Set Completion (High ATV Focus)
- Formalize Gifting/Collection Bundles: Create a mandatory set purchase for the high-Lift items. Market and price the Trinket Boxes (Sweetheart and Strawberry) as a "Collectible Pair" or "The Duo Gift Set."
- Size Bundling for Decor: Sell the Wicker Hearts (Large and Small) as a single product unit: "Wicker Heart Display Set." This ensures the higher-priced large item automatically drives the sale of the small complementary item, maximizing revenue per set.

b. Maximize Utility Multi-Buys (Volume/Variety Focus)
- Implement "Mix & Match" for Bags: Capitalize on the variety purchasing (Lunch Bags and Jumbo Bags) by running a sustained promotion like "Buy 2 Utility Bags, Get 15% Off," applicable across different patterns (e.g., Pink Retrospot, Red Spotty, Strawberry).
- Cross-Merchandise Strategically: Place the different patterns of Lunch Bags and Jumbo Bags side-by-side both online and in-store. Use signage that emphasizes organization and variety (e.g., "Different Designs for Different Uses").

**Goal: Convert every single-item purchase into a high-value, guaranteed set purchase to sustain the high revenue figures despite lower overall unit volume.**

---

**3. Seasonal Transition MBA (New Product Bundling)**

The March analysis reveals two major opportunities: aggressively capitalizing on new seasonal stock and reinforcing the multi-buy trend for spring utility items.

a. Capitalize on Seasonal Bundling (Easter Baskets)
- Mandatory Seasonal Sets: Given the extreme Lift and high confidence across all color combinations of the Felt Easter Egg Baskets, immediately launch them as a formal "Seasonal Trio" or "Easter Collection Set" (Pink, Blue, Cream). This should be the primary selling unit, rather than individual baskets.
- Early Launch Focus: Ensure maximum inventory and front-of-store visibility for these baskets, as March is the critical kickoff window where demand for the full set peaks.

b. Reinforce Utility and Hobby Multi-Buys
- Formalize Decor Sets: Group the associated decorative items. Specifically, market the LOVE and HOME Building Blocks as a "Complete Word Set" and ensure the Sweetheart/Strawberry Trinket Boxes are placed together to encourage the collectible pair purchase.
- Cross-Promote Variety (Baking & Storage): Implement a "Spring Variety Discount" on essential multi-buy categories:
Baking: Offer a discount when customers buy two different styles of Cake Cases (e.g., Pink Paisley + Retro Spot).
- Storage: Ensure all associated patterns of Jumbo Bags are displayed together to encourage the simultaneous purchase of multiple designs for organization.

**Goal: Maximize transaction value at the start of the season by formalizing all high-confidence associations into required, attractive bundles for both seasonal novelty and home utility.**

---

**4. a. Trough Season MBA (Core Business Staples) - February 2010**

The February analysis confirms reliance on stable multi-buy patterns and early seasonal launches during the lowest sales month. The focus is maximizing the value of every limited transaction.

a. Execute Aggressive Early Seasonal Bundling
- Launch Easter Baskets Early: Immediately leverage the extreme Lift (17.44) of the Felt Easter Egg Baskets. Place them highly visibly and promote them as a "Pre-Season Duo" (Pink + Blue) to capture guaranteed set sales before the March rush.
- Inventory Security: Treat the associated Easter Baskets as mandatory core stock in February due to their unparalleled co-purchase rate.

b. Formalize Utility & Organization Sets
- Mandate Multi-Buy for Storage: Formalize bundles for Toy Tidy Bags (Spaceboy + Pink Retrospot) and Lunch Bags (Pink Retrospot, Spaceboy, Suki) with permanent "Buy 2 for X Price" deals. This ensures the multi-buy behavior converts into maximum Average Transaction Value (ATV).
- Cross-Merchandise Utility: Group all associated Jumbo Bag patterns together in the storage aisle to facilitate the purchase of multiples for different organizational needs.

c. Maintain Stable Demand for Hobby & Decor
- Promote Baking Variety: Highlight the Cake Case variety (Pink Paisley, Retro Spot, Teatime) with signage encouraging customers to "Stock Up on Variety" for year-round low-cost entertaining.
- Display Complete Decor Sets: Always display the LOVE and HOME Building Blocks and the associated Heart T-Light Holders (Red and White) as complete visual sets to drive the co-purchase of these reliable decorative items during the sales slump.

**Goal: Maximize the value of limited traffic by converting resilient multi-buy behavior into guaranteed set purchases, while securing the advantage of an early seasonal launch.**

---

**4. b. Trough Season MBA (Core Business Staples) - July 2010**

The July analysis confirms that maximizing the value of the limited transactions (lowest quantity) relies on highly specific utility and variety bundling. The focus is converting every customer into a multi-item buyer.

a. Formalize "System" Bundles for Utility (Highest Lift)
- Mandate Lunch Box Pairs: Actively market the Dolly Girl and Spaceboy Lunch Boxes as a single unit: "His and Hers/Multi-Child Lunch Set." This leverages the extreme, high-Lift association driven by utility needs for multiple people.
- Encourage Design Variety: Use signage and online promotions to drive the purchase of multiple Lunch Bags and Jumbo Bags. Implement a tiered discount like: "Buy 2 Bags for 10% Off, Buy 4 for 20% Off" to facilitate the buying of an entire "System of Bags" (e.g., one for school, one for storage, etc.).

b. Maximize Decorative Set Completion
- Formalize Frame & Trinket Sets: Ensure all associated Picture Frames (White Finish/Antique White) are displayed together as a "Gallery Wall Set" with clear pricing. Maintain the placement of the Trinket Boxes (Sweetheart/Strawberry) as a high-value, collectible gift pair.
- Focus Placement: Group all these complementary items in a designated "Home Organization & Decor" section to facilitate the purchase of complete decorative projects in one trip.

c. Secure Core Hobby Demand
- Bundle Cake Case Variety: Capitalize on the stable demand for baking by creating a "Baking Variety Pack" that includes different styles of Cake Cases (Pink Paisley, Retro Spot, Teatime Fairy). Price this bundle competitively to maximize volume from hobbyist purchases.

**Goal: Leverage the high-confidence multi-buy associations to protect the Average Transaction Value (ATV) and maintain stable revenue despite the lowest customer traffic volume.**





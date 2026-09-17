# Analysis Notes

## 1. Objective

This analysis examines domestic airline ticket data in India to understand how airline, route, number of stops, departure timing, and flight duration relate to ticket prices.

The dataset contains **10,683 flight records** and was analyzed using Google Sheets.

---

## 2. Overall Pricing Snapshot

The dataset shows an **average ticket price of ₹9,087.06**, while the **median ticket price is ₹8,372**.

The median being lower than the mean suggests that the dataset contains some higher-priced flights that pull the average upward.

The observed ticket prices range from **₹1,759 to ₹79,512**, showing substantial variation across flights.

The average flight duration is approximately **10.72 hours**.

These figures provide the overall context for the more detailed airline, route, stop, timing, and duration comparisons below.

---

## 3. Average Ticket Price by Airline

Average ticket prices vary considerably across airlines.

| Airline | Average Ticket Price |
|---|---:|
| Air Asia | ₹5,590 |
| Air India | ₹9,611 |
| GoAir | ₹5,861 |
| IndiGo | ₹5,674 |
| Jet Airways | ₹11,644 |
| Jet Airways Business | ₹58,359 |
| Multiple carriers | ₹10,903 |
| Multiple carriers Premium economy | ₹11,419 |
| SpiceJet | ₹4,338 |
| Trujet | ₹4,140 |
| Vistara | ₹7,796 |
| Vistara Premium economy | ₹8,962 |

### Finding

Jet Airways Business has a much higher average price than the other categories, at approximately **₹58.4K**. However, it appears only **6 times** in the dataset, so this average should not be treated as representative of the wider market.

Among airlines with larger numbers of observations, Jet Airways has an average price of approximately **₹11.6K**, followed by Multiple carriers at approximately **₹10.9K** and Air India at approximately **₹9.6K**.

SpiceJet, Trujet, Air Asia, GoAir, and IndiGo have lower average ticket prices in this dataset.

### Interpretation

Airline choice is associated with noticeable differences in observed ticket prices. However, the comparison reflects the routes, timings, cabin categories, and other characteristics represented in the dataset, so airline alone should not be interpreted as the cause of the price difference.

---

## 4. Flight Count by Airline

| Airline | Flight Count |
|---|---:|
| Jet Airways | 3,849 |
| IndiGo | 2,053 |
| Air India | 1,752 |
| Multiple carriers | 1,196 |
| SpiceJet | 818 |
| Vistara | 479 |
| Air Asia | 319 |
| GoAir | 194 |
| Jet Airways Business | 6 |
| Multiple carriers Premium economy | 13 |
| Trujet | 1 |
| Vistara Premium economy | 3 |

### Finding

Jet Airways represents the largest number of observations in the dataset with **3,849 flights**, followed by IndiGo with **2,053** and Air India with **1,752**.

This is important when interpreting average prices because airlines with very few observations can produce unstable averages.

### Interpretation

The dataset is not evenly distributed across airlines. Therefore, comparisons should consider both **average price and flight volume** rather than relying on price alone.

---

## 5. Flight Distribution by Number of Stops

| Stops | Flight Count |
|---|---:|
| Non-stop | 3,491 |
| 1 stop | 5,625 |
| 2 stops | 1,520 |
| 3 stops | 45 |
| 4 stops | 1 |

### Finding

Flights with **1 stop** are the largest group, with **5,625 flights**, while non-stop flights account for **3,491 flights**.

Only 45 flights have 3 stops and just 1 flight has 4 stops.

### Interpretation

The dataset is dominated by non-stop and one-stop journeys. The very small number of flights with 3 or 4 stops means conclusions about those categories should be treated cautiously.

---

## 6. Average Ticket Price by Number of Stops

The average observed price increases as the number of stops increases in the available data:

| Stops | Average Ticket Price |
|---|---:|
| Non-stop | ₹5,025 |
| 1 stop | ₹10,594 |
| 2 stops | ₹12,716 |
| 3 stops | ₹13,112 |
| 4 stops | ₹17,686 |

### Finding

Non-stop flights have an average price of approximately **₹5.0K**, compared with approximately **₹10.6K** for one-stop flights.

The averages continue to increase for journeys with two, three, and four stops.

### Interpretation

The observed pattern shows a strong difference in pricing across stop categories. However, this does **not** mean that adding stops directly causes a higher price. Routes, distance, airline, travel date, and other factors may also contribute to these differences.

The 3-stop and 4-stop averages are based on very small numbers of observations.

---

## 7. Top 10 Most Expensive Routes

The routes with the highest average ticket prices are:

| Route | Average Ticket Price |
|---|---:|
| BOM → DED → DEL → HYD | ₹24,115 |
| BOM → JDH → DEL → HYD | ₹23,867 |
| BOM → VNS → DEL → HYD | ₹23,528 |
| BOM → UDR → DEL → HYD | ₹22,950 |
| BOM → BDQ → DEL → HYD | ₹22,793 |
| DEL → DED → BOM → COK | ₹19,540 |
| DEL → IXU → BOM → COK | ₹19,381 |
| BOM → JDH → JAI → DEL → HYD | ₹18,293 |
| BOM → JAI → DEL → HYD | ₹17,926 |
| BLR → CCU → BBI → HYD → VGA → DEL | ₹17,686 |

### Finding

The highest-priced route in the analysis is **BOM → DED → DEL → HYD**, with an average ticket price of approximately **₹24.1K**.

Several of the highest-priced routes contain multiple intermediate stops, particularly routes involving Delhi and Hyderabad.

### Interpretation

Route composition appears to be an important dimension of price variation in the dataset. The results suggest that certain multi-leg routes have substantially higher observed average prices.

Because the analysis uses average prices, route-level differences may also reflect differences in travel dates, airlines, and other flight characteristics.

---

## 8. Average Ticket Price by Departure Time

| Departure Category | Average Ticket Price |
|---|---:|
| Afternoon | ₹9,218 |
| Morning | ₹9,132 |
| Evening | ₹8,989 |
| Night | ₹8,842 |

### Finding

Average prices are relatively close across the four departure-time categories.

Afternoon departures have the highest observed average at approximately **₹9.2K**, while night departures have the lowest at approximately **₹8.8K**.

The difference between the highest and lowest category is only about **₹376**.

### Interpretation

Departure timing shows a smaller pricing difference than some of the other dimensions analyzed. This suggests that, within this dataset, departure category is associated with relatively modest variation in average ticket price.

---

## 9. Ticket Price vs Flight Duration

The scatter plot compares flight duration in hours with ticket price.

The calculated Pearson correlation between duration and price is approximately **0.51**, indicating a **moderate positive linear association** in this dataset.

### Finding

Longer flights generally tend to be associated with higher ticket prices, although the scatter plot shows considerable variation around this overall pattern.

### Interpretation

Flight duration appears to be more strongly associated with ticket price than departure category in this analysis. However, correlation does not establish causation. Longer duration may also reflect longer routes, more stops, or other characteristics that influence price.

---

## 10. Key Takeaways

1. **Ticket prices vary substantially across airlines**, with some airline categories showing much higher average prices than others.
2. **Jet Airways has the largest number of observations** in the dataset, so its average price is based on a much larger sample than very small categories such as Jet Airways Business or Trujet.
3. **One-stop flights are the most common journey type**, followed by non-stop flights.
4. **Observed average prices increase across stop categories**, although the categories with 3 or 4 stops contain very few observations.
5. **Several of the highest-priced routes are multi-leg routes**, indicating that route composition is an important dimension for understanding price differences.
6. **Departure timing shows relatively small differences in average price**, with afternoon, morning, evening, and night averages all remaining within a fairly narrow range.
7. **Flight duration has a moderate positive correlation with ticket price (r ≈ 0.51)**, meaning longer flights generally coincide with higher prices in the dataset, but with substantial variation.

---

## 11. Limitations

- The dataset represents a specific collection of domestic flight observations and should not be treated as a complete representation of the Indian airline market.
- Airline categories have very different sample sizes.
- Some categories, such as Jet Airways Business, Trujet, and 4-stop flights, contain very few observations.
- The analysis is descriptive and does not establish causal relationships.
- Ticket prices can be affected by factors such as travel date, route, airline, stops, cabin type, and other variables.
- The dashboard focuses on patterns visible in the supplied dataset rather than forecasting future ticket prices.

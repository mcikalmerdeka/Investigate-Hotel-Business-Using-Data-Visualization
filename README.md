# Investigate Hotel Business Using Data Visualization

![Project Header](https://raw.githubusercontent.com/mcikalmerdeka/Investigate-Hotel-Business-Using-Data-Visualization/refs/heads/main/Assets/Project%20Header.jpg)

**This project originally came from an assignment after a data science bootcamp program that I attended. Which is why you can see there are several folders of tasks that contain instructions about business questions that must be answered based on data and my presentation file for each of them.**

## Project Description

- The hospitality industry encompasses businesses that provide accommodation for guests, including room reservations, meals, and other facilities. It can range from small to large enterprises, from one-star to five-star hotels. Success in this industry depends on factors such as location, service quality, and competitive pricing. The demand for comfortable and affordable accommodation makes the hotel business a viable option for entrepreneurs. It's important to understand the target market and the health of the hotel business to devise appropriate strategies and provide services and facilities tailored to their needs.
- This project will analyze the hotel business by processing historical data to obtain information about hotel bookings, length of stay, and the time interval between booking and cancellation.
- The dataset for this project can be found in `hotel_bookings_data.csv` file, contains booking information for a city hotel and a resort hotel, and includes information such as when the booking was made, length of stay, the number of adults, children, and/or babies, and the number of available parking spaces, among other things. All personally identifying information has been removed from the data.

Here is the initial walkthrough of the task:

- `Task 1` explains the EDA (Exploratory Data Analysis) and initial preprocessing stages, including handling missing & invalid values, addressing duplicated rows, transforming and filtering data, and conducting basic statistical analysis to prepare the dataset for further investigation.
- `Task 2` details the analysis comparing the number of hotel bookings each month based on hotel type (city hotel vs. resort hotel), helping to identify seasonal trends and booking patterns across different accommodation types.
- `Task 3` explores the correlation between customer stay duration and hotel booking cancellation rates, examining whether longer or shorter planned stays are more likely to result in cancellations.
- `Task 4` investigates whether the time interval between when a hotel booking is made and the customer's planned arrival date influences the cancellation rate of hotel reservations, providing insights into advance booking behaviors.

> For each task, the summary can be accessed in the presentation file and technical details can be accessed in the main `Investigate Hotel Business Using Data Visualization Code.ipynb` file.

## Analysis and Findings

### Task 1: Data Cleansing & Preprocessing Analysis

Our data preparation involved careful cleaning and transformation of the hotel bookings dataset to ensure quality analysis. Key preprocessing steps included:

- Handling missing values in critical fields such as children, city, and agent information
- Removing duplicate entries to prevent skewed results
- Creating a "total_guests" column by summing adults, children, and babies for easier occupancy analysis
- Calculating "stay_duration" by adding weekend and weekday nights to better analyze booking patterns
- Converting categorical month names to numerical values for time-based analysis

Through this preprocessing, we established a robust dataset with 118,564 valid hotel bookings spanning from 2017 to 2019 across city and resort hotels in Indonesia.

### Task 2: Monthly Hotel Booking Analysis Based On Hotel Type

The monthly booking pattern analysis revealed significant insights into seasonal trends and customer preferences:

- **City Hotels vs. Resort Hotels**: City hotels consistently receive higher booking volumes than resort hotels throughout the year, with an average of 3,051 bookings per month compared to 1,522 for resort hotels.
- **Seasonal Trends**: Both hotel types experience peak booking seasons during July-August and December, coinciding with major holiday periods. City hotels see their highest occupancy in July (11.18% of annual bookings), while Resort hotels peak in December (9.61%).
- **Year-over-Year Growth**: Both hotel types showed booking growth from 2017 to 2019, with city hotels experiencing more significant increases, particularly in Q3 and Q4.
- **Business Implications**: This seasonal pattern offers opportunities for strategic marketing and pricing. Hotels should implement dynamic pricing strategies during peak seasons (July-August and December) to maximize revenue, while offering promotional packages during low seasons (February-March) to stimulate demand. The consistent growth trend indicates a healthy market with expansion potential.

### Task 3: Impact Analysis Of Stay Duration On Hotel Bookings Cancellation Rates

Our analysis of stay duration and cancellation rates revealed compelling patterns:

- **Duration-Cancellation Correlation**: There is a strong positive correlation between stay duration and cancellation rates across both hotel types. The longer the planned stay, the higher the likelihood of cancellation.
- **Hotel Type Differences**: City hotels experience significantly higher cancellation rates than resort hotels across all stay durations:

  - For stays ≤1 week: City hotels (41.70%) vs. Resort hotels (27.78%)
  - For 2-week stays: City hotels (52.20%) vs. Resort hotels (28.92%)
  - For 3-week stays: City hotels (72.38%) vs. Resort hotels (46.75%)
  - For stays ≥4 weeks: City hotels (87.23%) vs. Resort hotels (42.59%)
- **Critical Thresholds**: The cancellation rate increases dramatically for longer stays, with city hotels showing an alarming 87.23% cancellation rate for bookings of 4+ weeks.
- **Business Recommendations**:

  - Implement tiered deposit requirements based on stay duration, with higher deposits for longer stays
  - Develop special incentives and loyalty benefits for guests booking extended stays to reduce cancellations
  - For city hotels, investigate the underlying causes of their significantly higher cancellation rates (potentially related to business travel changes or competitive pricing)
  - Consider flexible booking terms for longer stays while maintaining stricter policies for shorter stays

### Task 4: Impact Analysis Of Lead Time On Hotel Bookings Cancellation Rate

The analysis of lead time (time between booking and arrival) on cancellation rates yielded critical insights:

- **Lead Time-Cancellation Relationship**: Both hotel types show a clear pattern where longer lead times correlate with higher cancellation rates. Short-notice bookings (≤1 month) have the lowest cancellation rates: City hotels (22.47%) and Resort hotels (13.11%).
- **Critical Points**: The highest cancellation rates occur for bookings made 11-13 months in advance: City hotels (77.56%) and Resort hotels (41.15%). This suggests significant uncertainty in plans made roughly a year ahead.
- **Hotel Type Comparison**: City hotels consistently show higher cancellation rates than resort hotels across all lead time segments, suggesting different customer behaviors or expectations.
- **Strategic Implications**:

  - Implement dynamic pricing strategies that account for lead time, with different deposit requirements based on booking window
  - For bookings with longer lead times (8+ months), consider implementing non-refundable or partially refundable policies with appropriate discounts
  - Develop targeted marketing campaigns for different customer segments based on their typical booking timeframes
  - For city hotels, which face consistently higher cancellation rates, consider more aggressive overbooking strategies for bookings with extended lead times

## Cross-Task Analysis and Business Recommendations

Combining insights from all four analyses reveals several overarching patterns:

1. **City vs. Resort Hotel Dynamics**: City hotels consistently show higher booking volumes but also significantly higher cancellation rates. This suggests different customer segments with distinct behavior patterns—likely business travelers vs. leisure travelers.
2. **Interplay of Time Factors**: Both lead time and stay duration strongly impact cancellation rates, with longer values in either dimension increasing cancellation risk. These factors likely compound each other.
3. **Seasonal Considerations**: Peak booking seasons also present opportunities to optimize policies around lead time and stay duration to maximize revenue.

Recommended Business Strategies:

- **Segmented Pricing Models**: Develop dynamic pricing strategies that account for hotel type, booking season, lead time, and stay duration simultaneously
- **Targeted Marketing**: Create specialized marketing campaigns for each hotel type that emphasize their unique value propositions
- **Policy Optimization**: Implement flexible cancellation policies for resort hotels to maintain their lower cancellation rates, while adopting more structured approaches for city hotels
- **Revenue Management**: Use the seasonal booking patterns and cancellation probabilities to optimize overbooking strategies and maximize occupancy rates
- **Customer Experience Enhancement**: For city hotels particularly, focus on improving the guest experience to address the higher cancellation rates that persist across all dimensions

This comprehensive analysis provides a foundation for strategic decision-making in inventory management, marketing, pricing, and operational planning across different hotel types.

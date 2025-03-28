# Airline Data Analysis using Power BI

### Project Overview
This Power BI dashboard provides a comprehensive analysis of airline operations, focusing on key metrics such as passenger count, ticket booking statuses, and flight performance across various destinations. It allows users to gain insights into the number of passengers traveling with each airline, track booking trends, and analyze flight statuses for better operational decision-making. The interactive features enable dynamic filtering by airline and destination, allowing users to drill down into specific data for detailed analysis. The dashboard is designed to support strategic planning, improve customer insights, and optimize flight schedules, making it an invaluable tool for airline management and operations.

### Data Source
The dataset was provided by the Internshala Trainings Team as part of the PGC Data Science Curriculum. It comprises three files:
1. Flight_Information.xlsx
2. Passenger_Information.xlsx
3. Ticket_Information.xlsx
With over 200 records, the data was processed and analyzed using Power BI.

### Objective
This project aims to analyze airline operations using Power BI to enhance efficiency and customer satisfaction.
Key Objectives:
1. **Data Transformation & Integration** – Clean and preprocess flight, passenger, and ticket data using Power Query.
2. **Data Modeling** – Establish relationships between datasets for seamless analysis.
3. **DAX Calculations** – Implement custom measures for KPIs like Passenger Load Factor, Revenue Analysis, and On-Time Performance.
4. **Interactive Dashboards** – Create visual reports for passenger trends, flight performance, and booking insights.
5. **Business Insights** – Provide data-driven recommendations to optimize operations and improve customer experience.
Using Power BI, data transformation, data modeling, and DAX, this project delivers actionable insights for better decision-making.

### Measures
Some of the measures used are:
1.**Count of Total Passengers** - Can be filtered on through various slicer
Total Passengers = 
var totalPass = CALCULATE(
    COUNT(passenger_information[PassengerID]),
    passenger_information[FlightID] = SELECTEDVALUE(flight_information[FlightID])
)

var output = IF(totalPass<>BLANK(),totalPass,0)
return output

2. **Best Flights Table** - Flights whose status is best
BestFlights = 
FILTER (
    flight_information,
    flight_information[FlightCondition] = "Best"
)

### Key Insights
1. Total Customers -> 100
2. Total Tickets Booked -> 50
3. Total Confirmed Tickets -> 54%
4. Airline D has sold highest number of tickets but only 29% were confirmed.
5. Airline B hold 20% of Total Filght Share and 54% flights are in optimal condition along with 50% ticket confirmation rate.
6. **More insights and detail explanation can be found here : https://drive.google.com/file/d/1ZexPCKqCDrAA70cNQ57cmh-d7IjPyT82/view?usp=sharing**

### Power BI Dashboard
The dashboard is hosted on Power BI Service, but I have also provided the .pbix file, which can be downloaded for a detailed view of the dashboard.

### Conclusion and Recommendations
Our airline data analysis reveals key operational trends and performance gaps. Enhancing flight management and customer service is essential, with a focus on improving ticket confirmations and flight conditions.

#### Key Recommendations:
**Increase Operations in Houston**: Airline B and Airline D should expand their presence, as they currently operate only 6 and 9 flights, respectively, despite high demand.
**Enhance Punctuality & Reduce Cancellations**: With only 41% of flights arriving on time, improving scheduling efficiency and minimizing delays is crucial.

Implementing these changes will optimize operations and enhance passenger experience.

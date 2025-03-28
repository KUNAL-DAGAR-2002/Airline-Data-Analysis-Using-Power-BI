# ✈️ Airline Data Analysis using Power BI 📊  

## 🚀 Project Overview  
This **Power BI dashboard** provides a comprehensive analysis of **airline operations**, focusing on key metrics such as **passenger count, ticket booking statuses, and flight performance** across various destinations. It enables users to:  
✔️ Gain insights into the **number of passengers** traveling with each airline 👥  
✔️ Track **booking trends** 📅  
✔️ Analyze **flight statuses** for better operational decision-making 🛩️  

The interactive features allow **dynamic filtering** by airline and destination, enabling detailed **drill-down analysis** 🔍. This dashboard supports **strategic planning**, improves **customer insights**, and optimizes **flight schedules**, making it an invaluable tool for airline management.  

---

## 💂️ Data Source  
The dataset was provided by the **Internshala Trainings Team** as part of the **PGC Data Science Curriculum**. It consists of **three files**:  
📌 **Flight_Information.xlsx**  
📌 **Passenger_Information.xlsx**  
📌 **Ticket_Information.xlsx**  

With **over 200 records**, the data was processed and analyzed using **Power BI**.  

---

## 🎯 Objective  
This project aims to analyze **airline operations** using **Power BI** to enhance **efficiency and customer satisfaction**.  

### 🔑 Key Objectives:  
1️⃣ **🛠️ Data Transformation & Integration** – Clean and preprocess **flight, passenger, and ticket data** using **Power Query**.  
2️⃣ **📊 Data Modeling** – Establish **relationships** between datasets for seamless analysis.  
3️⃣ **📈 DAX Calculations** – Implement custom **measures for KPIs** like **Passenger Load Factor, Revenue Analysis, and On-Time Performance**.  
4️⃣ **📉 Interactive Dashboards** – Create **visual reports** for **passenger trends, flight performance, and booking insights**.  
5️⃣ **💡 Business Insights** – Provide **data-driven recommendations** to optimize operations and improve **customer experience**.  

Using **Power BI**, **data transformation, data modeling, and DAX**, this project delivers **actionable insights** for better decision-making.  

---

## 📏 Measures  
Here are some of the **DAX measures** used:  

1️⃣ **🧙️ Count of Total Passengers** – Filterable through slicers ✂️  
```DAX
Total Passengers = 
VAR totalPass = CALCULATE(
    COUNT(passenger_information[PassengerID]),
    passenger_information[FlightID] = SELECTEDVALUE(flight_information[FlightID])
)
VAR output = IF(totalPass<>BLANK(), totalPass, 0)
RETURN output
```  

2️⃣ **🏆 Best Flights Table** – Shows **flights in optimal condition** ✅  
```DAX
BestFlights = 
FILTER (
    flight_information,
    flight_information[FlightCondition] = "Best"
)
```  

---

## 🔍 Key Insights  
📌 **Total Customers** → **100**  
📌 **Total Tickets Booked** → **50**  
📌 **Total Confirmed Tickets** → **54%**  
📌 **✈️ Airline D has sold the highest number of tickets** but only **29% were confirmed** ❗  
📌 **🛩️ Airline B holds 20% of the total flight share**, with **54% of flights in optimal condition** and a **50% ticket confirmation rate**.  
📌 **📊 More insights and a detailed explanation can be found here:** **https://drive.google.com/file/d/1ZexPCKqCDrAA70cNQ57cmh-d7IjPyT82/view?usp=sharing**  

---

## 📊 Power BI Dashboard  
The dashboard is hosted on **Power BI Service**, but the **.pbix file** is also available for a detailed view of the dashboard.  

---

## 👀 Conclusion and Recommendations  
Our **airline data analysis** reveals key **operational trends** and **performance gaps**. Improving **flight management** and **customer service** is crucial, focusing on **ticket confirmations** and **flight conditions**.  

### ✅ Key Recommendations:  
1️⃣ **✈️ Increase Operations in Houston** 📍: **Airline B** and **Airline D** should **expand their presence**, as they currently operate only **6 and 9 flights, respectively**, despite high demand.  
2️⃣ **🕒 Enhance Punctuality & Reduce Cancellations** ⏳: With only **41% of flights arriving on time**, improving **scheduling efficiency** and **minimizing delays** is crucial.  

🔹 Implementing these changes will **optimize operations** and **enhance passenger experience** 🌟✨

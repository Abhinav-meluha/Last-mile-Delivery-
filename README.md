# Last-mile-Delivery

FA-2 Project — IBCP Career-related Study in Artificial Intelligence  
**Student:** Abhinav Chanakya & Vihan
**School:** Meluha International School  
**Course:** IB Career-related Programme (AI CRS)


##  Project Objective
This project aims to analyze **last-mile delivery performance** using an interactive **Streamlit dashboard**.  
The dashboard provides insights into delivery delays, agent performance, vehicle efficiency, and the impact of traffic and weather conditions.

By visualizing delivery data, logistics managers can identify delay patterns and optimize operations to improve on-time delivery rates.



##  Dataset Description
The dataset used is **“Copy of Last mile Delivery Data.csv”**, containing records of delivery agents, vehicles, and environmental factors.  

### **Key Columns**
| Column Name | Description |
|--------------|--------------|
| `Order_ID` | Unique order identifier |
| `Agent_Age` | Age of delivery agent |
| `Agent_Rating` | Customer rating for the agent |
| `Store_Latitude` / `Store_Longitude` | Store location coordinates |
| `Drop_Latitude` / `Drop_Longitude` | Customer location coordinates |
| `Weather` | Weather conditions during delivery |
| `Traffic` | Traffic level on delivery route |
| `Vehicle` | Type of vehicle used |
| `Area` | Delivery zone or region |
| `Category` | Type of product or order |
| `Delivery_Time` | Delivery completion time (in minutes) |



##  Features of the Dashboard
The dashboard includes **five interactive visualizations** built using `Plotly` and `Streamlit`.

1. **Delay Analyzer** – Average delivery time based on *Weather* and *Traffic* conditions.  
2. **Vehicle Comparison** – Compares delivery times across different vehicle types.  
3. **Agent Performance** – Relationship between *Agent Rating* and *Delivery Time*, grouped by *Age*.  
4. **Area Analysis** – Identifies regions with higher average delays.  
5. **Category Visualizer** – Distribution of delivery times by *Order Category*.

Additional metrics:
- Average delivery time  
- Average agent rating  
- Percentage of late deliveries



## Data Processing Steps
1. **Data Cleaning** – Removed missing values, standardized column names, converted numeric types.  
2. **Feature Engineering**  
   - Created a `late` flag → delivery_time > (mean + std)  
   - Grouped agents by age (`Under 25`, `25–40`, `40+`)  
3. **Visualization** – Built interactive charts using Plotly Express.  
4. **Interactivity** – Sidebar filters for Weather, Traffic, Vehicle, Area, and Category.



## Tools & Technologies
- **Language:** Python 3  
- **Framework:** Streamlit  
- **Libraries:** pandas, numpy, plotly, requests  
- **Deployment:** ngrok (temporary public link)  
- **Platform:** Google Colab / Streamlit Cloud



##  Requirements
All required dependencies are listed in `requirements.txt`.

```txt
streamlit==1.31.0
pandas==2.2.1
numpy==1.26.4
plotly==5.20.0
requests==2.31.0

This is frontend repository of MarketLens application. This application is developed using ReactJS. It uses libraries like

- Recharts for interactive charts
- Formik, Yup for form handling and validation
- React Router for routing
- Axios for API call
- React Query for data fetching and client side caching

The [backend code](https://github.com/saipavankalyan/MarketLens-Service) serves the APIs written in SpringBoot that internally queries Oracle DB using Spring Data JPA

Here is the Enity Relationship diagram of the database

![ER Diagram](ER_diagram.png 'ER Diagram')

## Overview and Description:

This Investment Market Trend Analysis will be a UI-driven application that will help both newbies into the world of market and trading and existing investors learn new insights by analyzing the correlation between sectors and different financial instruments (Bonds, Commodities, Stocks, etc.). It will also enable a better understanding of macroeconomic factors such as the Consumer Price Index (CPI), Unemployment Rate with Treasury Bonds, and Stocks (Index Performance). Since the time frame chosen for this exercise had several unexpected events, like war and the COVID-19 pandemic, we can find how such events affect the market. Some Investments improved during the pandemic, while others flopped. This will enable us to realize the complex inter-connected nature of global trade. As said earlier, the application will be UI driven. In general, the application will expect the user to input the parameters like (Inflation, CPI, Retail Sales, and Payroll) or a combination of both as the independent variable. The user can select up to any granularity(month, quarter, year) to see its dependence on the chosen independent variable. It can be a financial instrument as a whole like (Stocks, Treasury Bonds, or Cryptocurrencies) or the user can drill deep and choose a particular sector of stock, Tech sector, or Pharma sector or can even drill deep and choose a particular entity, Tesla (TSLA), Treasury Bond (3 yr yield rate), Ethereum Crypto and see its dependence. It's possible to find a trend analysis of a particular entity over a specific time period.

The user can filter time through sliders. Some predefined  time sliders will be available as dropdowns for users to select, indicating the timeline of the war, the  timeline of the COVID pandemic, and the timeline of theoretical recession for specific usecases like news influence. The backend will be written using the Spring-Boot framework in java. It will involve interacting with the Database and fetching using appropriate dynamically generated queries and returning results using JSON. The front end will be written using React.js and will call the backend server with appropriate requests based on user input and will show the response from the backend server on the web app as interactive charts. The backend is purposefully separated to allow other forms of clients like ios, android apps to use the same backend in the future.

These are the major screens, each provide specific insights

### Economic Influence on Sectors

This dashboard provides an interactive analysis of the correlation between various economic indicators, such as the Federal Repo rate and the unemployment rate, and their impact on different economic sectors including Information Technology, Healthcare, Energy, and more. Users can select specific indicators from a dropdown menu to visualize and analyze the trends.

### Insights

The above walk through reveals several key insights during Covid-19(first half of 2020):

- **Unemployment Rate and Fed Repo rate:** As the COVID-19 pandemic emerged, unemployment rates surged dramatically. In response, the government reduced the Federal Repo rate to alleviate cash shortages and provide financial support to citizens.
- **Energy Sector:** The Energy sector experienced significant setbacks as industries were forced to shut down and people stayed at home, leading to reduced energy consumption.
- **Healthcare Sector:** Conversely, the Healthcare sector saw substantial growth due to increased investments in vaccine development and the urgent need to expand hospital capacities to manage the influx of COVID-19 patients.
- **Information Technology Sector:** The IT sector also benefited significantly during this period. The swift transition to remote work drove demand for collaboration technologies such as Zoom and Microsoft Teams. Additionally, with people spending more time at home, digital content consumption soared, boosting the revenues and profits of IT companies and leading to stock price increases.

### Risk vs Reward

This dashboard provides comprehensive insights into the risk and reward profiles of various asset classes such as the S&P 500, Dow Jones, and cryptocurrencies. Users can select their target asset class and customize the granularity of the chart to view data on a monthly, quarterly, or yearly basis over a specified time period. The dashboard displays two key graphs: a reward graph based on asset growth and a risk graph based on the standard deviation of the asset class within the selected time period.

### Insights

The analysis reveals several important insights:

- **Cryptocurrency:** Despite exhibiting high risk, as evidenced by the elevated standard deviation, cryptocurrencies have shown substantial rewards in the selected time period. This high-risk, high-reward dynamic is particularly pronounced in this asset class.
- **S&P 500:** The S&P 500, known for its relatively conservative risk profile, has demonstrated moderate performance within the given time period. While the risk is lower compared to cryptocurrencies, the reward is also more modest, reflecting the S&P 500's stability and gradual growth.

These insights help users understand the trade-offs between risk and reward for different asset classes, aiding in more informed investment decisions.

### Growth of Growth

This dashboard offers detailed insights into the performance of individual stocks over specified time periods, with the option to analyze data at monthly or quarterly granularities. Users can select specific stocks and time frames to visualize and compare their growth trajectories.

### Insights

The analysis highlights several key insights:

- **Amazon and Tesla (2016-2022):** In the selected time period, both Amazon and Tesla have demonstrated remarkable growth. Notably, Tesla has shown exceptional performance in the latter years, outpacing Amazon in terms of growth rate. This "growth of growth" analysis underscores the impressive upward trajectories of these two stocks over the past decade.

These insights allow users to delve into the performance metrics of high-performing stocks, facilitating a deeper understanding of their growth patterns and potential future performance.

### Sector Contribution

This dashboard provides insights into how the top-performing stocks contribute to the overall growth of their respective sectors over a specified time period. Users can select a sector and define the value of k (top 5 or top 10) to generate a chart illustrating the contributions of these leading stocks.

### Insights

The analysis reveals several important insights:

- **Financial Sector Analysis:** In the example walkthrough, analyzing the financial sector shows that JP Morgan Chase has made the highest contribution to the sector's growth. This highlights the significant impact of top-performing stocks on the overall performance of their sectors.

These insights help users understand the key drivers of sector growth, providing a clearer picture of how individual stock performance influences broader market trends.

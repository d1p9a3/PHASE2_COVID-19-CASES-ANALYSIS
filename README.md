# PHASE2_COVID-19-CASES-ANALYSIS
COVID-19 
import pandas as pd
import matplotlib.pyplot as plt

# Sample COVID-19 dataset (replace with your dataset)
data = {
    'Date': pd.date_range(start='2023-01-01', periods=30),
    'Cases': [100, 150, 200, 250, 300, 350, 400, 450, 500, 550,
              600, 650, 700, 750, 800, 850, 900, 950, 1000, 1050,
              1100, 1150, 1200, 1250, 1300, 1350, 1400, 1450, 1500, 1550],
    'Deaths': [5, 8, 12, 15, 20, 25, 30, 35, 40, 45,
               50, 55, 60, 65, 70, 75, 80, 85, 90, 95,
               100, 105, 110, 115, 120, 125, 130, 135, 140, 145],
    'Recovered': [30, 50, 70, 90, 110, 130, 150, 170, 190, 210,
                  230, 250, 270, 290, 310, 330, 350, 370, 390, 410,
                  430, 450, 470, 490, 510, 530, 550, 570, 590, 610]
}

# Create a DataFrame from the dataset
df = pd.DataFrame(data)
# Plot COVID-19 cases over time
plt.figure(figsize=(12, 6))
plt.plot(df['Date'], df['Cases'], label='Cases', marker='o')
plt.plot(df['Date'], df['Deaths'], label='Deaths', marker='x')
plt.plot(df['Date'], df['Recovered'], label='Recovered', marker='s')
plt.xlabel('Date')
plt.ylabel('Count')
plt.title('COVID-19 Cases Analysis')
plt.legend()
plt.grid(True)
plt.xticks(rotation=45)
plt.show()


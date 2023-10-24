import pandas as pd
import numpy as np
import matplotlib.pyplot as plt 

# load datasheet
data = pd.read_csv('4.csv')  # Adjust the file path if necessary

# pilih kolom
raw_data = data.iloc[:, 1]

# definikana fungsi mva
def moving_average(data, window_size):
    return data.rolling(window=window_size, min_periods=1).mean()

# set ukuran window untuk mva filter
window_size = 5  

# Apply the moving average filter
mva_filtered_data = moving_average(raw_data, window_size)

# visualisasikan hasil dalam grafik
plt.figure(figsize=(10, 6))
plt.plot(raw_data, label='Raw Data')
plt.plot(mva_filtered_data, label='MVA Data')
plt.legend()
plt.title('Raw Data vs. MVA Data (X-axis)')
plt.xlabel('Sample Index')
plt.ylabel('Acceleration')
plt.show()

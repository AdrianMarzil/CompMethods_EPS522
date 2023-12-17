## Lab 5: Abstraction - Modules

### Module: velocity_analysis.py

<b>Python functions include:</b> 
1. import_tenv3
2. fit_timeseries
3. fit_velocities
4. get_coordinates
5. fit_all_velocities

<b> How to Use: </b>
1. Import module:
import velocity_analysis

2. Specify the folder and pattern for timeseries files
folder_path = '/Users/Adrian/Documents/VS CODE/CompMethods_EPS522/Labs/Lab 5/timeseries'
file_pattern = '*.NA.tenv3'

3. Use the module to estimate velocities for all sites
df = velocity_analysis.fit_all_velocities(folder_path, file_pattern)

4. Print the results
print(df)

5. Save the results to a CSV file
df.to_csv('site_velocities.csv', index=False)

### Module: tidal_analysis.py

<b>Python functions include:</b> 
1. import_rlrdata
2. fit_timeseries
3. fit_tidal_gauge
4. fit_all_rates

<b> How to Use: </b>
1. Import module:
import tidal_analysis

2. Specify the folder and pattern for your timeseries files
folder_path = '/Users/Adrian/Documents/VS CODE/CompMethods_EPS522/Labs/Lab 5/tidal_timeseries'
file_pattern = '*.rlrdata'

3.  Use the module to estimate tidal rates for all sites
df = tidal_analysis.fit_all_rates(folder_path, file_pattern)

4. Print the results
print(df)

5. Save the results to a CSV file
df.to_csv('site_tides.csv', index=False)
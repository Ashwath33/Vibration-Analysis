# Vibration-Analysis
Contains details and codes related to Vibration Analysis and Machine Asset Monitoring 
This a Web application developed with Plotly Dash to visualize, diagnose and interpret vibration data from a MEMS based sensor. 

# Problem statement
The Data set provides information on key vibration, temperature and audio from the sensor mounted on a Machine Spindle. The Sesor records data for every 30 mins and the dataset comprises of 643 rows and 20 columns. The Objective of developing this application is to visualize, diagnose and analyze vibrations from the sensor that would help the end user for asset optimization and maintenance activities

# Approach
Since the Application demands a GUI, Plotly Dash was chosen for the Dashboard and Visualization components. The Approach was to give two windows to the User - One to Analyse Vibration parameters which would include setting Specification limits of thresholds across parameters and also setting a required time period to analyze the data. The Second window helps the user in prediction of a parameter trend in the coming days and also diagnose possible faults in the system based on Data Analysis. The Code was constructed with Jupyter Notebook 6.3.0

# Implementation
Constructing the Web App involved setting layouts for the different tabs. The Data was filtered and cleaned using pandas. The Analyis Tabs includes Input boxes created with dcc.Input component that takes Threshold inputs from the User. A dcc.datepicker component is given wherin the user will be able to select the specific date period to analyze. 

The Analytics tab includes a piechart and linechart created with plotly express. The Piechart shows a summary of the Selected vibration parameter interms of Good, Alert and Danger (bins as received from User specification inputs) and the Line chart shows a trend of selected parameter over the data range specified. The User will be able to hover over the line graph to see individual data points at each timestamp recorded and also be visually able to compare the range of parameter with a color coded background

The Predictions tab includes a dcc.dropdown component that lets the user to select the parameter to predict. A Line graph forecasts the trend of the parameter over the next 3 days. The Prediction is based on ARIMA Models after ensuring stationarity of the data and validation. A textbox displays a message indicating a possible machinery fault based on the data and specification set. An Fault animation is displayed to help the user understand and interpret the likely fault. 

# Running the Code
Please ensure that the Code and the CSV Data is in the same folder. Install all relevant packages and libraries as given in the Code

<span id="top">Data Visualization with Python | Course | IBM</span>

# Data Visualization with Python - Final Project
<br>

| <b> Task 1 &rarr; [Completed Notebook](https://github.com/wy-chan/Python-Data-Visualization-Project/blob/main/Final%20Assignment%20Part%201.jupyterlite.ipynb) </b> |
| -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <b> Task 2 &rarr; [Completed Codes](https://github.com/wy-chan/Python-Data-Visualization-Project/blob/main/DV0101EN-Final_Assign_Part_2_Questions_Completed.py) </b> |

---

<!-- TABLE OF CONTENTS -->
## Table of Contents:

<h3><u><a href="#task1">Task 1:</a> Create visualizations using Matplotib, Seaborn and Folium</u></h3>

- [Task 1.1](#Q1_1) - Line chart
- [Task 1.2](#Q1_2) - Line chart
- [Task 1.3](#Q1_3) - Bar chart
- [Task 1.4](#Q1_4) - Sub plott
- [Task 1.5](#Q1_5) - Bubble plot
- [Task 1.6](#Q1_6) - Scatter plot
- [Task 1.7](#Q1_7) - Pie chart
- [Task 1.8](#Q1_8) - Pie chart
- [Task 1.9](#Q1_9) - Count plot

  <br>
  
<h3><u><a href="#task2">Task 2:</a> Create Dashboard with Plotly and Dash</u></h3>

- [Task 2.1](#Q2_1) - Title
- [Task 2.2](#Q2_2) - Drop-downs
- [Task 2.3](#Q2_3) - Output Division
- [Task 2.4](#Q2_4) - Callback Function
- [Task 2.5](#Q2_5) - Recession Report Statistics
- [Task 2.6](#Q2_6) - Yearly Report Statistics

<br>

---

<div id="task1">
<h2>Task 1: Create visualizations using Matplotib, Seaborn and Folium</h2>
<div id="Q1_1">
  
- [x] <b>Task 1.1 - Develop a Line chart using the functionality of pandas to show how automobile sales fluctuate from year to year (1 point)</b>
  
  |![Line Plot 1](Data%20Visualization%20-%20Screenshots/Line_Plot_1.png)|
  |-|
  
</div>


---

<div id="Q1_2">
  
- [x] <b>Task 1.2 - Plot different lines for categories of vehicle type and analyse the trend to answer the question "Is there a noticeable difference in sales trends between different vehicle types during recession periods?" (1 point)</b>
  
  |![Line Plot 2](Data%20Visualization%20-%20Screenshots/Line_Plot_2.png)|
  |-|
  
</div>

---

<div id="Q1_3">
  
- [x] <b>Task 1.3 - Use the functionality of Seaborn Library to create a visualization to compare the sales trend per vehicle type for a recession period with a non-recession period. (1 point)</b>
  
  |![Bar Chart](Data%20Visualization%20-%20Screenshots/Bar_Chart.png)|
  |-|
  
</div>

---

<div id="Q1_4">
  
- [x] <b>Task 1.4 - Use sub plotting to compare the variations in GDP during recession and non-recession period by developing line plots for each period. (2 points)</b>
  
  |![sub plotting](Data%20Visualization%20-%20Screenshots/Subplot.png)|
  |-|
  
</div>

---

<div id="Q1_5">
  
- [x] <b>Task 1.5 - Develop a Bubble plot for displaying the impact of seasonality on Automobile Sales. (1 point)</b>
  
  |![Bubble plot](Data%20Visualization%20-%20Screenshots/Bubble.png)|
  |-|
  
</div>

---

<div id="Q1_6">
  
- [x] <b>Task 1.6 - Use the functionality of Matplotlib to develop a scatter plot to identify the correlation between average vehicle price relate to the sales volume during recessions. (1 point)</b>
  
  |![scatter plot](Data%20Visualization%20-%20Screenshots/Scatter.png)|
  |-|
  
</div>

---

<div id="Q1_7">
  
- [x] <b> Create a pie chart to display the portion of advertising expenditure of XYZAutomotives during recession and non-recession periods. (1 point)</b>
  
  |![pie chart 1](Data%20Visualization%20-%20Screenshots/pie_1.png)|
  |-|
  
</div>

---

<div id="Q1_8">
  
- [x] <b>Task 1.8 - Develop a pie chart to display the total Advertisement expenditure for each vehicle type during recession period. (1 point)</b>
  
  |![pie chart 2](Data%20Visualization%20-%20Screenshots/pie_2.png)|
  |-|
  
</div>

---

<div id="Q1_9">
  
- [x] <b>Task 1.9 - Develop a countplot to analyse the effect of the unemployment rate on vehicle type and sales during the Recession Period. (1 point)</b>
  
  |![count plot](Data%20Visualization%20-%20Screenshots/count_plot.png)|
  |-|
  
</div>

</div>

---

<div id="task2">
<h2>Task 2: Create Dashboard with Plotly and Dash</h2>
  
</div>


<div id="Q2_1">
  
- [x] <b>Task 2.1 - Create a Dash application and give it a meaningful title. (2 points)</b>
  
  |![Title](Data%20Visualization%20-%20Screenshots/Title.png)|
  |-|

<code>
html.H1("Automobile Sales Statistics Dashboard", style={'textAlign': 'center', 'color': '#503D36', 'font-size': '24px'})
</code>
  
</div>

---

<div id="Q2_2">
  
- [x] <b>Task 2.2 - Add drop-downs to your dashboard with appropriate titles and options. (1 point)</b>

  
  |![Drop-downs](Data%20Visualization%20-%20Screenshots/Dropdown.png)|
  |-|

<code>
 html.Div([
        #TASK 2.2: Add two dropdown menus
        html.Label("Select Statistics:"),
        dcc.Dropdown(
            id='dropdown-statistics',
            options= dropdown_options,
            placeholder='Select a report type',
            value='Select Statistics',
            style={'textAlign': 'center', 'font-size': '20px', 'width': '80%', 'padding':'3px'},
        )
    ]),
    html.Div(dcc.Dropdown(
            id='select-year',
            options=[{'label': i, 'value': i} for i in year_list],
            placeholder='Select Year',
        )),
</code>
  
</div>

---

<div id="Q2_3">
  
- [x] <b>Task 2.3 - Add a division for output display with appropriate 'id' and 'classname' property. (1 point)</b>


  
  |![Output Division](Data%20Visualization%20-%20Screenshots/Outputdiv.png)|
  |-|

<code>
html.Div([
        #TASK 2.3: Add a division for output display
         html.Div(id='output-container', className='chart-grid', style={'display':'flex'}),
        ]),
</code>
  
</div>

---

<div id="Q2_4">
  
- [x] <b>Task 2.4 - Creating Callbacks; Define the callback function to update the input container. (5 points)</b>
  
  |![Callback Function](https://github.com/wy-chan/Python-Data-Visualization-Project/blob/main/Data%20Visualization%20-%20Screenshots/Callbacks.png)|
  |-|

<code>
#TASK 2.4: Creating Callbacks
# Define the callback function to update the input container based on the selected statistics
@app.callback(
    Output(component_id='select-year', component_property='disabled'),
    Input(component_id='dropdown-statistics',component_property='value'))

def update_input_container(selected_statistics):
    if selected_statistics =='Yearly Statistics': 
        return False
    else: 
        return True

#Callback for plotting
# Define the callback function to update the input container based on the selected statistics
@app.callback(
    Output(component_id='output-container', component_property='children'),
    [Input(component_id='select-year', component_property='value'), Input(component_id='dropdown-statistics', component_property='value')])


def update_output_container(input_year, selected_statistics):
    if selected_statistics == 'Recession Period Statistics':
        # Filter the data for recession periods
        recession_data = data[data['Recession'] == 1]
      
</code>
  
</div>

---

<div id="Q2_5">
  
- [x] <b>Task 2.5 - Create and display graphs for Recession Report Statistics. (3 points)</b>
  
  |![Recession Report Statistics](Data%20Visualization%20-%20Screenshots/RecessionReportgraphs.png)|
  |-|

<code>
#TASK 2.5: Create and display graphs for Recession Report Statistics

#Plot 1 Automobile sales fluctuate over Recession Period (year wise)
        # use groupby to create relevant data for plotting
        yearly_rec=recession_data.groupby('Year')['Automobile_Sales'].mean().reset_index()
        R_chart1 = dcc.Graph(
            figure=px.line(yearly_rec,
                x='Year',
                y='Automobile_Sales',
                title="Average Automobile Sales Fluctuation Over Recession Period"))

#Plot 2 Calculate the average number of vehicles sold by vehicle type       
        # use groupby to create relevant data for plotting
        average_sales = recession_data.groupby('Vehicle_Type')['Automobile_Sales'].mean().reset_index()                           
        R_chart2  = dcc.Graph(
            figure=px.bar(average_sales, 
            x='Vehicle_Type',
            y='Automobile_Sales',
            title="Average Number Of Vehicles Sold By Vehicle Type"))

        
# Plot 3 Pie chart for total expenditure share by vehicle type during recessions
        # use groupby to create relevant data for plotting
        exp_rec= recession_data.groupby('Vehicle_Type')['Advertising_Expenditure'].sum().reset_index()
        R_chart3 = dcc.Graph(
                    figure=px.pie(exp_rec,
                    values='Advertising_Expenditure',
                 names='Vehicle_Type',
                 title="Total Expenditure Share By Vehicle Type During Recessions"
                )
        )

# Plot 4 bar chart for the effect of unemployment rate on vehicle type and sales
        average_sales = recession_data.groupby(['unemployment_rate','Vehicle_Type'])['Automobile_Sales'].mean().reset_index()                           
        R_chart4  = dcc.Graph(
                figure=px.bar(average_sales, 
                x='unemployment_rate',
                y='Automobile_Sales',
                color = 'Vehicle_Type',
                title="The Effect Of Unemployment Rate On Vehicle Type And Sales Over Recession Period"))


        return [
            html.Div(className='chart-item', children=[html.Div(children=R_chart1),html.Div(children=R_chart2)]),
            html.Div(className='chart-item', children=[html.Div(children=R_chart3),html.Div(children=R_chart4)])
            ]
</code>
  
</div>

---

<div id="Q2_6">
  
- [x] <b>Task 2.6 - Create and display graphs for Yearly Report Statistics. (2 points)</b>
  
  |![Yearly Report Statistics](https://github.com/wy-chan/Python-Data-Visualization-Project/blob/main/Data%20Visualization%20-%20Screenshots/YearlyReportgraphs.png)|
  |-|

<code>
# TASK 2.6: Create and display graphs for Yearly Report Statistics
 # Yearly Statistic Report Plots                             
    elif (input_year and selected_statistics=='Yearly Statistics') :
        yearly_data = data[data['Year'] == input_year]
                              
#plot 1 Yearly Automobile sales using line chart for the whole period.
        yas= data.groupby('Year')['Automobile_Sales'].mean().reset_index()
        Y_chart1 = dcc.Graph(
                figure=px.line(yas,
                x='Year',
                y='Automobile_Sales',
                title="Average Automobile Sales Fluctuation Over Time"))
            
# Plot 2 Total Monthly Automobile sales using line chart.
        mas= yearly_data.groupby('Month')['Automobile_Sales'].sum().reset_index()
        Y_chart2 = dcc.Graph(
                figure=px.line(mas,
                x='Month',
                y='Automobile_Sales',
                title="Total Monthly Automobile Sales in the year {}" .format(input_year)))

# Plot bar chart for average number of vehicles sold during the given year
        avr_vdata=yearly_data.groupby('Vehicle_Type')['Automobile_Sales'].mean().reset_index()
        Y_chart3 = dcc.Graph(
                figure=px.bar(avr_vdata,
                x='Vehicle_Type',
                y='Automobile_Sales',
                title='Average Vehicles Sold by Vehicle Type in the year {}'.format(input_year)))

# Total Advertisement Expenditure for each vehicle using pie chart
        exp_data=yearly_data.groupby('Vehicle_Type')['Advertising_Expenditure'].sum().reset_index()
        Y_chart4 = dcc.Graph(
                figure=px.pie(exp_data,
                values='Advertising_Expenditure',
                names='Vehicle_Type',
                title='Average Vehicles Sold by Vehicle Type in the year {}'.format(input_year)))

#TASK 2.6: Returning the graphs for displaying Yearly data
        return [
                html.Div(className='chart-item', children=[html.Div(children=Y_chart1),html.Div(children=Y_chart2)]),
                html.Div(className='chart-item', children=[html.Div(children=Y_chart3),html.Div(children=Y_chart4)])
                ]
        
    else:
        return None
</code>
  
</div>


</div>

---

<p align="center"> - <a href='#top'>Back to Top</a> | <a href='#task1'>Task 1</a> | <a href='#task2'>Task 2</a> - </p>


# Pymaceuticals

In this analysis I used mock pharmaceutical trial data (mouse_metadata.csv & study_results.csv, "Resources") to analyze potential treatment regimens for squamous cell carcinoma (SCC). In particular, this analysis compares the performace of Pymaceuticals' drug of interest, Capomulin, to other treatment regimens.

# Tools Used

- Python
- Pandas
- Matplotlib
- Jupyter Notebook
- Linear Regression

# Instructions

Before beginning the analysis, I checked the data for any mouse ID with duplicate time points and removed any data associated with that mouse ID. I then used the cleaned data for the remaining steps.

First, I generated a summary statistics table consisting of the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen.

![summary table](Images/summary_table.png)

Next, I generated a bar plot using both Pandas's DataFrame.plot() and Matplotlib's pyplot that shows the total number of measurements taken for each treatment regimen throughout the course of the study. NOTE: These plots should look identical.

![bar_plot_pandas](Images/bar_plot_pandas.png) ![bar_plot_mpl](Images/bar_plot_mpl.png)

Then, I generated a pie plot using both Pandas's DataFrame.plot() and Matplotlib's pyplot that shows the distribution of female or male mice in the study. NOTE: These plots should look identical.

![pie_chart_pandas](Images/pie_chart_pandas.png) ![pie_chart_mpl](Images/pie_chart_mpl.png)

Then, I calculated the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. I was sure to calculate the quartiles and IQR in order to quantitatively determine any potential outliers across the four treatment regimens.

Using Matplotlib, I generated a box and whisker plot of the final tumor volume for all four treatment regimens and highlighted any potential outliers in the plot by changing their color and style.

![final_tv](Images/final_tv_box_whisker.png)

Next, I selected a mouse that was treated with Capomulin and generated a line plot of tumor volume vs. time point for that mouse.

![line_plot](Images/line_plot.png)

I then generated a scatter plot of mouse weight versus average tumor volume for the Capomulin treatment regimen.

![scatter_plot](Images/scatter_plot.png)

Finally, I calculated the correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment, plotting the linear regression model on top of the previous scatter plot.

![lin_reg](Images/lin_reg.png)

# Final Observations 

Capomulin and Ramicane appear to be the most promising drugs for treating SCC, as both drugs' average final tumor volume is about 35-36mm³. The data showed that when treated with Capomulin, tumor size decreased for all test subjects over a span of 45 days. Alternately, Ceftamin and Infubinol appeared to be far less effective, with the average final tumor volume for both equaling around 65-66mm³. The data also shows a strong, positive correlation between mouse weight and tumor volume, suggesting increased tumor size with increased weight.

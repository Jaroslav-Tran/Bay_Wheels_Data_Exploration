# Bay_Wheels_Data_Exploration
My exploration of a FordBike(Bay Wheels) 2019 dataset showcasing key differences between two user types of this service: customers and subscribers.

<h2> Dataset chosen </h2>
Baywheels (FordBike) 2019 data available here: https://www.lyft.com/bikes/bay-wheels/system-data

<h2> Main Findings </h2>
<ol>
     <li> It is very likely that Subscribers are mostly daily commuters who use this service as a healthier alternative to driving a car or taking a public transportations as the peak times are around 8-9 am and 5-6 pm. </li>
     <li> Customers also have peaks around those times but the demand over the day is more or less consistent so I would assume that those are most likely tourist and use bikes for their bay area visit and trips </li>
     <li> The commuters(subscribers) clearly have the most bike trips during the workweek (Mon-Fri) whereas tourist(customers) demand for the bikes is more or less the same every day. </li>
     <li> What is quite interesting is that the longest trip for both Subscribers and Customers happen around 3 AM in the morning. It would be interesting to look deeper and find out why. (Hypothesis: Maybe they are using the bikes after parties?)</li>
     <li> The duration for both groups (especially the customers) is much higher during the weekend.</li>
</ol>

<h3> How I chose to put the results into explanatory analysis </h3>
<p> As I was quite thorough and precise with the charts and analysis during the exploratory phase, I did not need to do many changes
in the explanatory phase. I copied the most interesting and descriptive charts to the slide generator template and used nbconvert to create a deck. </p>


<h2> What to expect in each notebook </h2>

<h3> Bay Wheels Data Exploration dataset contains </h3>
<ol>
    <li> Step by step data gathering and data wrangling process </li>
        <ul>
            <li> Data Quality Issue Resolution: Converting start and end time objects into a timestamp format.</li>
            <li> Data Quality Issue Resolution: Converting bike_id, end_station_id, start_station_id from floats and int into the objects </li>
        </ul>
    <li> Univariate Exploration - Bike trip distribution among each user type: There is substantially more Subscribers (Over 20M) in this dataset than Customers (480K). That could impact potential applications statistical models. (Barplot) </li>
    <li> Univariate Exploration - Bike trip distribution among shared and unshared trips: There is substantially more non-bike sharers (2.2M) than bike sharers. (180K) (Barplot) </li>
    <li> Univariate Exploration - Bike trip distribution each month: The peaks are in March, April and July. The low points are in May(Surprise), November and December. The distribution looks like a random distribution even though one would expect a normal distribution based on seasonality but that could be explained by the bike-friendly weather in the Bay Area throughout the year. (Barplot) </li>
    <li> Univariate Exploration - Bike trip distribution each weekday: Peaks on Tuesday with 427K trips. Sunday is the worst with 212K trips. The distribution is righ-skewed. (Barplot) </li>
    <li> Univariate Exploration - Bike trip distribution each hour of the day: Bimodal distribution with two peaks at 8 am and 5 pm which perfectly coincides with the commuting time. (Barplot) </li>
    <li> Univariate Exploration - A histogram of bike trip duration in minutes: Right skewed distribution with a mean of 13 minute duration. Most trips last between 5-8 minutes. (Histogram)  </li>
    <li> Bivariate Exploration - Trip duration comparison between each user type: Median trip duration for Subscribers is ~7.5 minutes compared to Customer´s ~11 minutes. The trip duration range is much higher for customers with a range of ~34 min compared to Subscriber´s ~24 min. 50% of Subscriber trips last 5-13 min whereas for Customers it is 6-17 min. (Boxplot) </li>
    <li> Bivariate Exploration - Trip duration comparison between bikesharers and non-bikesharers. Median trip duration for bike sharers is ~7 min and for non-bike sharers it is ~9 min. The trip duration range for bike sharers is around 6 minutes and for non-sharers around 9 min. 50% of bike sharers trips last 4.8-11 min and for non-bike sharers 5-14 min. (Boxplot) </li>
    <li> Bivariate Exploration - Month by month comparison of usage by each user type: The subscriber monthly distribution looks random and customer´s is slightly skewed to the left. The peak months for subscribers are March, April and July. For customers its October and December. (Catplot) </li>
    <li> Multivariate Exploration - Weekday trip duration breakdown by each user type: For customers, the duration is fairly uniform on the weekdays and peaks during the weekend. Subscribers follow more or less the same pattern. (Barplot) </li>
    <li> Multivariate Exploration - Hour by hour trip duration breakdown by each user type: What is interesting is that the duration peaks around 3am for both groups. My hypothesis is that these long trips at these hour are likely party people trying to get home. (Barplot) </li>
    <li> Multivariate Exploration - Trip duration breakdown by each user type and bikeshare (Barplot): Whether subscribers share or not, it does not affect a duration that much as there is only ~2 minute difference. There is no comparison for customers since they dont do bikesharing. </li>
</ol>

<h3> Bay Wheel Slide Deck Generator contains </h3>
<p> This notebook is a subset of the Bay Wheel Data Exploration dataset containing 
only the Multivariate part of the analysis (With a polish) and was created to make the Nbconversion to slide deck smoother </p>

<h2> Process Taken </h2>
<p> The process I followed was pretty straightforward. I defined some interesting questions, variables and possible relationships and explored them in the exploratory phase.
Once I felt that there were enough interesting insights, I included the most interesting ones in the Slide Generator notebook (Explanatory stage) where I polished them and explained them more in depth. </p>

<h2> Sources </h2>
<ol>
    <li>Dataset: https://www.lyft.com/bikes/bay-wheels/system-data </li>
    <li>Seaborn documentation: https://seaborn.pydata.org/ </li>
    <li>Matplotlib documentation: https://matplotlib.org/3.2.0/contents.html </li>
    <li>Plotting: https://medium.com/@purnasaigudikandula/exploratory-data-analysis-beginner-univariate-bivariate-and-multivariate-habberman-dataset-2365264b751 </li>
    <li>Plotting: https://www.machinelearningplus.com/plots/top-50-matplotlib-visualizations-the-master-plots-python</li>
    <li> Converting notebooks to slides: https://medium.com/@mjspeck/presenting-code-using-jupyter-notebook-slides-a8a3c3b59d67</li>
    <li> Converting notebooks to slides: https://stackoverflow.com/questions/53186944/accommodating-large-slides-in-jupyter-presentation</li>
 </ol>

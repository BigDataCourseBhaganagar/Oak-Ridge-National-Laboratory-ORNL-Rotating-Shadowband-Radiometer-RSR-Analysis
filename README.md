# Oak-Ridge-National-Laboratory-ORNL-Rotating-Shadowband-Radiometer-RSR-Analysis
Gonzalo Martinez Medina

## Abstract
 
Oak Ridge National Laboratory uses a rotating shadowband radiometer to measure solar radiance in the Oak Ridge National Lab. Data files are available from September 2007 to November 2019. The station has the ability to measure global horizontal radiation (W/m2), diffuse horizontal irradiance, also known as diffuse sky radiation (W/m2), direct normal irradiance (W/m2), and direct normal (bird estimate) using an algorithm that produces estimates of clear sky direct beam.  Each irradiance factor can be paired with meteorological components such as air temperature (℃), relative humidity (%), wind speed(m/s), wind direction (degrees from N), estimated barometric pressure (mBar), precipitation and accumulated precipitation (mm), temperature of the CR800 datalogger panel (℃), and the voltage charge of the battery that powers the datalogger and the shadowband (V). The data set from the available dates can be selected in 1-minute intervals, hourly intervals, or daily statistics.

## Problem Statement

1.	Identify changes of measured factors across time. What has changed? When? How do season affect the factors, and which factor show no impact.
2.	Assess impact of radiation as a link to climate research and climate change.
3.	Determine possible solar power output as an alternative based on the data collected.
4.	Determine correlation between variables. Analyze high/low correlations and impact.
5.	Eliminate possible outliers from dataset.

## Expected Tools

Pandas descriptive statistics, specific python modules for dataset, statistical functions, frequencies, SciPy, Numpy discrete Fourier transformation, visualization with Matplotlib toolkit, and use of in class templates, Met_py modules to plot contour and surface maps of the analyzed region.

## Data

Data can be found here: 
https://midcdmz.nrel.gov/apps/daily.pl?site=ORNL&start=20070912&yr=2019&mo=11&dy=20

and the following table can be edited to extract desired data:
<p align="left">
  <img src="/Data selection image.JPG" height="800" title="hover text">
</p>


Data download can be done:
https://drive.google.com/drive/folders/1pQK7fA5RbQu3xF0XiIua30coFAGFY3mX?usp=sharing

The python program will lead you step by step on analyzing the data to proof the hypothesis that a possible solar power output can be 
obtained in that laboratory given the radiation measured throughout the years.

Yearly data for all 13 type of variables is analyzed, and the main components of the data base are:

A) Irradiance Variables
* Avg Global Horizontal [W/m^2]: is the total solar radiation received from above by a surface horizontal to the ground. This value is of particular importance for photovoltaic installations and includes Direct Normal Irradiance and Diffuse Horizontal Irradiance.
* Avg Direct Normal [W/m^2]: is the amount of solar radiation received per unit area by a surface that is always held perpendicular (or normal) to the rays that come in a straight line from the direction of the sun at its current position in the sky. Typically, you can maximize the amount of irradiance annually received by a surface by keeping it normal to incoming radiation. This quantity is of particular interest to concentrating solar thermal installations and installations that track the position of the sun.
* Avg Diffuse Horizontal [W/m^2]: Diffuse Horizontal Irradiance is the amount of radiation received per unit area by a surface (not subject to any shade or shadow) that does not arrive on a direct path from the sun, but has been scattered by molecules and particles in the atmosphere and comes equally from all directions.
* Avg Direct (Bird estimated) [W/m^2]: is an estimate measurement done by the Bird Clear Sky Model, authored by Richard Bird, which is a broadband algorithm that produces estimates of clear sky direct beam, hemispherical diffuse, and total hemispherical solar radiation on a horizontal surface.

B) Meteorological Variables (no detail needed)
* Avg Air Temperature [deg C]          
* Avg Rel Humidity [%]               
* Avg Avg Wind Speed @ 42ft [m/s]      
* Avg Est Pressure [mBar]              
* Avg Precipitation [mm]               

C) Other Variables
* Avg CR800 Temp [deg C]: is the temperature of the CR800 datalogger panel.
* Avg RSR Battery [VDC]: The RSR Battery powers the datalogger and the shadowband, it is charged by a photovoltaic panel, units in Volts of Direct Current.

### Now we take a look at the data types:

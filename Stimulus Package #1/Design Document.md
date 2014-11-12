In your team’s docs repository, make a file called 004-design-1.md. It should answer these questions:
     What are the other parts of your software? For example, for an MVC app: What models will you make? What attributes and methods will they have? What controllers will you make? What methods will they have? What views will you make?

Design Document

# Programming Language
- Javascript
- HTML
- CSS
- MySQL

# Other Tools/Libraries
- Amazon Web Services (Where we are hosting our application)
- Null School (Application we are modifying)
- jQuery
- Node.js
- Grib2JSON
- D3 Library
- LAMP Stack (For Server)
- NOAA Weather Data
- WMO Weather Data 
- NODC Weather Data
- NDBC Weather Data

# Architecture 
- Model View Controller

# Database
- MySQL database
- Relational Database
- Will store weather data
	= Observed Data
	= Forecasted Data
	= Difference Between the Data

# Notes
- We are simply altering and modfying an already existing application

- How Null School Works With Weather Data: 
= They pull data a file from ttp://nomads.ncep.noaa.gov/ in GRIB format then convert it to JSON 
= Place the JSON file into the directory earth/public/data/weather/current/current-wind-surface-level-gfs-1.0.json
= They have automated this process
= They have code that accesses this json file and renders the weather data that we see.

- These files are the one that are controlling the logic of pulling the data and rendering it on the globe.
= /earth/public/libs/earth/1.0.0/earth.js  
= /earth/public/libs/earth/1.0.0/globes.js  
= /earth/public/libs/earth/1.0.0/micro.js  
= /earth/public/libs/earth/1.0.0/products.js

- Design Decisions
= Division of system modes 
== “Null School Mode” - houses the predicted data visualization 
== “Quotaero Mode” - houses the actual data visualization 
== “Difference Layer Mode” - houses the visualization for the differences between the actual and predicted weather data. 
	should allow for a selection of year/month/day/hour to be displayed 



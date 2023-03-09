# Surfs Up!

Time to go on vacation, but first, let's check out the precipitation patterns in Hawaii. For this project, I used SQLAlchemy and a SQLlite database with station and precipitation totals for a range of years. The analysis examined:
* Dailiy precipitation averages for a year leading up to the most recent date in the dataset
* The total number of weather stations
* The most active station
* A histogram of the temperature and number of readings at that station

The second part of the prject uses Flask to create and API and series of endpoints to the data. The routes created are:

<b>/api/v1.0/precipitation</a></b> <br />
This route returns a json dictionary of dates and precipitation amounts that day
<br />
<br />
<b>/api/v1.0/stations</a></b><br />
This route returns a json list of stations from the data
<br />
<br />
<b><a href=\"/api/v1.0/tobs\">/api/v1.0/tobs</a></b> <br />
This route returns a json list of temperature observations for the last year <br />
from the most active weather station<br />
<br />
<br />
<b><a href=\"/api/v1.0/start/2014-09-09\">/api/v1.0/start</a></b> <br />
This route returns a json list of min, max and avg temps for all dates after a provided start date.<br />
from the most active weather station<br />
<br />
<br />
<b><a href=\"/api/v1.0/range?start=2014-09-14&end=2016-02-14\">/api/v1.0/range</a></b> <br />
This route returns a json list of min, max and avg temps for a given date range.<br />
You can enter a range or specify only a start and end date.<br /><br />
If only a start or end is specified, all dates from the data set leading up to<br />
or following that end date will be returned.<br /><br />
Dates should be passed in yyyy-mm-dd format using <i>start</i> and <i>end</i> parameters.<br />
(for example: /api/v1.0/range?start=2014-09-14&end=2016-02-14)

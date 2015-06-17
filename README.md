# Jaspersoft_InputControlsFromCSV

This is a simple project to show how to load input controls via the API.
The idea is that you have an input control that could pull 1M rows. You want a way to filter this.
So in this case we create a simple report that returns the id and value you want in the control.
You call that report asking for CSV, parse the results, and then load your UI element.

So there is a report in the backend to pull the csv for the input control and a report on the front end where those values are used.

This is based on the foodmart db, but the connection datasource is foodmart601, so double check that and the IP addresses used in the JS.

It should be a good example of exercising the API, and interesting use of a report, and a quick sample of visualize.js.

It is important to note that the "report" in the backend is requested to output CSV only. This is returned in the JS and parsed to build the input controls.

This is really the only neat part about the whole customization. Other than that it is a typical selector that then passes the results to the report run.
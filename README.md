# BrowserHistory_ELK
Script parse the browser history (Chrome, IE, and Firefox) and push the results to elasticsearch database



### Usage: 
This script used to push parse and push web history files to elasticsearch database
change the values for:
es_link: link to the elasticsearch database
es_index: index to push to on the database
browser: define the browser name (chrome,IE,firefox)
path: path of the web history file (
	chrome 	-> "History" file
	IE 		-> "WebCacheV01.dat" file
	firefox -> "places.sqlite"


### Output

the script parse the webshells and get a json output from three functions:

> extract_chrome_history

> extract_webcachev01_dat

> extract_firefox_history


the json results has a common fields among all the parser functions
> @timestamp    : used for the elasticsearch timeline

> browser_name  : the browser name 

> link          : the url

> time          : same as the timestamp, the visit, downloads, etc. time

> type          : visitis or downloads

the result then pushed to elasticsearch database as json

### Example from Kibana
![alt text](https://github.com/salehmuhaysin/BrowserHistory_ELK/blob/master/kibana.png?raw=true)

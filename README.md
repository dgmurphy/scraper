# Scraper

 A fork of the OEDA Scraper. See the original repo for more detailed information:
 https://github.com/openeventdata/scraper


## Prerequisites
Requires MonoDB.
 
## Install

```git clone https://github.com/dgmurphy/scraper.git```

```cd scraper```

### Create Python Environment & Install libraries

Create a Python2 virtual environment:

```virtualenv -p /usr/bin/python2.7 venv```

Activate the virtual environment:

```source venv/bin/activate```

Install the setuptools library (this step required for nltk install)

```pip install setuptools==9.1```

Install the libxml dependecies:

```sudo apt-get install libxml2-dev libxslt-dev python-dev```

Unzip the nltk library file:

```tar -xzvf nltk-2.0.4.tgz```

Install the nltk 2.0.4 library:

```pip install ./nltk-2.0.4```

*Q: Why not use the requirments.txt file to install the nltk library?*

*A: This is an old library version that requires a manual installation.*

Install the other required libraries for the scraper project:

```pip install -r requirements.txt```

### Do a Test Run of Scraper

Verify that the file `default_config.ini` has this line which will specify a short list of URLs to scrape for test purposes:

```file = whitelist_urls_short.csv```

Run the scraper:

`python scraper.py`

When it completes, inspect the log to verify that it added entries:

```vim scraper_log.log```

You should see a number of "added entry" lines with news article urls.


### MongoDB

Check the 'stories' collection in the 'event_scrape' database to view the scraped content.
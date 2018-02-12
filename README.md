# python-urlscan
Simple python class to interface with UrlScan.io


# Usage
```python
from urlscan import *

#Public scan, default useragent, no referer
u = UrlScan("apikey","https://google.com")
#Private scan, default useragent, no referer
u = UrlScan("apikey","https://google.com",public=False)
#Private scan, custom useragent, no referer
u = UrlScan("apikey","https://google.com",public=False,useragent="python-urlscan")
#Private scan, custom useragent, custom referer
u = UrlScan("apikey","https://google.com",public=False,useragent="python-urlscan",referer="https://github.com")

#Starting a scan
u.submit() #Wait a few seconds for the scan to complete, you can check with u.checkStatus()

#Getting the DOM
dom = u.getDom()

#Getting the screenshot
screenshot = u.getScreenshot()
```

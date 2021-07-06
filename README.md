The Complete Splunk Beginner Course (2021)
Homeworkdata.cvs Dataset

Search Queries
 
host="MEKHIS-PC" 

host="splunk/main" 
aka homeworkdataset  (creating a table view from this data)
Fields are “ip”, “time”, “state”.
 

















Creating a pivot

Demo

Searches:
host="splunk/main" backupduration=* domain=* | table _time backupduration domain
host="splunk/main" backupduration=* domain=* | stats max(backupduration) by domain
host="splunk/main" backupduration=* domain=* | stats max(backupduration)
host="splunk/main" backupduration=* domain=* | stats avg(backupduration)







host="splunk/main" | eval new_time=strftime(_time, "%m-%d-%y %I:%M%p") | table _time new_time




index="_internal"



index=_* OR index=* sourcetype=splunk_web_access | table _time protocol IP
Added 2 new fields called “protocol and “IP”

Building Dashboard WIth pivot (Not using the SPL)




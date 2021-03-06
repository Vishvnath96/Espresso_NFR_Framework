Performance testing is an important weapon before launching any product in market because customer reviews are highly based on performance. 
This is caused when there are either hardware issues or coding error.this cause a decrease of output under specific load conditions. Bottleneck is generally fixed by identifying cause and fixing poor process.

# Some common bottlenecks are:
1. Disk usage
2. Memory utilization
3. Network utilization
4. Operating System limitations
5. CPU utilization

# Espresso_NFR_Framework
Espresso NFR Framework for extracting memory cpu and network usage data automatically by using google api.
By Using this Framework we can easily capture android performance stats like CPU(user space,system space),Memory(Native,Dalvik,Private shared etc),
Network(RX/TX for mobile and WiFi data usage) and Frozen frames info after every ui test run and 
dump data into my sql/opentsdb data base for  current version of app and compare this data with previous version.It gives clear picture for if performance
degraded and get info for culprit classes and thread by heap dump and method trace.

# metrices to measure
![](https://github.com/Vishvnath96/Android-Espresso-PerformanceTest-Framework/blob/master/mem.png)

# Architecture
![](https://github.com/Vishvnath96/Android-Espresso-PerformanceTest-Framework/blob/master/Android.png)
1.Before running every test we clear shared prefrence and data base data so that before every test case app should be in fresh state.
2. After ui test pass test then only we capture memory usage,cpu usage and network usage and send this data into db.
3.Once we have data in db we can use in visualizing and reporting purpose.


# Alerting and monitoring:
![](https://github.com/Vishvnath96/Android-Espresso-PerformanceTest-Framework/blob/master/memoryStats.png)
We uses grafana dashboard for continous monitoring and alerting.
# For detailed info:
kindly refer below link
https://medium.com/makemytrip-engineering/non-functional-metrics-evaluation-of-makemytrip-android-app-ebffb4bdf91c




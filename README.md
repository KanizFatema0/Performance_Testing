# Performance Testing Using JMeter

This document explains how to run a performance test with JMeter for the given testing site, also includes the report for it along with report generated using Blazemeter for a website bangla puzzle.

# Testing Site
Testing Site - "https://restful-booker.herokuapp.com"

# Technologies Used
- Jmeter
- BlazeMeter

  
# Prerequisites
As of JMeter 5.6, Java 8+ and above are supported.
we suggest multicore cpus with 4 or more cores.
Memory 16GB RAM is a good value.


# Installations
Java

https://www.oracle.com/java/technologies/downloads/
JMeter

https://jmeter.apache.org/download_jmeter.cgi
Click =>Binaries
=>apache-jmeter-5.6.3.zip

We use BlazeMeter to generate JMX files

https://chrome.google.com/webstore/detail/blazemeter-the-continuous/mbopgmdnpcbohhpnfglgohlbhfongabi?hl=en,

# Elements of a minimal test plan
- Thread Group

  The root element of every test plan. Simulates the (concurrent) users and then run all requests. Each thread simulates a single user.

- HTTP Request Default (Configuration Element)

- HTTP Request (Sampler)

- Summary Report (Listener)

# Test Plan
Testplan > Add > Threads (Users) > Thread Group (this might vary dependent on the jMeter version you are using)

- Name: Users

- Number of Threads (users): 1 to 30

- Ramp-Up Period (in seconds): 3

- Loop Count: 3

i. The general setting for the tests execution, such as whether Thread Groups will run simultaneously or sequentially, is specified in the item called Test Plan.

ii. All HTTP Requests will use some default settings from the HTTP Request, such as the Server IP, Port Number, and Content-Encoding.

iii. Each Thread Group specifies how the HTTP Requests should be carried out. To determine how many concurrent "users" will be simulated, one must first know the number of threads. The number of actions each "user" will perform is determined by the loop count.

iv. The HTTP Header Manager, which allows you to provide the Request Headers that will be utilized by the upcoming HTTP Requests, is the first item in Thread Groups.

# Test execution (from the Terminal)
- keep your jmx file in bin
- JMeter should be initialized in non-GUI mode.
- Make a report folder in the bin folder.
- Run Command in ./jmeter folder
# Command
Jtl file generate command
```
jmeter -n -t demo.jmx -l report\demo.jtl


```
Report Generate command
```
jmeter -g report\ demo.jtl -o report\demo.html
```
# JMeter Project Images
<img width="1440" alt="Screenshot 2024-12-06 at 3 25 02 PM" src="https://github.com/user-attachments/assets/1c3a1319-2af3-464f-a694-f8e393334f10">

# Report
<img width="1440" alt="Screenshot 2024-12-06 at 3 27 10 PM" src="https://github.com/user-attachments/assets/4d18825a-0f88-4085-a580-37cda2ffef34">

# Blazemeter

<img width="1440" alt="Screenshot 2024-12-06 at 3 29 58 PM" src="https://github.com/user-attachments/assets/cca32fc7-da61-4083-9044-24e8090b1db9">








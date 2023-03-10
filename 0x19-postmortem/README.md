QUIZZERS routine maintenance releases bug leading to outage.


Issue Summary

From 5:30 AM to 2:15 PM WAT, requests to our Server resulted in 100 error response messages. The quizzers website was unable to be accessed by users as a result of our server not being able to receive requests to serve web content .The root cause of the outage was as a result of a routine maintenance carried out on our server  which unexpectedly released a bug in our database.

Timeline(WAT)
5:30 AM: Outage begins
5:30 AM: Pager alerted teams
12:00 PM: Successful location of released bug
1:00 PM : Successful containment of released bug
1:10 PM: Severe restart begins
2:15 PM: 100% of traffic back online

Root Cause
Routine maintenance on our web servers inadvertently released a bug which was overlooked during the testing phase which ended up affecting our database.The bug caused our servers to be unable to receive requests as the database containing content to be served could not be accessed.This caused traffic to be permanently queued waiting for a serving thread to become available.

Resolution and recovery

At 5:30 AM WAT, the monitoring systems alerted our engineers who investigated and quickly escalated the issue. By 5:50 AM, the incident response team identified that the monitoring system was exacerbating the problem caused by this bug.

At 10:00 AM, we attempted to locate the bug but as a result of the complexity in the configuration systemIt proved difficult . These problems were addressed and we successfully located the bug at 12:00 PM.

To help with the recovery of our server, we turned off the server in order to reboot.We started the  servers gradually (at 1:29 PM), to avoid possible cascading failures from a wide scale restart. By 2:00 PM, 25% of traffic was restored and 100% of traffic .



Corrective and Preventative Measures

In the last week, we’ve conducted an internal review and analysis of the outage. The following are actions we are taking to address the underlying causes of the issue and to help prevent recurrence and improve response times:
Ensure the testing phase before deployment is thorough to avoid bugs being overlooked.
Develop a technique that will enable the team to locate bugs much more accurately and precisely within a short duration in order to improve response time.

Quizzers is committed to continually and quickly improving our technology and operational processes.

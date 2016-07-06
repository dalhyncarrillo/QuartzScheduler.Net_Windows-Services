# Quartz.Net with Windows Service
Link: http://www.quartz-scheduler.net/

This contains the code for creating a windows scheduler job by using Quartz.net. Also using the log4net to write the log into a text file. The configuration info to start the job be configured in configuration.xml file. The job will repeat forever after some sleep times.

Go to Configuration.xml file to update the value for timeframe:

<?xml version="1.0" encoding="utf-8"?>
<config>
  <chienvh>
    <scheduleInterval>
      <!--Start: Set the times for the job start again-->
      <days>0</days>
      <hours>0</hours>
      <minutes>01</minutes> <!--For example, after 1 min the job will start again-->
      <!--/End: Set the times for the job start again-->

      <!--Start: Set the date and time to start the job in the 1st time-->
      <startAtDate>07/06/2016</startAtDate>
      <startAtHours>22</startAtHours>
      <startAtMinutes>32</startAtMinutes>
      <!--/End: Set the date and time to start the job in the 1st time-->

      <!--Explaination: In the above example, after installing the windows service, the job will
      start at 22:32 and today is 06 July 2016. After the job excuted the 1st time, it will sleep 1 minute
      and will start again as a loop, this job won't stop unless you stop or unintall the windows service by youself-->
    </scheduleInterval>
  </chienvh>
</config>



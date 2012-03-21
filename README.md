[Bootstrap Calendar](http://github.com/ahmontero/bootstrap-calendar)
=================
The aim of this plugin is to have a simple calendar to show events using Bootstrap. It can be improved for sure. You are welcome to do it!



Requisites
-----------

+ Bootstrap (http://github.com/twitter/bootstrap)
+ jQuery (http://jquery.com/)



Quick start
-----------

.
.
.

var evnts = function(){
              return {
                      "event":
                          [
                               {"date":"2012-01-25","title":"1"}
                              ,{"date":"2012-02-01","title":"2"}
                          ]
                      }
          };

$('#calendar').Calendar({ 'events': evnts, 'weekStart': 1 })

         .on('changeDay', function(event){ alert(event.day.valueOf()); })

         .on('onEvent', function(event){ alert(event.day.valueOf()); })

         .on('onNext', function(event){ alert("Next"); })

         .on('onPrev', function(event){ alert("Prev"); })

         .on('onCurrent', function(event){ alert("Current"); });
.
.
.
<div id="calendar"></div>
.
.
.




Parameters
------------

weekStart: 1|2|3|4|5|6|7

msg_days: Text for week days. Default: ["Su", "Mo", "Tu", "We", "Th", "Fr", "Sa"]

msg_months: Text for months. Default: ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"]

msg_today: Text for 'Today' button. Default: 'Today'

events: Events to show in the calendar. Format: {"event":[{"date":"2012-01-25", "title":"1"}]}

# DoxIfos_Calendar
An dynamic calendar to help patients keep track of their cancer infusion schedule (with doxorubicin and ifosfamide). Specifically made to print handouts for sarcoma patients in Dr. Davis' Vanderbilt Clinic.

**HTML is live for use on my website:** [emcarthur.github.io/projects/DoxIfos_Calendar/](http://emcarthur.github.io/projects/DoxIfos_Calendar/)

**Sample PDF Schedule downloaded from the website:** [emcarthur.github.io/projects/DoxIfos_Calendar/sample_schedule.pdf](http://emcarthur.github.io/projects/DoxIfos_Calendar/sample_schedule.pdf)

Dr. Davis' clinic is on M/Th so the schedule will start patient cycles on the upcoming M/Th. Labs and clinic visit at white blood cell count nadir is on day 10 for patients that start on Monday and day 11 for patients that start on Thursday.

Based extensively on html/javascript/css from [Fullcalendar](https://fullcalendar.io/).

All events can be dragged and dropped to different days in case the clinician is out of town and holds clinic on a different day.



To customize to your own schedule, change these parts of the `index.html` document:
```

	if (day == 0) { # this says if the current day is a Sunday, 
	  d = d + 1;    # day 1 of the cycle is the current day plus 1
	  d10 = d + 10; # and day 10 of the cycle is an additional 10 days from that
	} else if (day == 1) { # if the current day is a Monday, day 1 is today
	  d10 = d + 10;        # and day 10 is an additional 10 days from that
    
    ...
    
  events: [
	  {
        title: 'CYCLE 1', 
        start: new Date(y, m, d, 1), # cycle 1 starts on the day specified in the if-elseif statement above
        color: 'black' # event will be in a black box
		},
 
   ... # add more events here
```
Last edited 9/3/2019

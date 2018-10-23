# pdfscraper_raw
#
This program will pull tabulated data from ET-Rate Tables in the LCRAS Reports from 1995 to 2011.
It collects 13 values from a specific label, unless there is 12 values only.  These 13 values are 
the monthly values and the sum total of the months. For this specific program I have divided the parts 
for collection into 5 different parts. These 5 parts are (1)Reference ET, (2)Precipitation, (3)Crops, (4)Open Water,
and (5)Riparian Crops. The program works by finding a specific page in the pdf and converting all the text 
on that page into one large string. Then a Regular Expression is needed to match the text in the string 
variable. An example of this would be @"Open water " + @"((\-?\d+)+?(\.\d+)?)\s".  The first part is the matching
label and the other part is the value. The matching function is very percise be aware of spaces and parentheses
that would require escape charactrers. If it successfully finds a match it will be printed into the output file 
immediately. 

note:
Regular Expression positive/negative whole number and positive/negative decimal number
// @"((\-?\d+)+?(\.\d+)?)\s"


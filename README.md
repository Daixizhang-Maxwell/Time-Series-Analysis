# Time-Series-Analysis
Date time object is not a builtin datatype for python, instead we need to import a module called “datetime” in order to use it. By employing this module, we will  make many different methods and attributes for the datetime object available for us.

## Basic Datetime object

#### Import The module:

In order to deal both simple and complex problems with time, the datetime module are consist of 5 different classes:

            date -- Manipulate [Month, Day, Year]
            Time -- Manipulate [Hour, Minute, Second, Microsecond]
            Datetime -- Manipulate [Month, Day, Year, Hour, Minute, Second, Microsecond]
            Timedelta --The changes between two datetime object
            Tzinfo -- an abstract class that deals with timezone

How can you call the different classes listed above? There are two ways:

            1. from datetime import datetime / date / time
            2. Import datetime as dt
               A_instance = dt.datetime() / dt.date() ...

####  Create Datetime object:

There are basic two ways to create a datetimem object: 1. Create datetime object by using then datetime module and classes; 2. Convert strings and other forms of record of datetime to datetime object

1. Date1 = dt.datetime(1999,1,1,1,1, 1)

2. This one is a bit tricker because we are not sure about the format of the string. By format I mean how different time component are managed within the string, for example:

            a. YYYY-MM-DD  2018-12-1
            b. YYYY/MM/DD   2018/12/1
            c. MM-YY-DD  12-18-1                    
            d. MM-YY-DD   Dec-18-1  ….

         
Thus how can we deal with such complexity? The solution is using representing symbols and the following two method:

             strftime(format)  -- from datetime object to string
             datetime.strptime() -- from a string to a datetime object with a corresponding format string.

Symbol Representation (for more please refer to https://docs.python.org/3/library/datetime.html#strftime-and-strptime-behavior):

            Year:  %Y  4-digit year: 2020; %y 2-digit year: 20
            Month: %B Month in English, complete way: December; %b Month in English, short way: Dec; %m Month in number: 12
            Day: %d Day in number: 01-31; 
            Hour: %H Hour in number: 0-23;
            Second: %S Seconds in number: 00-59;
            Microseconds: %f Microsecond in number: 000000-999999;
          
## Pandas & Datetime object



datecalc-go
========
######v1.0.0

datecalc is created by Violet (http://pariahvi.com) and is licensed under a BSD License. Read LICENSE.txt for more license text.

Go library to calculate the day of the week of any date

####Dependencies
* Go

####Using the Library
To calculate the day of the week for any date, use *datecalc.date(y, m, d, t)* where y is the full year (a negative integer for BC years), m is the month number, d is the day number, and type is the calendar type.  The calendar types you have to chose from are:
* English
* Roman
* Gregorian
* Julian
* CE

English is the calendar system the English speaking western countries are using.  This is a system where the calendar was under the Julian system until 1752, when it switched to the Gregorian Calendar, skipping  September 3rd and going straight to September 15th to offset for the differences in the calendar systems on how they incorporated leap years.

Roman is the calendar system the Roman Empire used.  This was a system where the calendar was under the Julian until 1582, when it switched to the Gregorian Calendar, skipping October 5th and going straight to October 16th to offset for the differences in the calendar systems on how they incorporated leap yars.

####Example Uses
```
package main

import (
    "datecalc"
    "fmt"
)

func main() {
    fmt.Println(datecalc.Date(2014, 3, 14, "English"))
    fmt.Println(datecalc.Date(2014, 3, 14, "Roman"))
    fmt.Println(datecalc.Date(-2014, 3, 14, "English"))
    fmt.Println(datecalc.Date(-2014, 3, 14, "Julian"))
    fmt.Println(datecalc.Date(2014, 3, 14, "Julian"))
    fmt.Println(datecalc.Date(204727298871375019846193105719886136647191237731911139435, 3, 14, "Julian"))
    fmt.Println(datecalc.Date(-204727298871375019846193105719886136647191237731911139435, 3, 14, "English"))
}

```
prints out:
```
Friday
Friday
Friday
Wedneday
Wedneday
Thursday
Monday
Saturday
```

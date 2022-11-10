# strftime()
A JavaScript port of [`strftime()`](http://man7.org/linux/man-pages/man3/strftime.3.html), a function to format the date and time.

### Supported conversion specifications:

| Sequence | Description | Example |
|----------|-------------|---------|
| `%a`  | Abbreviated name of the day of the week. | Fri |
| `%A`  | Full name of the day of the week. | Friday |
| `%b`  | Abbreviated month name. | Apr |
| `%B`  | Full month name. | April |
| `%c`  | UTC date and time representation for the current locale. | Sat 02 Apr 2022 00:15:00 GMT |
| `%C`  | Century number (year/100) as a 2-digit integer. | 20 |
| `%d`  | Day of the month as a decimal number (range 01 to 31). | 01 |
| `%e`  | Day of the month as a decimal number (range 1 to 31). | 1 |
| `%F`  | ISO 8601 date format (equivalent to `%Y-%m-%d`). | 2022-04-01 |
| `%g`  | Like `%G`, but without century, that is, with a 2-digit year. | 22 |
| `%G`  | ISO 8601 week-based year with century as a decimal number. The 4-digit year corresponds to the ISO week number (see `%V`). This has the same format and value as `%Y`, except that if the ISO week number belongs to the previous or next year, that year is used instead. | 2022 |
| `%H`  | Hour as a decimal number using a 24-hour clock (range 00 to 23). See also `%k`. | 17 |
| `%I`  | Hour as a decimal number using a 12-hour clock (range 01 to 12). See also `%l`. | 05 |
| `%j`  | Day of the year as a decimal number (range 001 to 366). | 091 |
| `%k`  | Hour as a decimal number using a 24-hour clock (range 0 to 23). See also `%H`. | 17 |
| `%l`  | Hour as a decimal number using a 12-hour clock (range 1 to 12). See also `%I`. | 5 |
| `%m`  | Month as a decimal number (range 01 to 12). | 04 |
| `%n`  | Month as a decimal number (range 1 to 12). | 4 |
| `%M`  | Minute as a decimal number (range 00 to 59). | 15 |
| `%p`  | Either "AM" or "PM" according to the given time value. Noon is treated as "PM" and midnight as "AM". | PM |
| `%P`  | Like `%p` but in lowercase ("am" or "pm"). | pm |
| `%s`  | Number of seconds since the Epoch, 1970-01-01 00:00:00 +0000 (UTC). | 1648858500 |
| `%S`  | Second as a decimal number (range 00 to 59). | 00 |
| `%u`  | Day of the week as a decimal (range 1 to 7), Monday being 1. See also `%w`. | 5 |
| `%V`  | ISO 8601 week number of the current year as a decimal number (range 01 to 53), where week 1 is the first week that has at least 4 days in the new year (that is, the first Thursday). | 13 |
| `%w`  | Day of the week as a decimal (range 0 to 6), Sunday being 0. See also `%u`. | 5 |
| `%x`  | Preferred date representation for the current locale without the time. | 4/1/2022 |
| `%X`  | Preferred time representation for the current locale without the date. | 5:15:00 PM |
| `%y`  | Year as a decimal number without a century (range 00 to 99). | 22 |
| `%Y`  | Year as a decimal number including the century. | 2022 |
| `%z`  | The `+hhmm` or `-hhmm` numeric timezone (that is, the hour and minute offset from UTC). | -0800 |
| `%Z`  | Timezone name. | Pacific Standard Time |
| `%Zs` | Timezone short name (abbreviation). | PST |

### Compatibility notes:

* `%c` - formatted string is slightly different
* `%D` - not implemented (use `%m/%d/%y` or `%d/%m/%y`)
* `%e` - space is not added
* `%E` - not implemented
* `%h` - not implemented (use `%b`)
* `%k` - space is not added
* `%n` - like `%m`, but no leading zero (use `\n` for newline)
* `%O` - not implemented
* `%r` - not implemented (use `%I:%M:%S %p`)
* `%R` - not implemented (use `%H:%M`)
* `%t` - not implemented (use `\t`)
* `%T` - not implemented (use `%H:%M:%S`)
* `%U` - not implemented
* `%W` - not implemented
* `%+` - not implemented
* `%%` - not implemented (use `%`)

### Sample usage:

```
// Returns "15-09-2016 16:20"
strftime('%d-%m-%Y %H:%M');

// You can optionally pass it a Date object
// Returns "01-01-2016 21:30"
strftime('%d-%m-%Y %H:%M', new Date('Jan 1, 2016 9:30 PM'));
```

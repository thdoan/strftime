# strftime()
A JavaScript port of [`strftime()`](http://man7.org/linux/man-pages/man3/strftime.3.html), a function to format the date and time.

### Supported conversion specifications:

| Sequence  | Description |
|-----------|-------------|
| `%a` | Abbreviated name of the day of the week. |
| `%A` | Full name of the day of the week. |
| `%b` | Abbreviated month name. |
| `%B` | Full month name. |
| `%c` | Preferred date and time (UTC) representation for the current locale. |
| `%C` | Century number (year/100) as a 2-digit integer. |
| `%d` | Day of the month as a decimal number (range 01 to 31). |
| `%e` | Day of the month as a decimal number (range 1 to 31). |
| `%F` | ISO 8601 date format (equivalent to `%Y-%m-%d`). |
| `%G` | ISO 8601 week-based year with century as a decimal number. The 4-digit year corresponds to the ISO week number (see `%V`). This has the same format and value as `%Y`, except that if the ISO week number belongs to the previous or next year, that year is used instead. |
| `%g` | Like `%G`, but without century, that is, with a 2-digit year (00-99). |
| `%H` | Hour as a decimal number using a 24-hour clock (range 00 to 23). See also `%k`. |
| `%I` | Hour as a decimal number using a 12-hour clock (range 01 to 12). See also `%l`. |
| `%j` | Day of the year as a decimal number (range 001 to 366). |
| `%k` | Hour as a decimal number using a 24-hour clock (range 0 to 23). See also `%H`. |
| `%l` | Hour as a decimal number using a 12-hour clock (range 1 to 12). See also `%I`. |
| `%m` | Month as a decimal number (range 01 to 12). |
| `%n` | Month as a decimal number (range 1 to 12). |
| `%M` | Minute as a decimal number (range 00 to 59). |
| `%p` | Either "AM" or "PM" according to the given time value. Noon is treated as "PM" and midnight as "AM". |
| `%P` | Like `%p` but in lowercase ("am" or "pm"). |
| `%s` | Number of seconds since the Epoch, 1970-01-01 00:00:00 +0000 (UTC). |
| `%S` | Second as a decimal number (range 00 to 59). |
| `%u` | Day of the week as a decimal (range 1 to 7), Monday being 1. See also `%w`. |
| `%V` | ISO 8601 week number of the current year as a decimal number (range 01 to 53), where week 1 is the first week that has at least 4 days in the new year (that is, the first Thursday). |
| `%w` | Day of the week as a decimal (range 0 to 6), Sunday being 0. See also `%u`. |
| `%x` | Preferred date representation for the current locale without the time. |
| `%X` | Preferred time representation for the current locale without the date. |
| `%y` | Year as a decimal number without a century (range 00 to 99). |
| `%Y` | Year as a decimal number including the century. |
| `%z` | The `+hhmm` or `-hhmm` numeric timezone (that is, the hour and minute offset from UTC). |
| `%Z` | Timezone name or abbreviation. |

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

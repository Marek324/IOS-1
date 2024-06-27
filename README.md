# Crypto exchange log filter

Posixly correct bash script that takes in log(s) and user's name and prints filtered logs for the user. 

## Logs

Logs are in CSV format
```
NAME;DATETIME;CURRENCY;AMOUNT
```

## Usage
```
./xtf [-h|--help] [FILTER] [COMMAND] USER LOG [LOG2 [...]]
```
COMMAND may be one of:
- list - a listing of records for a given user.
- list-currency - a listing of a sorted list of occurring currencies.
- status - a listing of the actual account status grouped and sorted by currency.
- profit - a statement of the customer's account status with notional profit included.

FILTER can be a combination of the following:
- -a DATETIME - after: only records AFTER this date and time (without it) are considered. DATETIME is of format YYYY-MM-DD HH:MM:SS.
- -b DATETIME - before: only records BEFORE this date and time (without it) are considered.
- -c CURRENCY - only records corresponding to the given currency are considered.

-h and --help print a help message with a short description of each command and switch.

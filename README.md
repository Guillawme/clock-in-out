# A simple clocking tool

This `clock` script records the current date and time and stores them in a log
file, along with an `in` or `out` description. I use it to record the time I
spend at work because I am on flexible hours and not paid by the hour, so I need
to know my hours to keep a proper balance (sometimes I work too much, sometimes
not enough, sometimes with a good balance; either way, I want to know).

## Installation

1. Put the `clock` script in a directory listed in your `PATH`.
2. Make the `clock` script executable (`chmod +x /path/to/clock`).
3. Edit the `LOGFILE=` line at the top of the script to point to the file in
   which you want to save the data.

## Usage

The script only takes one of two options: `in` or `out`, so you may run it with
`clock in` to record the start time and `clock out` to record the end time of a
workday (or task, or whatever it is you want to log).

## Analysis

The `LOGFILE` populated by the script is a CSV file with the following format:

```
date,year,month,day,weekday,weeknumber,time,event
2023-01-03,2023,January,03,Tuesday,01,10:14:02,in
2023-01-03,2023,January,03,Tuesday,01,16:52:49,out
```

You can then analyze and/or plot this data with your method of choice. This
repository contains the [Pluto](https://plutojl.org/) notebook I use, but you
could use whatever works best for you (a spreadsheet, R, Python, etc.) and what
you can do is of course not limited to the simple examples in this notebook.


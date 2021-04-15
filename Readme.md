##Config.json

`active` and `inactive` are mutually exclusive. `inactive` supports the same options as `active` but negates them.

`active` is a list, which can contain the following data types:

* `bool`: matches always. True will execute the trigger, false will stop the trigger
* `int`: selects a day of a week. Starting with Monday as 0 and ending with Sunday as 6
* `dict`: finer selection of specific date or time. You have to select at least one of these. These we be combined by an AND expression:
    * `weekday`: `int` selects a day of a week. Starting with Monday as 0 and ending with Sunday as 6
    * `time_start`: `list` first value is the start hour, second the minute
    * `time_end`: `list` first value is the end hour, second the minute
    * `week`: `int` select the week of the month. 1 = the first week, 2 = the second week, -1 = the last week, -2 = the second last week, ...

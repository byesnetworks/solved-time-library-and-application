Download Link: https://assignmentchef.com/product/solved-time-library-and-application
<br>
5/5 - (1 vote)

Write an application to produce the following output in C




Note: User is presented with a menu of three items: change time A, change time B, or exit. Once the user inputs time A (or B) the program shows the time A plus duration B, and the time difference between A and B.

=======================

Time A: 23:15 or 11:15 PM [1395]Time B: 01:00 or 01:00 AM [60]added: 00:15 duration: 22:15

[A] [B] [X] aA: 4:30Time A: 04:30 or 04:30 AM [270]Time B: 01:00 or 01:00 AM [60]added: 05:30 duration: 03:30

[A] [B] [X] bB: 17:30Time A: 04:30 or 04:30 AM [270]Time B: 17:30 or 05:30 PM [1050]added: 22:00 duration: -13:00

[A] [B] [X] x

=======================

Press &lt;RETURN to close this window…Note: Time arithmetics are done by converting each time pair (hr, min) to minutes since midnight, arithmetics are done on the minutes units and then converted back to time.

It will be better if you follow the functions below.

bool time_is_valid(int hr, int min); //true if hr:min is validbool time_is_valid(int hr, int min, char ap); //true if hr:min [ap]m is valid

void time_input(int&amp; hr, int&amp; min, char &amp;ap, string prompt = “:”); //input hr:min apvoid time_input(int&amp; hr, int&amp; min, string prompt=”:”); //input hr:min

void time_output(int hr, int min); //output hr:minvoid time_output(int hr, int min, char ap); //output hr:min ap

void time_convert(int hr_24, int&amp; hr_12, char &amp;ap); //hr:min – hr:min apvoid time_convert(int hr_12, char ap, int&amp; hr_24); //hr:min ap – hr:min

void time_add(int&amp; hr_start, int&amp; min_start, int hr_duration, int min_duration); //hr:min += hr:minvoid time_add(int hr_start, int min_start, int hr_duration, int min_duration, int&amp; end_hr, int&amp; end_min); //end_time = t1+t2

void time_subtract(int &amp;hr_end, int &amp;min_end, int hr_start, int min_start); //hr:min -= hr:minvoid time_subtract(int hr_end, int min_end, int hr_start, int min_start, int&amp; hr_duration, int&amp; min_duration); //hr:min -= hr:min
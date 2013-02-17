erlstring
=========

erlstring is an alternate to Erlang strings..

Features
========
Currently supports only concatenation of strings. 

Erlang strings are list. So concatenation operation is O(n). 
For large number of concatenations it can be very slow O(n*m) 
where n is the string length and m is the number of contenations.
erlstring is based on tree implementation. Thus its complexity is O(n).
Space can be little high but of O(n).

Note: Please correct me if I have said something wrong.

Example
=======
E1 = erlstring:new().
E2 = erlstring:concat(E1, "hi").	% lot many concatenations
S = erlstring:to_string(E2).		% get back concatenated string if required.

TODO
====
substr
len
str
spec and eunit

Test
====
Sample comparison timing data (using timer:tc) with 10240 concatenation 
1>erlstring_test:test(10240).
erlstring time: 16363 
string time: 1478919
ok


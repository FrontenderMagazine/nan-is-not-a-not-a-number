In software development it’s crucial to be precise when you’re using terms:
proper use of terms is essential for people to communicate efficiently. It’s 
highly important to be on the same wavelength.

One of the terms that is frequently misused is the `NaN`.

It has its roots in the IEEE754 standard, which defines it as a special value (
actually, as we’ll see later – a set of values), that represents a result of an 
arbitrary evaluation that cannot or should not be represented as a particular 
number, or simply is not known. Eg:`arcsine(2)` or `0/0`. This also leads us to
another discovery:`NaN` value actually is of a numeric type! But just a special
number that is treated and represented in its own very special way.

So, again, `NaN` as per the IEEE754 standard is not any arbitrary value of a
non-numeric type, but actually is a number! What it means is that one better not
say a string`"foo"` is a `NaN`, since it’s not.

It gets even more interesting if you check how the `NaN` values are represented
. For double precision (64 bit long) floating point numbers (that are used to 
represent a`Number` data type in javascript and few other languages) a special
range with the exponent equal to`0x7FF` is reserved to represent `NaN` values.
Which means that the other 53 bits of a number can be of any value (unless when 
a fraction equals to`0x0` that is reserved for `+Infinity` and `-Infinity`). So
having a double precision floating point number we can construct a`NaN` value
in`9007199254740990` (2 power 53 minus 2) distinct ways. That’s a lot isn’t
it.

To summarise: if you use `NaN` as a substitution for simply anything that is
not a number (a string, a null value, an object, etc) – please stop. If you don’
t – please share the knowledge and help other people be as precise as you.

Useful links:
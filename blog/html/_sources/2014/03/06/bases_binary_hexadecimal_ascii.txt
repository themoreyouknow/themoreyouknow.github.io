Bases, binary, hexadecimal, ascii
=================================

You may have heard that computers use binary, but why is that? Simply because in
electronic, if you want to keep it simple, components have two possible state:
on or off -> 0 or 1. The hardware is easier to design this way.

Bases
-----

When we normally count, in what we call `decimal
<http://en.wikipedia.org/wiki/Decimal>`_, is actually base-10, which means we
use 10 numbers: from 0 to 9

So if you count::

  0, 1, 2, 3, 4, 5, 6, 7, 8, 9...

And then what? 10 of course, but why is that: you reached the end of your
*base*, thus increment the second digit, and loop back to beginning for the
first digit, you could use this notation to see it better::

  08, 09, 10...

Another way to think of it is to use the calculation behind it, we use base 10,
so each digit is number * base ^ rank, with the rank starting out at 0. Lets use
42::

  (4 * 10¹) + (2 * 10⁰)
  (4 * 10) + (2 * 1)

Any bases are possible, as long as you define what needs to be used to represent
it, of course, some are more common than others, especially in computer science.

Binary
------

Given the previously explained on/off paradigm in electronic, it was chosen to
use `binary <http://en.wikipedia.org/wiki/Binary_number>`_, or base-2 in
computers. We so have 2 numbers to count: 0 and 1

If you apply the same as earlier::

  0, 1

And that's it, you reached the end of the base, so increment next digit::

  0, 1, 10, 11, 100, 101, 110, 111...
  0  1   2   3    4    5    6    7...

And as of 42::

  101010

  0 * 2⁰ + 1 * 2¹ + 0 * 2² + 1 * 2³ + 0 * 2⁴ + 1 * 2⁵
  0      + 2      + 0      + 8      + 0      + 32
  = 42

In computer, the number of `bits <http://en.wikipedia.org/wiki/Bit>`_ you may
have heard about, is the number of binary digit used to represent the number.
The `byte <http://en.wikipedia.org/wiki/Byte>`_ which is used to compute volume
of data, is 8 bits, which allows for values up to 255.

To identify we sometimes use prefix **0b**::

  0b101010

Hexadecimal
-----------

To avoid the need to read binary all the time, it is actually easier given the
data is grouped in bytes in computers to represent values in `hexadecimal
<http://en.wikipedia.org/wiki/Hexadecimal>`_ rather than binary or decimal.
Hexadecimal is base-16, we use numbers from 0 to 9, and letters form A to F, and
the prefix **0x**::

  0x1, 0x2, 0x3, 0x4, 0x5, 0x6, 0x7, 0x8, 0x9, 0xa, 0xb, 0xc, 0xd, 0xe, 0xf

Applying the same technique as before::

  0x0e, 0x0f, 0x10, 0x11

And for 42::

  0x2a

  a * 16⁰ + 2 * 16¹
  10 * 1 + 2 * 16
  = 42

Ascii
-----

Aka `American Standard Code for Information Interchange
<http://en.wikipedia.org/wiki/Ascii>`_, is the basic representation of
characters used in computers, using numbers up to 128 to encode characters
representation. It was later extended in various different versions to suite
more languages.

For example **A** is 0x41 (65), and following capital letters are following in
order, and **a** is 0x61 (97) and so on.

In binary, this means::

  0x41 -> 0b01000001
  0x61 -> 0b01100001

You may notice that the left hand bit is 0 in both case, as said, ascii is
limited to 128, thus never using the bit of rank 7. The various extended
versions make use of it, but have to be a different version for different
languages as this still is quite limited.

Later, the `unicode <http://en.wikipedia.org/wiki/Unicode>`_, and `UTF
<http://en.wikipedia.org/wiki/Utf>`_ variations where created, but this is a
vast topic, which I will not talk about in here.


.. author:: default
.. categories:: none
.. tags:: bases, maths, counting, binary, hexadecimal, ascii
.. comments::

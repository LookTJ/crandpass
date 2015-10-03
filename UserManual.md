# Introduction #
crandpass is a simple password creator that for UNIX that is built to be both flexible and minimal.  Usage is very simple and straight forward through the command line:
` crandpass [option] `

The default setting of crandpass with no options given is as follows:
` crandpass -c 1 -l 32 -sr -A3 -N1 -S0 `

This will create one password of 32 characters using /dev/random as the generator.  The password will include letters and numbers, but it will not include symbols.  I chose this as the default because it will reliable produce a good password that is difficult to crack and compatible with most sensible systems.

# Options #
Below are all of the options crandpass provides listed in logical order.

## Program Information ##
<pre> -h   print help message<br>
-v   print version number</pre>


## Character Options ##
All character output options are uppercase.  This decision was made to make it easier to distinguish between output and generator options.
<pre> -A   alphabetic characters options:<br>
0  x  exlude       exclude letters<br>
1  l  lower        use only lowercase<br>
2  u  upper        use only uppercase<br>
3  m  mix          use mixed case (default)<br>
-H   create hexadecimal passwords<br>
1  l  lower        use lowercase<br>
2  u  upper        use uppercase<br>
-N   numerical character options:<br>
0  x  exclude      exclude numbers<br>
1  i  include      include numbers (default)<br>
-S   symbol character options:<br>
0  x  exclude      exclude symbols (default)<br>
1  i  include      include symbols</pre>

## Generation Options ##
All generation options are lowercase.
<pre> -c   number of passwords to create (default: 1)<br>
-l   length of passwords (default: 32)<br>
-s   source of the passwords<br>
r  random          use /dev/random *(default)<br>
u  urandom         use /dev/urandom</pre>
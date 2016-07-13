# Args-Kata

## Problem Statement
Most of us have had to parse command-line arguments from
time to time. If we don’t have a convenient utility, then
we simply walk the array of strings that is passed into the
main function. There are several good utilities available from
various sources, but they probably don’t do exactly what we
want. So let’s write another one!

The arguments passed to the program consist of flags and
values. Flags should be one character, preceded by a minus
sign. Each flag should have zero, or one value associated with
it.

You should write a parser for this kind of arguments. This
parser takes a schema detailing what arguments the program
expects. The schema specifies the number and types of flags
and values the program expects.

Once the schema has been specified, the program should pass
the actual argument list to the args parser. It will verify that
the arguments match the schema. The program can then ask
the args parser for each of the values, using the names of
the flags. The values are returned with the correct types, as
specified in the schema.

For example if the program is to be called with these arguments:
-l -p 8080 -d /usr/logs

this indicates a schema with 3 flags: l, p, d. The “l” (logging)
flag has no values associated with it, it is a boolean flag, Tr ue
if present, False if not. the “p” (port) flag has an integer value,
and the “d” (directory) flag has a string value.

If a flag mentioned in the schema is missing in the arguments,
a suitable default value should be returned. For example
“False” for a boolean, 0 for a number, and “” for a string.
If the arguments given do not match the schema, it is important
that a good error message is given, explaining exactly
what is wrong.

If you are feeling ambitious, extend your code to support lists
Eg.
-g this,is,a,list -d 1,2,-3,5

So the “g” flag indicates a list of strings, [“this”, “is”, “a”, “list”]
and the “d” flag indicates a list of integers, [1, 2, -3, 5].

Make sure your code is extensible, in that it is straightforward
and obvious how to add new types of values.
 
What the schema should look like and how to specify
it is deliberately left vague in the Kata description. An
important part of the Kata is to design a concise yet
readable format for it.
 
Make sure you have a test with a negative integer
(confusing - sign) 
 
The order of the arguments need not match the order
given in the schema.
 
Don’t forget to check suitable default values are correctly
assigned if flags given in the schema are missing
in the args given.


## Requiements 

1. This is utility for command line argument parsing
4. A command can have single or multiple flags set
5. A flag should be a character and must be preceded with minus such as (-l)
6. Each flag can have one or more associated value
7. Each argument passed has certain schema of passing it
8. verify argument match schema

## Requirement analysis 

1. It should accept command line arguments
2. It should check if any flag is set or not
3. It should find how many flags are set
4. It should check if each flag is in the form (-)character
5. It should check if each flag has right schema
6. It should check if associated value is in right format


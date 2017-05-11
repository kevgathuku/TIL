The `+` operator cannot work on different types e.g. integers and strings

i.e  `1 + "1"` raises `(ArithmeticError)  bad argument in arithmetic expression`

The `/` operator always returns a float.

```elixir
4 / 2 == 2.0
```

For integer division use the `div` function
```elixir
div(4, 2) == 2
```

Representing binary, octal, and hexadecimal numbers

```elixir
0b1010 == 10
0o777 == 511
0x1A == 26
```

The booleans `true` and `false` are atoms

```elixir
is_atom(false) == true
is_boolean(:false) == true
```

Creating anonymous functions:

```elixir
sum = fn a, b -> a + b end
```

Invoking anonymous functions requires a dot between the function name and parentheses

```elixir
sum.(1, 2)
```

Single-quoted and double-quoted representations are not equivalent

```elixir
'hello' == "hello" # false
```

To get more info on a value in iEX, use the `i/1` function to see more info about it:

```
iex(40)> i 'hello'
Term
  'hello'
Data type
  List
Description
  This is a list of integers that is printed as a sequence of characters
  delimited by single quotes because all the integers in it represent valid
  ASCII characters. Conventionally, such lists of integers are referred to as
  "charlists" (more precisely, a charlist is a list of Unicode codepoints,
  and ASCII is a subset of Unicode).
Raw representation
  [104, 101, 108, 108, 111]
Reference modules
  List
Implemented protocols
  IEx.Info, Collectable, Enumerable, Inspect, List.Chars, String.Chars
```

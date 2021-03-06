!!!Note
    While this section is up-to-date and complete, it has to be reformated
    to be easier on the eyes. All UPPERCASE statement names and code should
    be changed to lowercase.

## `IN _ SOLVE _`

The `IN - SOLVE` statement will solve a simple arithmetic expression and place the result in a NUMBER variable. Only `+`, `-`, `/`, `*` operators, NUMBER values, and TEXT values can be used in a MATH-EXPRESSION. Other LDPL arithmetic functions, like `floor` and `modulo`, are not supported by this statement and should be used as standalone statements. TEXT values will be implicitly converted to NUMBERs using the same algorithm as the one used in `store _ in _`.

Spaces **must** be used to separate numbers, variables and operators.

As in actual arithmetic, `*` and `/` have higher precedence than `+` and `-` , while parens `()` can be used to group expressions.

**Syntax:**

```coffeescript
IN <NUMBER-VAR> SOLVE <MATH-EXPRESSION>
```

**Example:**

```coffeescript
IN myNumVariable SOLVE 1 + 1
```

Will set the value of `myNumVariable` to `2`.

**Area of Circle:**

```coffeescript
DATA:
Radius is NUMBER
Area is NUMBER

PROCEDURE:
DISPLAY "Enter Radius: " 
ACCEPT Radius

IN Area SOLVE 3.14159 * (Radius * Radius)
DISPLAY "Area is: " Area CRLF
```

Outputs:

```text
Enter Radius: 0.5
Area is: 0.7853975
```

## `FLOOR`

The `FLOOR` statement rounds down the value of NUMBER-VAR to the nearest lower integer.

**Syntax:**

```coffeescript
FLOOR <NUMBER-VAR>
```

## `MODULO _ BY _ IN _`

The `MODULO` statement calculates the remainder of the modulo operation between two NUMBER values and stores the result in a NUMBER variable.

**Syntax:**

```coffeescript
 MODULO <NUMBER-VAR or NUMBER> BY <NUMBER-VAR or NUMBER> IN <NUMBER-VAR>
```


## `GET RANDOM IN _`

The `GET RANDOM` statement stores a random value between 0 \(inclusive\) and 1 \(noninclusive\) in a NUMBER variable.

**Syntax:**

```coffeescript
GET RANDOM IN <NUMBER-VAR>
```

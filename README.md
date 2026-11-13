# Function Tool
Function tool is an open source librairy to transform a String into a function, and compute it

## How to use it
### Available Operators
`+`, `-`, `*`, `/`, `^` *(exponentiation)*

### Variables & Constants
* `x` or `-x` *(evaluates over a range)*
* `pi`
* `e`

### Priority of Operations
* **No operator precedence:** Operators are evaluated strictly from left to right.
* Use **parentheses** to define execution order.
* **Example:** Do not write `3 + 2 * x`. Write `3 + (2 * x)` instead.

### Built-in Functions

| Category | Functions |
| :--- | :--- |
| **Trigonometric** | `sin`, `cos`, `tan`, `atan` |
| **Hyperbolic** | `sinh`, `cosh`, `tanh`, `atanh` |
| **Exponential & Log** | `exp`, `sqrt`, `log`, `ln` |

---

### Function Syntax

* **`FUNCTION_NAME`**  
  Computes the given function using the variable `x` *(e.g., `sin` evaluates `sin(x)`)*.

* **`FUNCTION_NAME(VALUE)`**  
  Computes the function for a specific `VALUE`. `VALUE` can be a raw number, an expression, or another nested function *(e.g., `sin(cos(x))` or `sqrt(16)`)*.

### Example of Usage

```java
public class Main {
    public static void main(String[] args) {
        Function function = new Function("sin(x + 1)");
        try {
            System.out.println(function.getFunction() + ", for x = 1, gives : " + function.solveFor(1));
        } catch (Exception e) {
            throw new RuntimeException(e);
        }
    }
}
```

> ⚠️ **Current Limitation (v1.0):**  
>Always leave a space between arguments and operators. Numbers are parsed as signed doubles. 

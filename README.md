# matrices.luau
> [!IMPORTANT]
> This library has not been released.

## Constructs

* #### `matrices.create(rows: number, cols: number, value: number?)`  
  Creates a matrice with rows and cols and fills them with an optional `value` parameter.

&nbsp;
* #### `matrices.random(rows: number, cols: number, min: number?, max: number?)`  
  Creates a matrice with rows and cols and fills them with random values between min and max (default is 0 - 1)

&nbsp;
* #### `matrices.identity(n: number)`  
  Creates a identity matrice with rows and cols equal to n

&nbsp;
* #### `matrices.array(table: {{number}})`  
  Converts a table into a matrice, provided that the table takes this format
  
  ```luau
  const t = {
    {1, 0, 0},
    {0, 1, 0},
    {0, 0, 1}
  }
  ```

&nbsp;
## Operations

* #### `matrices.transpose(b: matrix)`  
  Returns a new transposed matrice of b

&nbsp;
* #### `matrices.dot(b1: matrix, b2: matrix)`  
  Returns the dot product of 2 matrices as one
  
> [!CAUTION]
> For element-wise multiplication with a matrice or scalar use the `*` operator.

&nbsp;
* #### `matrices.map(b1: matrix, fn: (number) -> number)`  
  Some description here

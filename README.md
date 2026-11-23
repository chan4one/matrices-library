### matrices.luau
> [!IMPORTANT]
> This library has not been released.


## API Functions





### create
```luau
matrices.create(rows: number, cols: number, value: number)
```
Creates a matrix with the specified `rows` and `cols`, filled with an optional `value` (defaults to `0`).  
```luau
print(matrices.create(2, 4, 1.0))
```
```
1.00   1.00   1.00   1.00
1.00   1.00   1.00   1.00
```

> [!TIP]
> Omit `value` when you don't need a specific fill. Without it, the matrice is created noticeably faster, since there's no need to write a value into every cell. The cells default to `0`.

---


### random
Creates a matrice with the specified `rows` and `cols`, filled with random numbers between `min` and `max`.

```luau
matrices.random(rows: number, cols: number, min: number, max: number)
```
---


### identity
Creates an identity matrix of size `n × n`: a square matrix with `1` on the main diagonal and `0` everywhere else.
```luau
matrices.identity(n: number)
```

---


### array
Creates a matrix from a two-dimensional array of numbers (t), where each inner array becomes a `row` of the matrix.
```luau
matrices.array(t: {{number}})
```

---

### clone
Creates a new matrix that is a copy of the given `matrice`. Changes to the clone do not affect the original.
```luau
matrices.clone(matrice: matrice)
```

---

### dot
Computes the matrix product (dot product) of `a` and `b`. The number of columns in `a` must equal the number of rows in `b`. The result has the same number of rows as a and the same number of columns as `b`
```luau
matrices.dot(a: matrice, b: matrice)
```

---

### map
Creates a new matrix by calling `fn` on every element of the given matrix and storing the returned value in the same position. The original matrix is not modified.
```luau
matrices.map(matrice: matrice, fn: (value: number, row: number, col: number) => number)
```

---

### transpose
Returns a new matrix where rows and columns are swapped, so the element at position [i][j] moves to [j][i]. A matrix with r rows and c columns becomes one with c rows and r columns.
```luau
matrices.transpose(matrice: matrice)
```

---

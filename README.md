# Explicit Formula for Inverse and Determinant in Geometric Algebras over Odd-dimensional Vector Spaces

Implementation of explicit formulas for **inverse** and **determinant** in 7D geometric algebras `Cl(p,q)` (p+q=7), as presented in the paper.

**Paper**: Explicit Formula for Inverse and Determinant in Geometric Algebras over Odd-dimensional Vector Spaces

**Authors**: Kamron Abdulkhaev, Dmitry Shirokov  

**Abstract**: In this paper, we present  explicit formulas for the inverse and determinant in geometric (Clifford) algebras over vector spaces of dimension $n=7$. The derivation of these formulas is made possible by generalizing the concept of conjugation to basis conjugation operations. We further develop a general method for constructing such formulas over odd-dimensional spaces from the known even-dimensional case. To validate computational utility of the results, we provide a numerical implementation of the formulas. The code implementation is available at the repository \url{github.com/kamranuz/clifford_7d}. These formulas extend previous results for lower dimensions and offer new insights for applications in mathematical physics and computational geometry.

## Implemented Functions

### Our Explicit Formulas (Projection Method)

| Function | Description | Stability |
|----------|-------------|-----------|
| `cl7_determinant(A)` | Computes determinant of multivector A in 7D Cl(p,q) | ✅ Stable |
| `cl7_inverse(A)` | Computes inverse of multivector A in 7D Cl(p,q) | ✅ Stable |
| `cl7_determinant_opt(A)` | Optimized version | ✅ Stable |
| `cl7_inverse_opt(A)` | Optimized version | ✅ Stable |

### Our Explicit Formulas (Signed Array Method)

| Function | Description | Stability |
|----------|-------------|-----------|
| `cl7_ar_determinant(A)` | Determinant using element‑wise sign array for conjugations | ✅ Stable |
| `cl7_ar_inverse(A)` | Inverse using element‑wise sign array for conjugations | ✅ Stable |
| `cl7_ar_determinant_opt(A)` | Optimized signed array version | ✅ Stable |
| `cl7_ar_inverse_opt(A)` | Optimized signed array version | ✅ Stable |

> The projection method subtracts specific components from the original multivector; the signed array method applies conjugations by multiplying basis elements with a predefined sign array. Performance gain depends on the conjugation operation.

### Isomorphism‑Based Formulas (Hitzer & Sangwine)

| Function | Description | Stability |
|----------|-------------|-----------|
| `cl7_determinant_hitzersangwine(A)` | Determinant via embedding in reduced algebra | ⚠️ Unstable* |
| `cl7_inverse_hitzersangwine(A)` | Inverse via embedding in reduced algebra | ❌ Unstable |

\* Clipped close to zero non‑scalar artifacts.

### Recursive Method (Faddeev–LeVerrier)

| Function | Description | Stability |
|----------|-------------|-----------|
| `cl7_determinant_fvs(A)` | Determinant via Faddeev–LeVerrier recursion | ✅ Stable |
| `cl7_inverse_fvs(A)` | Inverse via Faddeev–LeVerrier recursion | ✅ Stable |

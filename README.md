# FastMatrixMultiplication-
Fast Matrix Multiplication Algorithm, Implemented in Javascript[a11 a12 / a21 a22] * [b11 b12 / b21 b22] = [c11 c12 / c21 c22]  
  
// Algorithm //  
// 8 Multiplications //  
// 4 Additions //  
  
c11 = a11 * b11 + a12 * b21  
c12 = a11 * b12 + a12 * b22  
c21 = a21 * b11 + a22 * b21  
c22 = a21 * b12 + a22 * b22  
  
// Algorithm 1 //  
  
a = a11 * b11  
b = a12 * b21  
c = a11 * b12  
d = a12 * b22  
e = a21 * b11  
f = a22 * b21  
g = a21 * b12  
h = a22 * b22  
  
c11 = a + b  
c12 = c + d  
c21 = e + f  
c22 = g + h  
  
// Algorithm 2 //  
  
[a1 a2 / a3 a4] * [b1 b2 / b3 b4] = [c1 c2 / c3 c4]  
  
a = a1 * b1  
b = a2 * b3  
c = a1 * b2  
d = a2 * b4  
e = a3 * b1  
f = a4 * b3  
g = a3 * b2  
h = a4 * b4  
  
c1 = a + b  
c2 = c + d  
c3 = e + f  
c4 = g + h  
  
// Algorithm 3 //  
  
[a1 a2 / a3 a4] * [b1 b2 / b3 b4] = [c1 c2 / c3 c4]  
  
m1 = (a2 - a4)(b1 + b4)  
m2 = (a3 + a4)(b1)  
m3 = (b2 - b4)(a1)  
m4 = (b3 - b1)(a4)  
m5 = (a1 + a2)(b4)  
m6 = (a3 - a1)(b1 + b2)  
m7 = (a2 - a4)(b3 + b4)  
  
c1 = m1 + m4 - m5 + m7  
c2 = m3 + m5  
c3 = m2 + m4  
c4 = m1 - m2 + m3 + m6  
  
// Algorithm 4 //  
  
[a1 a2 / a3 a4] * [b1 b2 / b3 b4] = [c1 c2 / c3 c4]  
  
m1 = (b1 + b2)(a1)  
m2 = (b2 + b4)(a2)  
m3 = (b1 + b3)(a3)  
m4 = (b2 + b4)(a4)  

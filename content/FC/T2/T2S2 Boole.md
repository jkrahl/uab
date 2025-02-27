---
title: Álgebra de Boole
---
Un álgebra de Boole es un conjunto finito de elementos con las operaciones suma y producto, y que cumple con estos 5 postulados:
1. Las operaciones + y * son internas, sus resultados siempre están en mismo conjunto que se use. $\forall a,b \in B,\; a+b \in B \text{ y } a \cdot b \in B$
2. Existe un elemento neutro para cada operación, 0 para la suma, y 1 para el producto. $\forall a\in B,\; a+0=a,\; a \cdot 1 = a$
3. Existe un elemento inverso para cualquier elemento del conjunto. $\forall a \in B,\; \exists \;\bar a \in B \;| \; a + \bar a= 1 , \;a \cdot \bar a = 0$
4. Las operaciones son conmutativas. $a+b=b+a , \; a\cdot b=b \cdot a$
5. Las operaciones son distributivas. $a\cdot (b+c) = a\cdot b + a \cdot c , \; a + b\cdot c = (a+b)\cdot (a+c)$

El álgebra de conmutación es un álgebra de Boole con el conjunto {0,1}. En sistemas digitales se utiliza el nombre Álgebra de Boole para el álgebra de conmutación, aunque sean cosas distintas.

Definimos las operaciones suma y producto de esta forma:

| a   | b   | a+b | a.b |
| --- | --- | --- | --- |
| 0   | 0   | 0   | 0   |
| 0   | 1   | 1   | 0   |
| 1   | 0   | 1   | 0   |
| 1   | 1   | 1   | 1   |
La suma coincide con la tabla de la puerta OR, y el producto coincide con la puerta AND.  
Esto nos sirve para implementar cualquier circuito digital con el menor número posible de puertas.
### Propiedades útiles
1. Elemento inverso: $\bar 0 = 1 ,\; \bar 1 = 0$
2. Idempotencia: $a+a=a,\; a\cdot a=a$
3. Involución: $\bar {\bar a} = a$
4. Asociatividad: $a+(b+c)=(a+b)+c,\; a\cdot (b\cdot c)=(a\cdot b)\cdot c$
5. Absorción: $a+a\cdot b=a,\; a\cdot (a+b)=a$
6. Leyes de Morgan: $\overline{(a+b)}=\bar a\cdot \bar b,\; \overline{a \cdot b}=\bar a+\bar b$
7. Ley de Morgan generalizada: $\overline{(a_1+a_2\dots +a_n)}=\bar a_1\cdot \bar a_2 \dots \bar a_n,\; \overline{a_1\cdot a_2\dots a_n}=\bar a_1+ \bar a_2+ \dots + \bar a_n$
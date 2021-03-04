# Hoja 1

### Ejercicio 1

Comenzamos probando que si $x\in \mathfrak N_A$, entonces $1+x\in \mathcal U(A)$. Existe $n>0$ tal que $x^n=0$, y entonces observamos que $(1+x)x^{n-1}=x^{n-1}$. Así:
$$
(1+x^{n-1})(1+x) = 1+2x^{n-1} =1+2x^{n-1}(1+x)\\
(1+x^{n-1})(1+x)-2x^{n-1}(1+x)=1\\
(1+x^{n-1}-2x^{n-1})(1+x)=1\\
(1-x^{n-1})(1+x)=1
$$
Por otra parte, si $u\in \mathcal U(A)$, existe $v\in A$ tal que $uv=1$. Además, por ser $\mathfrak N_A$ un ideal, $vx \in \mathfrak N_A$ con mismo índice de nilpotencia, y podemos aplicar lo anterior 
$$
(1-(vx)^{n-1})(1+vx)=1
$$
Ahora podemos escribir $1+vx = v(u+x)$ y por tanto la anterior identidad queda escrita como
$$
[v(1-(vx)^{n-1})](u+x)=1
$$


### Ejercicio 2

a) En general, si $\phi:A\to B$ es un isomorfismo, y $\mathfrak a \sub A$ un ideal, entonces $\phi(\mathfrak a)$ es un ideal de $B$:

- Para todo $\phi(x),\phi(y)\in \phi(\mathfrak a)$ tenemos que $\phi(x)+\phi(y) = \phi(\underset{\in \mathfrak a}{x+y}) \in \phi(\mathfrak a)$.
- Para todo $\phi(x)\in \phi(\mathfrak a),z\in B$ existe $w\in A$ tal que $\phi(w) = z$, y entonces $z\phi(x) = \phi(\underset{\in \mathfrak a}{wx}) \in \phi(\mathfrak a)$.

Y todo ideal del producto $\mathfrak b \sub A_1\times A_2$, es un producto de ideales $\mathfrak b_1 \times \mathfrak b_2$. Efectivamente, sea 
$$
\mathfrak b_1 = \{x\in A_1: \; \exist y\in A_2//(x,y)\in \mathfrak b\}
$$
y veamos que es un ideal:

- Para todo $x, x' \in \mathfrak b_1$ existen $y,y' \in A_2$ tales que $(x,y),(x',y')\in \mathfrak b$ y por ser un ideal tenemos $\mathfrak b \ni (x,y)+(x',y') = (x+x',y+y')$ y por tanto $x+x' \in \mathfrak b_1$.
- Para todo $x\in \mathfrak b_1$ y todo $z\in A_1$ existe $y\in A_2$ tal que $(x,y)\in \mathfrak b$, y además $(z,0)\in A_1\times A_2$, y por ser un ideal se tiene $\mathfrak b\ni (x,y)(z,0) = (xz,0)$ con lo que $xz \in \mathfrak b_1$.

Con esto queda probado que todo $\mathfrak a \sub A$ es isomorfo a un producto de ideales.

b) En general, si $\phi:A\to B$ es un isomorfismo, y $\mathfrak p \sub A$ un ideal primo, entonces $\phi(\mathfrak p)$ es un ideal primo de $B$:

- Sean $x',y' \in B$ tales que $x' = \phi(x), y' = \phi(y)\in \phi(\mathfrak p)$, entonces $\phi(\mathfrak p) \ni x'y' = \phi(x)\phi(y) = \phi(xy) $ por tanto $xy\in \mathfrak p$ y como es un ideal primo, $x \in \mathfrak p$ o $y\in \mathfrak p$ $\iff$ $x' \in \phi(\mathfrak p)$ o $y' \in \phi(\mathfrak p)$. 

Si $\mathfrak p \sub A_1\times A_2$ es un ideal primo, entonces sabemos de a)  que $\mathfrak p = \mathfrak a_1\times \mathfrak a_2$ producto de ideales. Veamos que o bien $\mathfrak p = \mathfrak p_1\times A_2$ con $\mathfrak p_1$ primo, o bien $\mathfrak p = A_1\times \mathfrak p_2$ con $\mathfrak p_2$ primo. Supongamos $\mathfrak p_1 \neq A_1$:

- Para todo $x,y \in A_1$ tales que $xy\in \mathfrak p_1$  existe $z\in A_2$ tal que $(xy,z)\in \mathfrak p$. Entonces se tiene $\mathfrak p \ni (xy,z) = (x,z)(y,1)$ y por lo tanto $(x,z)\in \mathfrak p$ o bien $(y,1)\in \mathfrak p$ lo que implica que $x\in \mathfrak p_1$ o $y \in \mathfrak p_1$. Por tanto $\mathfrak p_1$ es un ideal primo.
- Más aún, dado $x\in \mathfrak p_1$, obviamente se cumple $1\cdot x \in \mathfrak p_1$. Siguiendo lo de arriba, $(1,z)(x,1) \in \mathfrak p$, y como $\mathfrak p_1\neq A_1$ no puede ser que $(1,z)\in \mathfrak p$, luego necesariamente $(x,1)\in \mathfrak p$ y por lo tanto $1\in\mathfrak p_2$ y así $\mathfrak p_2 = A_2$.



### Ejercicio 3

Utilizando la caracterización que conocemos del nilradical de un anillo aplicado al cociente, y teniendo en cuenta que la biyección del teorema de la correspondencia conserva la primalidad, tenemos que:
$$
\begin{multline}
x\in \sqrt {\mathfrak a} \iff x+\mathfrak a \in \mathfrak N_{A/\mathfrak a} = \bigcap_{\bar {\mathfrak p}\in \operatorname{Spec}(A/\mathfrak a)}\bar {\mathfrak p} \iff \forall \bar {\mathfrak p} \in \operatorname{Spec}(A/\mathfrak a), \, x+\mathfrak a \in  \bar {\mathfrak p}  \iff \forall \mathfrak p\in\operatorname{Spec}(A),\;  x\in \mathfrak p
\end{multline}
$$


### Ejercicio 4

$\Leftarrow)$ Sabemos que $\mathfrak N_A$ es un ideal, así que $\sum_{j=1}^n a_j X^j\in \mathfrak N_A$, y como $a_0\in \mathcal U(A)$, en virtud del ejercicio 1 se tiene que $\sum_{j=1}^n a_j X^j+a_0 = f \in \mathcal U(A)$.

$\Rightarrow)$ Como $f$ es una unidad, existe $g =\sum_{j=1}^m b_j X^j \in A[X]$ tal que $fg = 1$. En primer lugar, esto implica que $a_0b_0 = 1$ luego $a_0\in \mathcal U(A)$.

FALTA LA SEGUNDA PARTE

### Ejercicio 5

$A$ es un dominio de ideales principales.

$a)\iff b)$ La implicación $\Leftarrow$ se tiene siempre. Sea $\mathfrak a = aA$ un ideal primo, y supongamos que existe $\mathfrak b = bA$ tal que $\mathfrak a\subsetneq \mathfrak b$. Existe $x\in A$ tal que $bx = a\in \mathfrak a$ primo, luego $b\in \mathfrak a$ o $x\in \mathfrak a$. No puede ser que $b\in \mathfrak a$ porque en tal caso existiría un $z\in A$ tal que $az = b$ y entonces para todo $t\in  A$ se tendría que $bt = a(zt) \in aA = \mathfrak a$ y por tanto $\mathfrak b \subseteq \mathfrak a$, en contra de nuestra hipótesis. Por tanto $x \in \mathfrak a$, y existe $w\in A$ tal que $x = aw$, entonces $a(bw) = a$ y por tanto $1=bw   \in \mathfrak b$, con lo que $\mathfrak b = A$. Así $\mathfrak a$ es maximal.

$b)\iff c)$ Sea $\mathfrak a =aA$ un ideal, y supongamos que $a$ se puede expresar como $a=uv$ con $u,v\not\in \mathcal U(A)$. Entonces $\mathfrak a\subseteq uA$ y, además, $uA\neq A$ porque $u$ no es unidad. Veamos que $uA \not \subseteq \mathfrak a$, o equivalentemente, $u\not \in \mathfrak a$. Si $u\in \mathfrak a$ existe un $w$ tal que $u = aw =u(vw)$ y por tanto $u(1-vw)=0$ luego $1=vw$, ya que $u\neq 0$ pues si no $\mathfrak a = 0$ que no es maximal. Esto va en contra de la suposición de que $v \not \in \mathcal U(A)$. Así que $\mathfrak a \subsetneq uA\subsetneq A$ y por tanto no es un ideal maximal.

Supongamos ahora que $a$ es irreducible, y existe $\mathfrak b=bA \supset \mathfrak a$. Existe $w \in A$ tal que $a = bw$, y como $a$ es irreducible entonces $b\in \mathcal U(A)$ o $w\in \mathcal U(A)$, en cualquier caso $\mathfrak b = A$, y por tanto $\mathfrak a$ es maximal.


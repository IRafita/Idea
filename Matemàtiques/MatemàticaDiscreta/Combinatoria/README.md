Definició
=========
La combinatoria és una branca de les [matemàtiques](../../README.md) que pertany a
l'àrea de les [matemàtiques discretes](../README.md).<br>

Estudia
-------
L'enumeració, construcció i existència de propietats de configuracions que satisfan certes condicions.<br>
L'ordenació o agrupacions d'un determinat nombre d'elements.

Preferència
-----------
Contar el nombre de vegades que uns objectes poden organitzar-se d'una determinada forma.

Toca
====
- Regla del producte, un arbre, on cada nivell fan les mateixes preguntes.
- Principi multiplicatiu, equivalent a la Regla del producte

Regla del producte
------------------
Una elecció tens alternatives, al fer qualsevol d'elles, tindràs unes altres possiblitats.<br>
Subconjunt → [Permutació sense repetició](permutacio/README.md)

Permutació
----------
Té una relació molt directa amb els factorials. 
> P\_n = n!
# Història
El càlcul de permutacions `n!` és creu que va apareixer per primer cop a la India.
Se sap que 300 aC treballaven amb permutacions.

Subbranques
===========
- Permutacions (cartes, vas treient poc a poc).
- Coeficient binomial (cartes sense ordre).
- Amb o sense ordre.
- Combinació extremal (wiki castellà)


Exemples
========
- Papiro Rhind.
- Braille, Regla del producte
- Amadeus Mozart, "juego de dados musical", Regla del producte

Dominos
-------
**Regla del producte**.<br>
*Fer que el segon pesa de domino pugui ser llençada amb relació al primer*.<br>
Tenim 28 formes diferents vàlides. 7 de que siguin dobles i 21 que no.<br>
Dobles → 6 maneres | 7 x 6 = 42<br>
Diferents → 12 maneres | 21 x 12 = 252<br>
Total = 42 + 252 = 294 casos diferents vàlids.

Combinació
----------
Sabem de **permutacions** `P_n` i sobretot de la **Regla del producte**.<br>
`A_i`, `B_j` on i canvia en 5 i j en 4. I els `A_i` estàn tots junts i el B respectivament també.<br>
Total = `P_5 · P_4 = 2880` maneres diferents.

Combinació
----------
Hi ha 7 persones, on dues volen anar juntes.<br>
`2 x P_6 = 1440`

Permutacions
------------
Quantes permutacions és poden fer amb la paraula `BONDAD`?
6!/2!

Taula rodona
------------
# !!!!!!!!!!!!!!!!!!!
Voldria fer un programa per calcular aquest cas.
# !!!!!!!!!!!!!!!!!!!
Tenim que per simetria, 2 casos són iguals.<br>
Tenim que per rotació, 4 casos són iguals.<br>
Tenim que les permutacions totals són 4!.<br>
Llavors la solució és 4!/(2 x 4) = 3<br>
## Posibilitat
n!/(n x 2)

Ordre importa
-------------
Si tenim 5 elements, però no podem fer que un sigui abans que l'altre:
`5!/2 = 60`

Parelles
--------
Donat 2n objectes, quantes n parelles diferents podem fer?<br>
sol? (2n!)/(2^n n!)
### Generalitzat
`m n` objectes, conjunts de m objectes?<br>
[(m n)!]/[(m!)^n n!]

Variacions (sense repetició) (Combinatoria)
===========================================
Subconjunt de les Combinacions.<br>
D'ell, les permutacions són un subconjunt.<br>
Les variacions no tenen repetició.<br>
`V_n,r ⇒ V_n,n-1 = P_n`<br>
`V_n^r = n!/r!`<br>
On `r<n`

Futbolistes
-----------
20 fubolistes, 10 en joc. Combinacions?<br>
`20!/10! = V_20,10`.

Variacions amb repetició
========================
Subconjunt de la regla del producte.<br>
`VR_n,r = n^r = VR_n^r`

Combinatoria (sense repetició)
==============================
<!-- pagina 44 1_Combinatoria -->
`C_n^r = (n over r) = V_n^r / P_r`

Triangle de Pascal (o Tartaglia)
================================
<!-- Pàgina 53 1_Combinatoria -->
Propietats (són intuitius pel triangle de Tartaglia)
- (n over r) = (n over n-r)
> demostració<br>
> (n over r) = n!/(r!(n-r)!)<br>
> (n over n-r)=n!/(n-r)!(n-(n-r)!) = n!/(n-r)!r!
- (n-1 over r-1) + (n-1 over r) = (n over r)
> demostració<br>
> (n-1 over r-1) + (n-1 over r) =<br>
> (n-1)!/((r-1)!(n-r)!) + (n-1)!/((r!(n-r-1)!) = [r(n-1)!+(n-r)(n-1)!]/[r!(n-r)!] = n!/r!(n-r)! = (n over r)
- `sum_r=0^n C_r^n = 2^n`

Conjunt potència
================
<!-- Pàgina 62 -->
```
S = {a,b,c}
P(S) = {{}, {a}, {b}, {c}, {a,b}, {a,c}, {b,c}, {a,b,c}}
2^3 combinacions.
```

Tartaglia
=========
<!-- Pàgina 66 -->
Un altre punt de vista. Si podem anar a dreta o esquerra. Quantes maneres diferents podem arribar a un punt indicat?<br>
Doncs si, la resposta és el mateix valor de Tartaglia.

La conjectura de Singmaster
===========================
Nombre de vegades que apareix un nombre.<br>
És creu que no és infinit. Però no s'ha pogut demostrar!!

Principi del palomar o els caixons de Dirichlet
===============================================
Si tenim kn +1 palomes i n nius. Hi haurà almenys un niu amb k+1 palomes.

Teoria de grafos i nombres de Ramsey
====================================
Nombre mínim per assegurar que hi ha 3 persones que es coneien o no?<br>
Són 6. Fer dibuix per entendre-ho.

Permutacions amb repetició
==========================
`PR_n ^{n_1, ..., n_r} = n!/ (n_1! ... n_r!)`

Binomi de Newton
================
Moltes respostes si fas la pregunta correcta o el punt de vista adecuat.<br>
3a²b veiessim ←←→? a = ← i b = →<br>

Generalitació del binomi de Newton
----------------------------------
<!-- Pàgina 99 -->
Voldria fer una representació d'aquest com un triangle de tartaglia.<br>
Són permutacions amb repetició...

Combinacions amb repetició
--------------------------
<!-- Pàgina 112 -->
`CR_r ^n = ( n+r-1 over r ) = C_r ^n-1+r`

Dubtes
======
- Quina relació té la teoria de grafs amb combinatoria?
```
codi git o comandes hihihi
```
Ara per poder-ho fer pel mitg `lola mola`.

- Demostracions
- Axiomes
Tot això crec que és molt intuitiu, però realment, com se fa?

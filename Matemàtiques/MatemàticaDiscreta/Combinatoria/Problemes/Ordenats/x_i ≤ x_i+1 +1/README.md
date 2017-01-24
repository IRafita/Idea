# Plantejament del problema
`Жⁿ_r = χⁿ_r(∀ i | x_i ≤ x_i+1 +1) = {(x_i) | [(i ∈ |N) ∧ (i < n)] ∧ [(x_i ∈ |N) ∧ (x_i < r)] ∧ (∀ i | x_i ≤ x_i+1 +1)}`.<br>
Acabem de definir `Жⁿ_r` per a no tenir que escriure tota l'estona `χⁿ_r(x_i ≤ x_i+1 +1)`

## Estudi
Aquí plantejo el plantejament que he fet.
I l'evolució fins el resultat, o fins on arribi.
Potser no sóc capaç de trobar la solució correcta.<br>
`Āⁿ_r = χⁿ_r(∃ i | x_i > x_i+1 +1) = {(x_i) | [(i ∈ |N) ∧ (i < n)] ∧ [(x_i ∈ |N) ∧ (x_i < r)] ∧ (∃ i | x_i > x_i+1 +1)}

### Estudiarem el cas `Жⁿ₃`
``
	Ж⁰₃ = ø			#Ж⁰₃ = 0	#Ā⁰₃ = 0
	Ж¹₃ = {(0), (1), (2)}	#Ж¹₃ = 3	#Ā¹₃ = 0
	Ж²₃ =	{
			(0,0), (0, 1), (0,2),
			(1,0), (1, 1), (1,2),
			       (2, 1), (2,2),
		}		#Ж²₃ = 8	#Ā²₃ = 1
``
Ara el `Ж³₃` és més dificil de calcular.<br>

#### Estudi complert `Ж²₃`
És un valor correcte.
``
	#Ж²₃ = 3² - 3⁰(20) = 8
	#Ж²₃ = 3² - (2-1)*3⁰ = 8
``

#### Estudi complert `Ж³₃`
No està comprovat el resultat.!!!!!!!
``
	#Ж³₃ = 3³ - 3¹(20x) - 3¹(x20) = 21
	#Ж³₃ = 3³ - (3-1)*3¹ = 21
``

#### Estudi complert `Ж⁴₃`
No està comprovat el resultat.!!!!!!!
``
	#Ж⁴₃ = 3⁴ - 3²(20xx) - 3²(x20x) - 3²(x20x) + 3⁰(2020) = 55
	#Ж⁴₃ = 3⁴ - (4-1)*3² + (4-3)*3⁰ = 55
``

#### Estudi complert `Ж⁵₃`
No està comprovat el resultat.!!!!!!!
``
	#Ж⁵₃ = 3⁵ - 3³(20xxx) - 3³(x20xx) - 3³(xx20x) - 3³(xxx20) + 3¹(2020x) + 3¹(20x20) + 3¹(x2020) = 188
	#Ж⁵₃ = 3⁵ - (5-1)*3² + (5-2)*3¹ = 188
``

#### Resolució
Per motius de complexitat d'escriure en format d'ordinadors vs a mà.
Només aniré escrivint les conclusions.
Ja que sinó és massa complicat per a mi.<br>
``
	#Ж⁰₃ =   0	#Ā⁰₃ =  0	3⁰ .... = 1 ≠ 0
	#Ж¹₃ =   3	#Ā¹₃ =  0	3¹				=    3
	#Ж²₃ =   8	#Ā²₃ =  1	3² - (2-1)*3⁰			=    8
	#Ж³₃ =  21	#Ā³₃ =  6	3³ - (3-1)*3¹			=   21
	#Ж⁴₃ =  55	#Ā⁴₃ = 26	3⁴ - (4-1)*3² + (4-3)*3⁰	=   55
	#Ж⁵₃ = 188	#Ā⁵₃ = 55	3⁵ - (5-1)*3³ + (5-2)*3¹	=  188
``

#### Equacions plantejades
No validat!!!!!!!!!
``
	#Жⁿ₃ = 3³ - (n-1)*3ⁿ⁻² + (n-2)*3ⁿ⁻⁴ - ...
		± {
			⌈n/2⌉* 3¹	si n imparell
			1		si n parell
``

No validat!!!!!!!!!
``
	#Ā⁰₃ = 0
	#Ā¹₃ = 0
	#Āⁿ⁺²₃ = -(n+1)*3ⁿ - #Āⁿ₃
``

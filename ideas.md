# Idée générale 
(En vrac)
[X] = Oui,  [ ] = Non

- [ ] Les paramètres des fonctions sont immuables
- [ ] Si une valeur est en dehors d'une assignation à une variable, alors elle est considérée comme un 'return'
```
func test (Int x) -> Void | Err {
    if a == 0 {
        return Err
    }
}

let a = 10
test(a) // Rien ne se passe car Void

let b = 0
let e = test(b) // Renvoie une Err mais qui est attrapée par 'e'

if ?e {...}

test(b) // la valeur n'est pas capturée dans une assignation -> equivaut a un 'return value'
```
Idem avec autre chose que des Err : 
```
func test (Int a) -> Int | Err {
    a // Equivaut à return a
}
...
```
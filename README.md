# 🧮 Python Calculator Checkpoint

## 🎯 Objectif
Ce projet a pour but de créer une calculatrice en Python en utilisant la programmation orientée objet.  
La calculatrice doit gérer les opérations de base (+, -, *, /) et permettre d’ajouter des opérations avancées (exponentiation, racine carrée, logarithme).

---

## ⚙️ Fonctionnalités
- **Opérations de base :**
  - Addition (+)
  - Soustraction (-)
  - Multiplication (*)
  - Division (/), avec gestion de l’erreur de division par zéro
- **Opérations avancées :**
  - Exponentiation (^)
  - Racine carrée (sqrt)
  - Logarithme naturel (log)
- **Gestion des erreurs :**
  - Vérification des types (les entrées doivent être des nombres)
  - Vérification des symboles (opération non supportée → erreur)

---

## 🏗️ Structure du code
- Classe `Calculator` :
  - `operations` : dictionnaire qui associe chaque symbole à sa fonction
  - `__init__()` : initialise les opérations de base
  - `add_operation(symbol, func)` : ajoute une nouvelle opération
  - `calculate(x, symbol, y=None)` : exécute l’opération choisie avec gestion des erreurs
- Fonctions avancées définies séparément :
  - `exponentiation(x, y)`
  - `square_root(x)`
  - `logarithm(x)`

---

## ▶️ Exemple d’utilisation
```python
calc = Calculator()

print(calc.calculate(5, '+', 3))      
print(calc.calculate(10, '/', 2))     

calc.add_operation('^', exponentiation)
print(calc.calculate(2, '^', 3))      

calc.add_operation('sqrt', square_root)
print(calc.calculate(16, 'sqrt'))     

calc.add_operation('log', logarithm)
print(calc.calculate(10, 'log'))      

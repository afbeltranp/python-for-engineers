# Quiz 2: 

## Pregunta 1. Depuración de CalculadoraPromedio

### Enunciado del Problema

- Se te proporciona un **script inicial con errores** para **CalculadoraPromedio**.
- El objetivo del programa es calcular el **promedio ponderado de un estudiante para exactamente tres cursos**, basándose en **calificaciones numéricas** (de `0.0` a `5.0`).
- Actualmente, el script tiene varios errores que impiden que se ejecute correctamente.
- Tu trabajo es **identificar el código corregido** que funcione según lo previsto y coincida con el formato de entrada/salida requerido.

---

### Requisitos del Programa

1. **Mensaje de Inicio**: Cuando el programa comience, debe mostrar exactamente:
```plaintext
   Bienvenido a CalculadoraPromedio!
```

2. **Mensajes de Entrada**: Para cada uno de los 3 cursos, el programa debe solicitar:

   1. **Calificación** del curso
   2. **Créditos** del curso

   - Usa este formato exacto:

        ```plaintext
            Ingrese la calificación del curso 1:
            5.0
            Ingrese los créditos del curso 1:
            3
            Ingrese la calificación del curso 2:
            4.5
            Ingrese los créditos del curso 2:
            4
            Ingrese la calificación del curso 3:
            3.7
            Ingrese los créditos del curso 3:
            5
        ```
   - Las **calificaciones** son números de punto flotante (ej: `5.0`, `4.5`, `3.7`)
   - Los **créditos** son números enteros (ej: `3`, `4`, `5`)

3. **Cálculo del Promedio Ponderado**: Usa la fórmula:
```
   Promedio = (suma de calificaciones × créditos para todos los cursos) / (total de créditos)
```

4. **Salida Final**: Después de todas las entradas, el programa debe imprimir:
```plaintext
   Su promedio ponderado es: <promedio>
```
   donde `<promedio>` está redondeado a **dos decimales**.

---

### Consejo de Python: `round()`

La función incorporada `round()` puede usarse para formatear el resultado del promedio.

- **Sintaxis:** `round(numero, digitos)`
- **Ejemplo:** `round(4.6789, 2)` → `4.68`

---

### Ejemplo de Ejecución

**Entrada:**
```plaintext
4.5
3
5.0
4
3.8
3
```

**Salida:**
```plaintext
Bienvenido a CalculadoraPromedio!
Ingrese la calificación del curso 1:
4.5               
Ingrese los créditos del curso 1:
3             
Ingrese la calificación del curso 2:
5.0 
Ingrese los créditos del curso 2:
4  
Ingrese la calificación del curso 3:
3.8 
Ingrese los créditos del curso 3:
3   
Su promedio ponderado es: 4.49
```

---

## Código Original (CON ERRORES)
```python
print("Bienvenido a CalculadoraPromedio!")

# curso 1
cal1 = input("Ingrese la calificación del curso 1:\n")
cred1 = input("Ingrese los créditos del curso 1:\n")

# curso 2
cal2 = input("Ingrese la calificación del curso 2:\n")
cred2 = input("Ingrese los créditos del curso 2:\n")

# curso 3
cal3 = input("Ingrese la calificación del curso 3:\n")
cred3 = input("Ingrese los créditos del curso 3:\n")

total_ponderado = (cal1 * cred1) + (cal2 * cred2) + (cal3 * cred3)
total_creditos = cred1 + cred2 + cred3

promedio = total_ponderado / total_creditos
promedio_redondeado = round(promedio, 2)

print("Su promedio ponderado es: " + promedio_redondeado)
```

---

## Pregunta: ¿Cuál es la versión CORRECTA del código?

### Opción A
```python
print("Bienvenido a CalculadoraPromedio!")

# curso 1
cal1 = float(input("Ingrese la calificación del curso 1:\n"))
cred1 = int(input("Ingrese los créditos del curso 1:\n"))

# curso 2
cal2 = float(input("Ingrese la calificación del curso 2:\n"))
cred2 = int(input("Ingrese los créditos del curso 2:\n"))

# curso 3
cal3 = float(input("Ingrese la calificación del curso 3:\n"))
cred3 = int(input("Ingrese los créditos del curso 3:\n"))

total_ponderado = (cal1 * cred1) + (cal2 * cred2) + (cal3 * cred3)
total_creditos = cred1 + cred2 + cred3

promedio = total_ponderado / total_creditos
promedio_redondeado = round(promedio, 2)

print("Su promedio ponderado es: " + str(promedio_redondeado))
```

---

### Opción B
```python
print("Bienvenido a CalculadoraPromedio!")

# curso 1
cal1 = int(input("Ingrese la calificación del curso 1:\n"))
cred1 = int(input("Ingrese los créditos del curso 1:\n"))

# curso 2
cal2 = int(input("Ingrese la calificación del curso 2:\n"))
cred2 = int(input("Ingrese los créditos del curso 2:\n"))

# curso 3
cal3 = int(input("Ingrese la calificación del curso 3:\n"))
cred3 = int(input("Ingrese los créditos del curso 3:\n"))

total_ponderado = (cal1 * cred1) + (cal2 * cred2) + (cal3 * cred3)
total_creditos = cred1 + cred2 + cred3

promedio = total_ponderado / total_creditos
promedio_redondeado = round(promedio, 2)

print("Su promedio ponderado es: " + str(promedio_redondeado))
```

---

### Opción C
```python
print("Bienvenido a CalculadoraPromedio!")

# curso 1
cal1 = float(input("Ingrese la calificación del curso 1:\n"))
cred1 = float(input("Ingrese los créditos del curso 1:\n"))

# curso 2
cal2 = float(input("Ingrese la calificación del curso 2:\n"))
cred2 = float(input("Ingrese los créditos del curso 2:\n"))

# curso 3
cal3 = float(input("Ingrese la calificación del curso 3:\n"))
cred3 = float(input("Ingrese los créditos del curso 3:\n"))

total_ponderado = (cal1 * cred1) + (cal2 * cred2) + (cal3 * cred3)
total_creditos = cred1 + cred2 + cred3

promedio = total_ponderado / total_creditos
promedio_redondeado = round(promedio, 2)

print("Su promedio ponderado es:", promedio_redondeado)
```

---

### Opción D
```python
print("Bienvenido a CalculadoraPromedio!")

# curso 1
cal1 = float(input("Ingrese la calificación del curso 1:\n"))
cred1 = int(input("Ingrese los créditos del curso 1:\n"))

# curso 2
cal2 = float(input("Ingrese la calificación del curso 2:\n"))
cred2 = int(input("Ingrese los créditos del curso 2:\n"))

# curso 3
cal3 = float(input("Ingrese la calificación del curso 3:\n"))
cred3 = int(input("Ingrese los créditos del curso 3:\n"))

total_ponderado = (cal1 * cred1) + (cal2 * cred2) + (cal3 * cred3)
total_creditos = cred1 + cred2 + cred3

promedio = total_ponderado / total_creditos
promedio_redondeado = round(promedio, 2)

print("Su promedio ponderado es:", promedio_redondeado)
```

---


## Pregunta2. Programa FoodieBot

### Enunciado del Problema

Escribe un programa de Python llamado "FoodieBot" que interactúe con el usuario para tomar su orden de comida.

---

### Requisitos del Programa

1. **Saludo inicial**: Saludar al usuario con un mensaje alegre y preguntar su nombre en el siguiente formato:
```plaintext
   Welcome to FoodieBot! What's your name?
```

2. **Preguntar comida favorita**: Preguntar al usuario su comida favorita con la pregunta:
```plaintext
   Nice to meet you, <name>! What's your favorite food?
```

3. **Mensaje de despedida**: Agradecer al usuario y resumir su orden imprimiendo un mensaje final en el siguiente formato:
```plaintext
   Thank you, <name>! I'll get some <favorite food> ready for you right away!
```

---

### Ejemplo 1 de Ejecución

**Entrada:**
```plaintext
Alice
Pizza
```

**Salida:**
```plaintext
Welcome to FoodieBot! What's your name?
Alice
Nice to meet you, Alice! What's your favorite food?
Pizza
Thank you, Alice! I'll get some Pizza ready for you right away!
```

---

### Ejemplo 2 de Ejecución

**Entrada:**
```plaintext
evelyn
tacos
```

**Salida:**
```plaintext
Welcome to FoodieBot! What's your name?
evelyn
Nice to meet you, evelyn! What's your favorite food?
tacos
Thank you, evelyn! I'll get some tacos ready for you right away!
```

---

### Consejo Importante

- Asegúrate de usar el carácter `\n` apropiadamente en las funciones `input()` para que la entrada del usuario aparezca en una nueva línea.
- El mensaje debe estar dentro de la función `input()`, no en un `print()` separado.

---

## Pregunta: ¿Cuál es el código CORRECTO para FoodieBot?

### Opción A
```python
name = input("Welcome to FoodieBot! What's your name?\n")
food = input("Nice to meet you, " + name + "! What's your favorite food?\n")
print("Thank you, " + name + "! I'll get some " + food + " ready for you right away!")
```

---

### Opción B
```python
print("Welcome to FoodieBot! What's your name?")
name = input()

print("Nice to meet you, " + name + "! What's your favorite food?")
food = input()

print("Thank you, " + name + "! I'll get some " + food + " ready for you right away!")
```

---

### Opción C
```python
name = input("Welcome to FoodieBot! What's your name?")
food = input("Nice to meet you, " + name + "! What's your favorite food?")
print("Thank you, " + name + "! I'll get some " + food + " ready for you right away!")
```

---

### Opción D
```python
print("Welcome to FoodieBot! What's your name?\n")
name = input()

print("Nice to meet you, " + name + "! What's your favorite food?\n")
food = input()

print("Thank you, " + name + "! I'll get some " + food + " ready for you right away!")
```

---

# Factorial
El factorial de un número entero positivo nn (denotado como n!n!) es el producto de todos los números enteros positivos desde 1 hasta nn.
![Sin título](https://github.com/user-attachments/assets/12de2e7a-cb4b-4c64-af44-3781f1853797)

El cálculo del factorial de un número es un clásico ejemplo de uso de la recursión. En Kotlin, puedes implementar una función recursiva para calcular el factorial de un número de la siguiente manera:
~~~
fun factorial(n: Int): Int {
    // Caso base: el factorial de 0 o 1 es 1
    if (n == 0 || n == 1) {
        return 1
    }
    // Caso recursivo: n! = n * (n-1)!
    return n * factorial(n - 1)
}

fun main() {
    val number = 5
    println("El factorial de $number es ${factorial(number)}")
}
~~~
### Explicación:
 - Función factorial(n: Int): Int:
        Esta función toma un número entero n y devuelve el factorial de n.
        El caso base es cuando n es 0 o 1, en cuyo caso el factorial es 1.
        Para otros valores de n, la función se llama a sí misma con el valor n - 1 y multiplica el resultado por n.

 - Función main():
        Define un número para calcular su factorial y llama a la función factorial.
        Imprime el resultado.

Puedes probar este código con diferentes valores de number para calcular el factorial de otros números. Ten en cuenta que, para números grandes, la recursión puede llevar a un desbordamiento de pila, por lo que en casos de números extremadamente grandes es mejor usar una solución iterativa o técnicas más avanzadas.

### Explicacion por Linea
Código del factorial

kotlin
~~~
fun factorial(n: Int): Int {
    // Caso base: el factorial de 0 o 1 es 1
    if (n == 0 || n == 1) {
        return 1
    }
    // Caso recursivo: n! = n * (n-1)!
    return n * factorial(n - 1)
}
~~~
 
   fun factorial(n: Int): Int {
        Esta línea define una función llamada factorial que toma un número entero (n) y devuelve otro número entero.

    // Caso base: el factorial de 0 o 1 es 1
        Esto es solo un comentario que nos dice que el factorial de 0 o 1 siempre es 1.

    if (n == 0 || n == 1) {
        Aquí se verifica si el número n es 0 o 1.

    return 1
        Si n es 0 o 1, la función devuelve 1. Esto es porque el factorial de 0 o 1 es 1.

    return n * factorial(n - 1)
        Si n no es 0 ni 1, la función se llama a sí misma con el valor n - 1 y multiplica el resultado por n. Esto es lo que hace que la función siga calculando el factorial.

    }
        Termina la definición de la función.

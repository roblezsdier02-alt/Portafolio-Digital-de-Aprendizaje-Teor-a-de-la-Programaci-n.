<div align="center">

<img src="https://github.com/user-attachments/assets/0249b6fe-8642-4ea1-ba56-dd3e713088fc" width="180"/>

# UNIVERSIDAD NACIONAL DE LOJA

### Facultad de la Energía, las Industrias y los Recursos Naturales No Renovables

## Carrera de Computación

### Portafolio Académico - Teoría de Programación

</div>

---

## Información General

| Información | Detalle |
|:------------|:--------|
| **Asignatura** | Teoría de Programación |
| **Ciclo** | Primer Ciclo |
| **Período Académico** | Abril – Agosto 2026 |
| **Docente** | Ing. Lissette Geoconda López Faicán |
| **Estudiante** | Sdier Emanuel Roblez Roblez |

---

# Índice

- [Unidad 3](#unidad-3)
  - [1. Modularidad](#1-modularidad)
  - [2. Arreglos y Estructuras de Datos Estáticas](#2-arreglos-y-estructuras-de-datos-estáticas)
  - [3. Dificultades y Reflexión Crítica](#3-dificultades-y-reflexión-crítica)
- [Conclusiones Generales](#conclusiones-generales)
- [Bibliografía](#bibliografía)
- [Declaración de uso de IA](#declaración-de-uso-de-la-ia-generativa)

---

# Unidad 3

# 1. Modularidad

## Teoría

La programación modular es un paradigma de diseño que consiste en dividir un programa complejo en módulos independientes (funciones, procedimientos o métodos). Esto mejora la organización del código, facilita su mantenimiento y favorece la reutilización.

---

## Ejemplo 1. Paso de parámetros por **Valor**

En el paso por valor se envía una **copia** del dato original. Las modificaciones realizadas dentro de la función no afectan a la variable original.

```c
#include <stdio.h>

void modificarValor(int x) {
    x = 100;
    printf("Dentro de la función (por valor): %d\n", x);
}

int main() {
    int numero = 10;

    printf("Antes de la función: %d\n", numero);

    modificarValor(numero);

    printf("Después de la función: %d\n", numero);

    return 0;
}
```

### Evidencia práctica

<p align="center">
<img src="https://github.com/user-attachments/assets/cc05e8b7-38d4-4fac-8a89-8b59eb8ae5ee" width="500">
</p>

---

## Ejemplo 2. Paso de parámetros por **Referencia**

En el paso por referencia se envía la **dirección de memoria** de la variable. Las modificaciones realizadas dentro de la función afectan directamente a la variable original.

```c
#include <stdio.h>

void modificarReferencia(int *x) {
    *x = 100;
    printf("Dentro de la función (por referencia): %d\n", *x);
}

int main() {

    int numero = 10;

    printf("Antes de la función: %d\n", numero);

    modificarReferencia(&numero);

    printf("Después de la función: %d\n", numero);

    return 0;
}
```

### Evidencia práctica

<p align="center">
<img src="https://github.com/user-attachments/assets/24086650-26b1-4b4c-adde-d4a70afc8427" width="550">
</p>

---

# 2. Arreglos y Estructuras de Datos Estáticas

## Teoría

Los arreglos (*arrays*) son estructuras de datos estáticas que almacenan elementos del mismo tipo en posiciones consecutivas de memoria. Se clasifican según el número de dimensiones.

---

## 2.1 Arreglo Unidimensional (Vector)

Permite almacenar elementos en una estructura lineal utilizando un único índice.

```java
public class VectorEjemplo {

    public static void main(String[] args) {

        int[] calificaciones = {85,90,78,92,88};

        int suma = 0;

        for(int i=0;i<calificaciones.length;i++){

            suma += calificaciones[i];

        }

        System.out.println("Promedio = "+(suma/calificaciones.length));

    }

}
```

---

## 2.2 Arreglo Bidimensional (Matriz)

Organiza la información en filas y columnas, requiriendo dos índices para acceder a cada elemento.

```python
matriz = [
    [1,2,3],
    [4,5,6],
    [7,8,9]
]

print("Diagonal principal:")

for i in range(len(matriz)):
    print(matriz[i][i])
```

---

## 2.3 Arreglo Multidimensional

Representa estructuras con tres o más dimensiones.

```java
public class CuboDatos {

    public static void main(String[] args) {

        int[][][] cubo = new int[2][3][4];

        cubo[0][1][2]=50;

        System.out.println(cubo[0][1][2]);

    }

}
```

### Evidencia práctica

<p align="center">
<img src="https://github.com/user-attachments/assets/93dfe495-63f6-4f9d-947d-e42e38953709" width="900">
</p>

---

# 3. Dificultades y Reflexión Crítica

## Principales dificultades

- Comprender el funcionamiento del paso por referencia mediante punteros.
- Evitar errores de segmentación (*Segmentation Fault*).
- Controlar correctamente los bucles anidados en arreglos multidimensionales.
- Evitar errores de índices fuera del rango permitido.

---

## Reflexión crítica

El aprendizaje de la modularidad y de las estructuras de datos estáticas fortaleció mi capacidad para desarrollar programas más organizados y eficientes. Comprendí que dividir un problema en módulos facilita su mantenimiento y reutilización, mientras que el dominio de los arreglos permite representar y procesar información de manera estructurada. Estos conocimientos constituyen una base fundamental para el estudio de estructuras de datos dinámicas y el desarrollo de software de mayor complejidad.

---

# Conclusiones Generales

1. La programación modular mejora la organización, reutilización y mantenimiento del software.

2. Comprender el paso por valor y por referencia permite un uso más eficiente de la memoria.

3. Los arreglos constituyen una estructura fundamental para almacenar y procesar información en aplicaciones informáticas.

---

# Bibliografía

> **Formato IEEE**

[1] L. Joyanes Aguilar, *Fundamentos de Programación: Algoritmos, Estructura de Datos y Objetos*, 5.ª ed. Madrid, España: McGraw-Hill, 2020.

[2] J. Smith, "Memory Management and Modular Programming in C," *IEEE Transactions on Software Engineering*, vol. 48, no. 5, pp. 120–135, May 2022.

[3] Oracle, *Arrays (The Java™ Tutorials)*, Oracle Documentation, 2023. Disponible en: https://docs.oracle.com/javase/tutorial/java/nutsandbolts/arrays.html

---
##  Declaración de uso de la IA generativa
Declaro que durante la elaboración de este portafolio se empleó Inteligencia Artificial generativa (modelo de lenguaje) como herramienta de apoyo para estructurar el formato Markdown en GitHub, generar plantillas base de código y sugerir organización visual. Todo el código final, las reflexiones críticas, compilaciones y diagramas presentados son de mi total auditoría y comprensión, cumpliendo con los estándares de probidad académica de la Universidad Nacional de Loja.

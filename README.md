<div align="center">

  <img width="180" height="180" alt="UNL Logo" src="https://github.com/user-attachments/assets/0249b6fe-8642-4ea1-ba56-dd3e713088fc" />

  # UNIVERSIDAD NACIONAL DE LOJA
  ### FACULTAD DE LA ENERGÍA, LAS INDUSTRIAS Y LOS RECURSOS NATURALES NO RENOVABLES
  ### CARRERA DE COMPUTACIÓN

  ---

  #  PORTAFOLIO DIGITAL DE APRENDIZAJE

  [![Universidad](https://img.shields.io/badge/UNL-Loja-E30613?style=for-the-badge&logo=university&logoColor=white)](https://unl.edu.ec)
  [![Carrera](https://img.shields.io/badge/Computaci%C3%B3n-2026-007ACC?style=for-the-badge&logo=codefactor&logoColor=white)](https://github.com)
  [![Lenguajes](https://img.shields.io/badge/C%20%7C%20Java%20%7C%20Python-4CAF50?style=for-the-badge)](https://github.com)

  **Asignatura:** Teoría de la Programación  
  **Ciclo:** 1er Ciclo  
  **Período Académico:** Abril - Agosto 2026  
  **Docente:** Ing. Lissette Geoconda López Faicán  
  **Estudiante:** Sdier Emanuel Roblez Roblez  

  ---

</div>

##  Índice de Contenidos
1. [Unidad 1 (Archivo)](#-unidad-1)
2. [Unidad 2 (Archivo)](#-unidad-2)
3. [ Unidad 3: Modularidad y Estructuras de Datos Estáticas](#-unidad-3)
   - [3.1 Modularidad](#1-modularidad)
     - [Ejemplo 1: Paso por Valor](#ejemplo-1-pase-de-par%C3%A1metros-por-valor)
     - [Ejemplo 2: Paso por Referencia](#ejemplo-2-pase-de-par%C3%A1metros-por-referencia)
   - [3.2 Arreglos y Estructuras Estáticas](#2-arreglos)
     - [Arreglos Unidimensionales (Vectores)](#21-arreglo-unidimensional-vectores)
     - [Arreglos Bidimensionales (Matrices)](#22-arreglo-bidimensional-matrices)
     - [Arreglos Multidimensionales](#23-arreglo-multidimensional)
     - [Cadenas de Caracteres (Strings)](#24-cadenas-de-caracteres-strings)
   - [3.3 Dificultades y Reflexión Crítica](#3-dificultades-y-reflexi%C3%B3n-cr%C3%ADtica)
4. [🎯 Conclusiones Generales](#conclusiones-generales)
5. [📚 Bibliografía (Norma IEEE)](#bibliograf%C3%ADa)
6. [🤖 Declaración de Uso de IA Generativa](#declaraci%C3%B3n-de-uso-de-la-ia-generativa)

---

##  Unidad 1
<details>
<summary><b>Haz clic aquí para desplegar la información de la Unidad 1</b></summary>

*Contenido correspondiente al primer bloque del ciclo académico.*
</details>

---

##  Unidad 2
<details>
<summary><b>Haz clic aquí para desplegar la información de la Unidad 2</b></summary>

*Contenido correspondiente al segundo bloque del ciclo académico.*
</details>

---

##  Unidad 3

> [!Nota]
> **Descripción de la Unidad:** En este apartado se consolida el aprendizaje sobre el paradigma de programación modular (descomposición en funciones y procedimientos con manejo de parámetros por valor y referencia) y el uso de estructuras de datos estáticas (vectores, matrices, arreglos multidimensionales y cadenas de caracteres) implementados en **C, Java y Python**.

---

### 1. Modularidad

**Teoría:**  
La programación modular es un paradigma de diseño de software que consiste en dividir un programa complejo en subprogramas más pequeños, independientes y manejables denominados módulos (funciones o procedimientos). Este enfoque promueve la reutilización de código, mejora la legibilidad, facilita la depuración y optimiza el mantenimiento del sistema.

#### Ejemplo 1: Pase de parámetros por VALOR
En el paso por valor, la función recibe únicamente una **copia** del dato original almacenado en una nueva posición de memoria. Por ende, cualquier modificación realizada dentro del cuerpo de la función no afecta a la variable del programa principal.

```c
// Ejemplo en C: Demostración de paso por valor
#include <stdio.h>

void modificarValor(int x) {
    x = 100; // Solo modifica la copia local en el stack de la función
    printf("Dentro de la función (por valor): %d\n", x);
}

int main() {
    int numero = 10;
    printf("Antes de la función: %d\n", numero);
    modificarValor(numero);
    printf("Después de la función: %d\n", numero); // Mantiene su valor original (10)
    return 0;
}

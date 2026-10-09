# CWE-190: Integer Overflow

Práctica de la experiencia educativa **Programación Segura** de la Licenciatura en Ingeniería de Software de la Universidad Veracruzana.

Este programa en C muestra la debilidad [CWE-190 (Integer Overflow or Wraparound)](https://cwe.mitre.org/data/definitions/190.html) con tres ejemplos de desbordamiento de enteros.

## Ejemplos

| Ejemplo | Operación | Resultado |
|---------|-----------|-----------|
| 1 | `int` con su valor máximo (2147483647) + 1 | -2147483648 |
| 1 | `unsigned int` con su valor máximo (4294967295) + 1 | 0 |
| 2 | Asignar -1 a un `unsigned short` | 65535 |
| 3 | `char` = 100 + 27 | 127 |
| 3 | `char` = 100 + 28 | -128 |

## Compilación y ejecución

```bash
gcc programa.c -o programa.out -fno-stack-protector -z execstack
./programa.out
```

Probado en Ubuntu Server 16.04 de 32 bits (i686) con GCC.

## Autor

Angel Gabriel Aguilar Hernandez
Docente: Guillermo Humberto Vera Amaro
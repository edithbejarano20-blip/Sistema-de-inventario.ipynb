# Sistema-de-inventario.ipynb
Sistema de inventario y pedidos de una tienda .
Sistema de inventario y pedidos de una tienda

1. Descripción del sistema

Este proyecto desarrolla un pequeño sistema para administrar los productos y pedidos de una tienda.

El sistema permite registrar, buscar, eliminar y recorrer productos. También permite manejar pedidos en el orden en que llegan, buscar productos mediante un árbol binario de búsqueda y representar relaciones entre productos mediante un grafo.

El proyecto fue desarrollado en Python como actividad final de la asignatura Estructura de Datos.

2. Estructuras utilizadas

Lista enlazada

Se utiliza una lista simplemente enlazada para almacenar los productos.

Permite:

- Insertar productos.
- Buscar productos.
- Eliminar productos.
- Recorrer los productos.

Se eligió una lista simple porque el sistema solamente necesita avanzar desde el primer elemento hasta el último.

Cola

La cola representa los pedidos de los clientes.

Se utiliza el principio FIFO, es decir, el primer pedido que llega es el primero que se atiende.

Se implementaron dos versiones:

- Cola con arreglo.
- Cola con lista enlazada.

Árbol binario de búsqueda

El árbol utiliza el código del producto como clave.

Los códigos menores se almacenan a la izquierda y los mayores a la derecha.

Se implementaron:

- Inserción.
- Búsqueda.
- Recorrido preorden.
- Recorrido inorden.
- Recorrido postorden.
- Cálculo recursivo de la altura.

El recorrido inorden permite obtener los productos ordenados por código.

Grafo

El grafo representa relaciones entre productos que pueden comprarse juntos.

Por ejemplo, el celular se puede relacionar con una funda, unos audífonos y un cargador.

Se utiliza una representación mediante listas de adyacencia.

Las consultas implementadas son:

- Obtener vecinos.
- Calcular el grado de un nodo.
- Verificar si dos productos están conectados directamente.

3. Clases principales

Clase| Responsabilidad
Producto| Almacenar los datos del producto
NodoProducto| Crear nodos de la lista
ListaProductos| Administrar los productos
NodoCola| Crear nodos de la cola
ColaLista| Implementar la cola con lista
ColaArreglo| Implementar la cola con arreglo
NodoArbol| Crear nodos del árbol
ArbolBusqueda| Administrar el árbol binario
Grafo| Administrar las relaciones entre productos

4. Comparación entre las colas

Operación| Arreglo| Lista enlazada
Encolar| O(1) amortizado| O(1)
Desencolar| O(1)| O(1)
Está vacía| O(1)| O(1)
Memoria| O(n)| O(n)

Las dos implementaciones cumplen el mismo contrato, por lo que el programa puede trabajar con cualquiera de ellas.

5. Experimento del árbol

Se utilizaron 15 claves.

Inserción desordenada

50, 20, 80, 10, 30, 70, 100, 5, 15, 25, 40, 60, 75, 90, 120

Altura obtenida: 5 niveles.

Inserción ordenada

10, 20, 30, 40, 50, 60, 70, 80, 90, 100, 110, 120, 130, 140, 150

Altura obtenida: 15 niveles.

Cantidad de datos| Inserción| Altura
15| Desordenada| 5
15| Ordenada| 15

Cuando los datos se insertan ordenados, el árbol puede degenerarse y tomar una forma similar a una lista. Esto aumenta la cantidad de comparaciones necesarias para realizar una búsqueda.

Un árbol AVL evita esta situación mediante rotaciones que mantienen el árbol equilibrado.

6. Rotaciones AVL

Para la demostración manual se utilizaron las claves:

10, 20, 30, 40, 50, 60 y 70.

Al insertar las claves en orden ascendente aparecen desequilibrios de tipo RR.

Estos se corrigen mediante rotaciones hacia la izquierda.

La fotografía del dibujo realizado a mano se encuentra en:

"imagen_avl.jpg"

7. Casos de prueba

Se probaron los siguientes casos:

1. Registro de productos.
2. Búsqueda de un producto existente.
3. Búsqueda de un producto inexistente.
4. Eliminación de un producto.
5. Intento de eliminar un producto inexistente.
6. Atención de pedidos mediante cola.
7. Consulta de productos relacionados.
8. Búsqueda mediante el árbol.
9. Recorrido inorden.
10. Funcionamiento de la cola con arreglo.
11. Funcionamiento de la cola con lista enlazada.

8. Condiciones especiales

El sistema controla:

- Lista vacía.
- Cola vacía.
- Eliminación del único elemento.
- Producto inexistente.
- Clave repetida.
- Búsqueda de una clave inexistente.

9. Limitaciones

El sistema funciona en consola y los datos se almacenan únicamente durante la ejecución del programa.

No utiliza una base de datos ni una interfaz gráfica.

El grafo utiliza relaciones previamente definidas y no calcula automáticamente las relaciones entre productos.

10. Posibles mejoras

Como mejoras futuras se podría:

- Incorporar una base de datos.
- Crear una interfaz gráfica.
- Permitir registrar productos desde el usuario.
- Agregar usuarios y clientes.
- Implementar un árbol AVL.
- Generar reportes de ventas.
- Calcular automáticamente los productos más relacionados.

11. Instrucciones para ejecutar

1. Descargar o clonar el repositorio.
2. Abrir el archivo "sistema_tienda.py".
3. Ejecutarlo utilizando Python 3.
4. Revisar los resultados mostrados en la consola.

link del video 

https://fumcc.sharepoint.com/:v:/s/TAREADEESTRUCTURA/IQCIpaGHIYkiTr4hv6vGP9VBAVdTyxzxHvosFUcXDI4aRg4?e=IMU80V&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D

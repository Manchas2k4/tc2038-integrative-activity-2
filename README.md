![Tec de Monterrey](images/logotecmty.png)
# Actividad 3.5 - Implementación de "Graph coloring"

## <span style="color: rgb(26, 99, 169);">¿Qué tengo que hacer?</span>
En este repositorio encontrarás el archivo "main.cpp". En este archivo deberás desarrollar la implementación del problema presentado en esta actividad.  En la parte superior del archivo coloca, en comentarios, tus datos. Por ejemplo:
```
// =========================================================
// File: main.cpp
// Author: Edward Elric - A00123456
// Date: 01/01/2021
// =========================================================
```
Implementa, <span style="text-decoration-line: underline;">de forma individual</span>, un solución para el conjunto de problemas que se describen a continuación.

## <span style="color: rgb(26, 99, 169);">**Descripción**</span>
La empresa "InternetMáximo" ha empezado operaciones en la ciudad. Actualmente con poco personal y dinero inicial, así que requiere tomar decisiones inteligentes que le permitan entrar pronto en competencia con las empresas ya instaladas.

### <span style="color: rgb(26, 99, 169);">**Problema 1. Cobertura máxima**</span>
Los ingenieros de la compañía han generado un mapa que muestra cada una de las colonias y las distancias máximas existente entre los centros geográficos de las mismas. Con el fin de poder empezar a competir, la empresa planea colocar fibra óptima para conectar todas las colonias. Sin embargo, el costo de interconectar todas las colonias entre sí es elevado, por lo que la empresa necesita determinar la forma de conectar todas las colonias con el menor número de enlaces de fibra óptima posible.

### <span style="color: rgb(26, 99, 169);">**Problema 2. Publicidad y contratación**</span>
La empresa cuenta con poco personal así que la tareas de publicidad y contratación es manejada por un solo grupo de personas. La idea es recorrer cada una de las colonias, una solo vez cada una de ellas, y regresar al punto de inicio. A decir verdad, se desea que sea siempre la menor ruta posible.

### <span style="color: rgb(26, 99, 169);">**Problema 3. Máximo servicio qe se puede ofrecer**</span>
Como se comentó antes, la empresa cuenta con pocos recursos, por lo que los equipos instalados son muy heterogeneos. Por lo mismo, las capacidades máximas (Mbps) en los diferentes enlaces son muy varias. La empresa desea determinar cuál es la transferencia máxima que se puede obtener entre dos colonias determinadas. Para ello ya se cuenta con un registro de las velocidades de transferencia máxima entre cada una de las colonias instaladas.

## <span style="color: rgb(26, 99, 169);">**Entrada**</span>
El programa recibe dos grafos, uno no dirigo (que usarás en los dos primeros problemas) y un grafo no dirigido (que usarás para el tercer problema), en forma de matriz ponderada de adyacencias. La primera línea de entrada contiene un entero, *n* (7 <= *n* <= 15), indicando el número de vértices del grafo y dos enteros , *start* y *end* (0 <= *start*, *end* < n), vértices que se emplearan como inicio y fin para algunos problemas.

A continuación, unas primeras *n*  líneas. La *i*-esima línea contiene *n* números.  El *j*-ésimo valor es la distancia, en kilometros, entre el centro de la colonia *i* con el centro de la colonia *j*. En caso de no existir conexión, este valor será -1.

Las siguientes *n* líneas contienen las capacidad máximas de conexión. La *i*-esima línea contiene *n* números. El *j*-ésimo valor es la capacidad máxima, en Mbps, en el enlace que existe entre colonia *i* con la colonia *j*. En caso de no existir conexión, este valor será -1.

## <span style="color: rgb(26, 99, 169);">**Salida**</span>
En primer lugar, deberá desplegar la lista de arcos seleccionados para lograr la cobertura requerida. Los arcos aparecerán en orden descendente por costo. Cada arco deberá mostrarse como un par "(a, b)" donde a < b.

A continuación, se desplegará el costo y los vértices que integran la ruta requerida en el problema 2. Si el costo de la ruta es negativa, deberá desplegar el mensaje "There is no possible route.".

Por último, se desplegará la velocidad máxima de transferencia que se puede lograr entre los vértices *start* y *end*.

## <span style="color: rgb(26, 99, 169);">**Ejemplo de entrada**</span>
```
4 0 3
0 16 45 32
16 0 18 21
45 18 0 7
32 21 7 0
0 48 12 -1
52 0 42 -1
18 -1 0 56
-1 -1 52 0
```

## <span style="color: rgb(26, 99, 169);">**Ejemplo de salida**</span>
```
-------------------------------------
Problem 1
(2, 3)
(0, 1)
(1, 2)
-------------------------------------
Problem 2
Minimum cost: 9
Path: 0 2 1 3
-------------------------------------
Problem 3
Maximum flow from 0 to 3 is 54
-------------------------------------
```

Para probar tu implementación, compila tu programa con el comando:
```
g++ -std=c++11 main.cpp -o app
```
Posteriormente, ejecuta tu programa. Para realizar las pruebas, puedes usar las siguientes líneas de código.
```
./app > mysolution.txt
diff mysolution.txt solution.txt
```
Si el segundo comando no tiene ninguna salida, los resultados que obtuviste son los esperados.

## <span style="color: rgb(26, 99, 169);">**¿Bajo qué criterios se evalúa mi evidencia?**</span>

- **90%** - Para cada una de las funcionalidades se evaluará:

    - **Excelente (90%)** - pasa correctamente todos los casos de prueba.
    - **Muy Bien (68%)** - pasa correctamente el 75% de los casos de prueba.
    - **Bien (45%)** - pasa correctamente el 50% de los casos de prueba.
    - **Insuficiente (23%)** - pasa correctamente menos del 50% de los casos de prueba.

- **10%** - El código deberá seguir los lineamientos estipulados en el estándar de codificación: <span class="instructure_file_holder link_holder">[liga_estándar_codificación](estandar.pdf)</span>

## <span style="color: rgb(26, 99, 169);">**¿Dónde la entrego?**</span>
Cuando hayas pasado todas las pruebas, recuerda publicar el código en tu repositorio (*git push*).

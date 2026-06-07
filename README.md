Red Social Académica Universitaria
Este proyecto implementa una simulación de red social académica universitaria en C++ y realiza un análisis comparativo de rendimiento (Benchmark) contra Java.

El sistema contrasta el uso de estructuras dinámicas manuales basadas en punteros frente a las colecciones nativas integradas de un framework comercial. 

Estructura del Repositorio
/proyecto-final

├── cpp-system/ -> Código fuente (main.cpp) y métricas de salida cpp_results.csv.

├── java-benchmark/ -> Código en NetBeans (Finalprogra.java) y salida java_results.csv.

├── dataset/ -> Archivo origen estudiantes.csv (10,000 registros).

└── README.md -> Descripción general.

Estructuras de Datos Implementadas
Sistema Principal (C++)
Desarrollado de manera manual mediante punteros, sin utilizar la biblioteca estándar (STL):

Tabla Hash (Separate Chaining): Indexación por ID con resolución de colisiones por encadenamiento.

Árbol AVL: Estructura de búsqueda balanceada para la gestión y ordenamiento del ranking según el skill score.

Grafo No Dirigido: Representa las conexiones entre usuarios mediante listas de adyacencia.

Colas y Pilas Manuales: Estructuras a nivel de nodos que dan soporte a los algoritmos de recorrido BFS y DFS.

Listas Enlazadas: Almacenamiento y gestión de proyectos individuales dentro de cada estudiante.

Módulo de Benchmark (Java)
Uso de colecciones nativas para evaluar la abstracción del framework:

HashMap: Equivalente directo a la Tabla Hash por ID.

TreeMap: Estructura balanceada (Árbol Rojo-Negro) equivalente a la funcionalidad del AVL.

Módulo de Benchmark (Resultados)
Ambos sistemas procesan los 10,000 estudiantes y exportan reportes en formato CSV midiendo los tiempos en milisegundos.

C++: Muestra menores tiempos de ejecución gracias a la compilación nativa a código máquina y la gestión directa de punteros en memoria.

Java: Presenta una alta velocidad de desarrollo, pero añade sobrecarga por la ejecución sobre la Máquina Virtual (JVM) y los ciclos del recolector de basura (Garbage Collector).

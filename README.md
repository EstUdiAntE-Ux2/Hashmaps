Este readme es dedicado a los elementos de los programas añadidos pero primero se mencionaran los archivos que se comparten entre los 2.
diccionario.py: Describe que metodos se deben de implementar en cada clase en la que se implemente.
tabla_hash.py: Aqui se implementa la tabla hash desde 0 con listas enlazadas que contiene nodos, valores y punteros a los siguientes nodos, los metodos mas importantes en esta clase son:
__hash_aux: Calcula un índice seguro aplicando hash(key) % capacidad.
put(key, value): Inserta o actualiza un valor.
get(key): devuelve el valor asociado a la clave
remove(key): Elimina la clave y retorna el valor eliminado.
containskey(key): Retorna True/False según si la clave existe.
resize(): Duplica la capacidad y reubica todas las claves.
los otros 2 archivos en el primer programa de hash son de prueba
ruta.py: modela una ruta en la tabla de ruteo para que la tabla guarde objetos completos
tabla_ruteo.py. Aqui se simula el ruteo y tiene estos metodos:
*agregarRuta(ruta): convierte la ruta en clave "red/mascara", si ya existe una ruta para esa red: solo actualiza si la métrica es menor. Si no existe, la agrega
*buscarRuta(ipDestino): Encuentra la mejor ruta para una IP usando longest prefix match.
*eliminarRuta(redDestino): Quita una ruta de la tabla hash, simulando la caida de un enlace.
En el archivo de simulador_router.py se simula un router procesando paquetes usando TablaRuteo.
El archivo contiene constructores para crear una tabla de ruteo lista para ser usada, metodos para agregar rutas, eliminarlas, procesar paquetes(ip), mostrar tabla con las rutas almacenadas

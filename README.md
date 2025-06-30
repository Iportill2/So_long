# So_long

## 📋 Tabla de Contenidos
- [📝 Descripción](#-descripción)
- [🛠️ Compilación](#️-compilación)
- [📚 Uso](#-uso)
- [✅ Pruebas](#-pruebas)
- [🔍 Características](#-características)
- [🧪 Ejemplos](#-ejemplos)
- [📋 Evaluación](#-evaluación)

## 📝 Descripción

So_long es un proyecto de la escuela 42 cuyo objetivo es crear un pequeño juego en 2D utilizando la biblioteca gráfica MiniLibX. El jugador debe recoger todos los coleccionables y llegar a la salida en un mapa cerrado, evitando errores de validación y cumpliendo con las normas de la escuela.

## 🛠️ Compilación

Para compilar el proyecto, ejecuta:

```bash
make
```

Esto generará el ejecutable `so_long`. Para compilar la versión bonus (si existe):

```bash
make bonus
```

## 📚 Uso

Ejecuta el juego pasando como argumento un mapa válido en formato `.ber`:

```bash
./so_long maps/map.ber
```

El mapa debe contener únicamente los caracteres válidos:
- `1`: Muro
- `0`: Suelo
- `C`: Coleccionable
- `E`: Salida
- `P`: Jugador

## ✅ Pruebas

El proyecto ha sido probado con diferentes mapas, incluyendo:
- Mapas válidos y solucionables
- Mapas con errores de formato (elementos desconocidos, sin paredes, sin coleccionables, etc.)
- Mapas grandes y pequeños
- Mapas con caminos no solucionables

Para probar el juego, puedes usar los mapas de la carpeta `maps/` o crear los tuyos propios.

## 🔍 Características
- Validación estricta del mapa (bordes, elementos, formato)
- Gestión de errores y mensajes claros
- Uso de MiniLibX para gráficos y eventos
- Soporte para movimientos del jugador y conteo de pasos
- Cierre correcto del programa y liberación de memoria
- Versión bonus con animaciones y/o enemigos (si está implementada)

## 🧪 Ejemplo de mapa

```
111111
1P0C01
1000E1
111111
```

## 📋 Evaluación

Este proyecto cumple con los requisitos de la asignatura So_long de 42:
- Implementa un juego jugable en 2D con MiniLibX
- Valida correctamente los mapas y gestiona errores
- No tiene fugas de memoria (puedes comprobarlo con Valgrind)
- Sigue la norma de 42
- Incluye Makefile funcional y limpio

Para comprobar fugas de memoria:
```bash
valgrind --leak-check=full ./so_long maps/map.ber
```

Si tienes dudas o sugerencias, puedes abrir un issue o contactar con el autor.

# Simulador de compra de remeras

Simulador interactivo de una tienda de remeras, hecho en JavaScript para Coderhouse. El programa muestra un menú por `prompt`, controla el stock de cada color y va armando un carrito de compras. Los mensajes se muestran con `alert` y también en la consola.

En esta entrega se incorporó la clase `Producto`: cada remera es un objeto que guarda sus propios datos y sabe venderse a sí misma.

## Cómo usarlo

1. Descargá o cloná el repositorio.
2. Abrí `index.html` en el navegador.
3. Elegí las opciones del menú escribiendo el número correspondiente.
4. Para ver los mensajes también en la consola, abrila con `F12`.

## Clase Producto

Cada remera se crea con `new Producto(tipo, color, stock, precio)`:

| Propiedad | Descripción |
|-----------|-------------|
| `tipo` | Tipo de prenda (`"Remera"`) |
| `color` | Color de la remera |
| `stock` | Unidades disponibles |
| `precio` | Precio en pesos |

**Método de instancia:** `vender()` resta una unidad de stock. Devuelve `true` si se pudo vender y `false` si no había stock.

## Productos y stock inicial

| Color | Stock | Precio |
|-------|-------|--------|
| Negra | 10 | $10000 |
| Roja | 4 | $7000 |
| Blanca | 7 | $8000 |
| Verde | 8 | $9000 |
| Azul | 5 | $6000 |

Las cinco remeras se guardan en el array `productos`. Cuando el stock de un color queda en 3 unidades o menos, el programa muestra un aviso de stock bajo.

## Menú de opciones

| Opción | Qué hace |
|--------|----------|
| 1 a 5 | Compra una remera (negra, roja, blanca, verde o azul) |
| 6 | Deshace la última compra y devuelve el stock |
| 7 | Consulta el stock de un color |
| 8 | Compra prioritaria: agrega la remera al principio del carrito |
| 9 | Entrega la primera remera del carrito |
| 10 | Cambia una remera del carrito por otro color |
| 11 | Sale del programa y muestra el carrito final |

## Conceptos aplicados

- Clases, constructor y `this` para modelar las remeras como objetos.
- Instancias creadas con `new`.
- Arrays (`productos` y `carrito`) y sus métodos: `push`, `pop`, `shift`, `unshift`, `find` y `splice`.
- `splice` para reemplazar una remera del carrito por su índice (opción 10).
- Ciclo `do...while` para repetir el menú hasta que se elija salir.
- Estructura `switch` para manejar las opciones.
- Condicionales y validaciones de los datos que ingresa la persona.
- Funciones con parámetros, función flecha (`esStockBajo`) y constante (`STOCK_BAJO`).

## Tecnologías

- HTML
- JavaScript

## Estructura del proyecto

```
├── index.html
├── js
│   └── main.js
└── README.md
```

## Autora

Florencia Francos, Coderhouse (curso de Desarrollo Web).
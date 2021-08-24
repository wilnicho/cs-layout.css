cs-layout.css
==============

Proyecto mantenido por `Wilfredo Nina Choquetarqui`.

Documentación y ejemplos [aquí](https://wilnicho.github.io/cs-layout.css).

¿Qué es cs-layout.css?
----------------------
Es una complemento `CSS` que ofrece un sistema de diseño responsivo basado en cuadrículas que facilita la creación de páginas web, el manejo de este complemento es similar al que `Bootstrap` tiene con su sistema de grillas, con filas y columnas, pero con la ventaja de ser no sólo flexible con el ancho de la pantalla sino que también con el alto, trabajando así a pantalla completa.

¿Qué necesito?
--------------
Incluya dentro de su proyecto el archivo `cs-layout.css` que debe descargar previamente.

```html static
<link rel="stylesheet" href="cs-layout.css">
```

| Clase | Descripción |
| - | - |
| `.layout-desktop` | El uso de esta clase indica que el comportamiento del diseño será responsivo. |
| `.layout-mobile` | El uso de esta clase indica que el comportamiento del diseño no será responsivo. |
| `.grid-row` | El uso de esta clase indica la creación de una fila. |
| `.grid-col` | El uso de esta clase indica la creación de una columna. |
| `.grid-cell` | El uso de esta clase indica la creación de una celda con un alto o un ancho flexible según el contenedor padre. |
| `.grid-cell-auto` | El uso de esta clase indica la creación de una celda con un alto o un ancho automático según el contenedor padre. |

### Ejemplo # 1

```html static
<div class="layout-desktop">
    <div class="grid-row">
        <div class="grid-cell">row # 1</div>
        <div class="grid-cell">row # 2</div>
        <div class="grid-cell">row # 3</div>
        <div class="grid-cell">row # 4</div>
        <div class="grid-cell">row # 5</div>
    </div>
</div>
```

### Ejemplo # 2

```html static
<div class="layout-desktop">
    <div class="grid-col">
        <div class="grid-cell">col # 1</div>
        <div class="grid-cell">col # 2</div>
        <div class="grid-cell">col # 3</div>
        <div class="grid-cell">col # 4</div>
        <div class="grid-cell">col # 5</div>
    </div>
</div>
```

### Ejemplo # 3

```html static
<div class="layout-desktop">
    <div class="grid-row">
        <div class="grid-cell-auto">header</div>
        <div class="grid-cell">main</div>
        <div class="grid-cell-auto">footer</div>
    </div>
</div>
```

### Ejemplo # 4

```html static
<div class="layout-desktop">
    <div class="grid-row">
        <div class="grid-cell-auto">header</div>
        <div class="grid-cell">
            <div class="grid-col">
                <div class="grid-cell-auto">aside</div>
                <div class="grid-cell">main</div>
            </div>
        </div>
        <div class="grid-cell-auto">footer</div>
    </div>
</div>
```

### Ejemplo # 5

```html static
<div class="layout-desktop">
    <div class="grid-row">
        <div class="grid-cell-auto">header</div>
        <div class="grid-cell-auto">nav</div>
        <div class="grid-cell">
            <div class="grid-col">
                <div class="grid-cell-auto">aside</div>
                <div class="grid-cell">
                    <div class="grid-row">
                        <div class="grid-cell">main</div>
                        <div class="grid-cell-auto">footer</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
```

### Integración con "jq-collapse.js"

Como habrá visto el complemento es muy fácil de usar y personalizar, además fue desarrollado pensando en la integración con [jq-collapse.js](https://wilnicho.github.io/jq-collapse.js) que hará mas interactiva la plantilla que diseñe, a continuación un ejemplo de su uso.

Licencia
--------
Copyright © 2021 Wilfredo Nina Choquetarqui; Publicado bajo la licencia MIT.

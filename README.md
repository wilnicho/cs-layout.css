cs-layout.css
=============

Librería ligera basada en Flexbox para la construcción de interfaces de pantalla completa.

Proyecto mantenido por `Wilfredo Nina Choquetarqui`.

Documentación y ejemplos [aquí](https://wilnicho.github.io/cs-layout.css).

¿Qué es cs-layout.css?
----------------------
Es una librería `CSS` ultra-ligera basada en `Flexbox`, diseñada específicamente para la construcción de interfaces de pantalla completa `Viewport-Locked UIs`. A diferencia de los frameworks tradicionales, ofrece un sistema bidireccional que permite un control total sobre el flujo horizontal y vertical, eliminando el scroll global de la ventana. Ideal para desarrolladores que buscan crear interfaces adaptables `Desktop/Mobile` que se ajusten perfectamente al marco de la pantalla sin complicaciones de cálculos manuales de altura.

¿Cómo se implementa?
--------------------
Descarga e incluye el archivo en el `<head>` de tu documento HTML:

```html static
<link rel="stylesheet" href="cs-layout.min.css">
```

La librería utiliza tres componentes clave para construir cualquier interfaz:

| Clase | Descripción |
| - | - |
| `.g-container` | El marco principal, por defecto ocupa todo el ancho y alto disponible. |
| `.g-row` `.g-col` | Define la dirección del flujo: vertical - filas u horizontal - columnas. |
| `.g-cell` | El bloque de contenido, se expande automáticamente para llenar el espacio sobrante. |
| `.g-cell-auto` | Bloque con tamaño fijo basado en su contenido, ideal para headers o footers. |
| `.g-static` | Modo Estático, desactiva el comportamiento responsivo para mantener el layout fijo en móviles, este modo no se hereda a las clases hijos asi que debe ser usado de la siguiente manera: &lt;div class="g-container g-static"&gt; &lt;div class="g-row g-static"&gt; &lt;div class="g-col g-static"&gt; |
| `.g-240` `.g-320` `.g-480` `.g-720` | Altura fija de 240px, 320px, 480px y 720px, se usan para definir un alto mínimo para la interfaz antes de que aparezca el scroll, debe ser usado solo de la siguiente manera: &lt;div class="g-container g-static g-480"&gt; &lt;div class="g-container g-480"&gt; |

Ejemplos prácticos
--------------------
A continuación, se presentan las estructuras más comunes resueltas con cs-layout. Copia y pega estas estructuras HTML para iniciar tu proyecto.

### Ejemplo # 1 (Diseño con solo filas)

```html static
<div class="g-container">
    <div class="g-row">
        <div class="g-cell">row # 1</div>
        <div class="g-cell">row # 2</div>
        <div class="g-cell">row # 3</div>
    </div>
</div>
```

### Ejemplo # 2 (Diseño con solo columnas)

```html static
<div class="g-container">
    <div class="g-col">
        <div class="g-cell">row # 1</div>
        <div class="g-cell">row # 2</div>
        <div class="g-cell">row # 3</div>
    </div>
</div>
```

### Ejemplo # 3 (Diseño básico de aplicación)

```html static
<div class="g-container">
    <div class="g-row">
        <div class="g-cell-auto">header</div>
        <div class="g-cell">main</div>
        <div class="g-cell-auto">footer</div>
    </div>
</div>
```

### Ejemplo # 4 (Diseño simple con menú lateral)

```html static
<div class="g-container">
    <div class="g-row">
        <div class="g-cell-auto">header</div>
        <div class="g-cell">
            <div class="g-col">
                <div class="g-cell-auto">aside</div>
                <div class="g-cell">main</div>
            </div>
        </div>
        <div class="g-cell-auto">footer</div>
    </div>
</div>
```

### Ejemplo # 5 (Diseño robusto con menú lateral y barra de navegación)

```html static
<div class="g-container">
    <div class="g-row">
        <div class="g-cell-auto">header</div>
        <div class="g-cell-auto">nav</div>
        <div class="g-cell">
            <div class="g-col">
                <div class="g-cell-auto">aside</div>
                <div class="g-cell">
                    <div class="g-row">
                        <div class="g-cell">main</div>
                        <div class="g-cell-auto">footer</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
```

### Ejemplo # 6 (Diseño robusto anidado)

```html static
<div class="g-container">
    <div class="g-row">
        <div class="g-cell-auto header">header 1</div>
        <div class="g-cell-auto nav">nav 1</div>
        <div class="g-cell">
            <div class="g-col">
                <div class="g-cell-auto aside">aside 1</div>
                <div class="g-cell">
                    <div class="g-row">
                        <div class="g-cell main" style="padding: 30px;">
                            <div class="g-row">
                                <div class="g-cell-auto header">header 2</div>
                                <div class="g-cell-auto nav">nav 2</div>
                                <div class="g-cell">
                                    <div class="g-col">
                                        <div class="g-cell-auto aside">aside 2</div>
                                        <div class="g-cell">
                                            <div class="g-row">
                                                <div class="g-cell main">main 2</div>
                                                <div class="g-cell-auto footer">footer 2</div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="g-cell-auto footer">footer 1</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>
```

Licencia
--------
Copyright © 2021 Wilfredo Nina Choquetarqui; Publicado bajo la licencia MIT.

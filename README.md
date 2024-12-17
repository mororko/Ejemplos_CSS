# CSS: Los conceptos esenciales que necesitas saber

Este documento presenta los **conceptos fundamentales** de CSS, siguiendo el principio **80/20** (Principio de Pareto), lo que significa que el **20% del conocimiento** aquí descrito te permitirá cubrir **el 80% de los casos prácticos** al momento de trabajar con CSS.

---

## 1. Selectores
Los **selectores** permiten aplicar estilos a elementos específicos de HTML:

- **Selector de tipo**: Selecciona todas las etiquetas de un tipo.
  ```css
  p {
    color: blue;
  }
  ```
- **Selector de clase**: Selecciona elementos con una clase específica.
  ```css
  .nombre-clase {
    font-size: 18px;
  }
  ```
- **Selector de ID**: Selecciona un elemento con un ID específico.
  ```css
  #nombre-id {
    background-color: yellow;
  }
  ```
- **Selector universal**: Selecciona todos los elementos.
  ```css
  * {
    margin: 0;
  }
  ```
- **Selectores combinados**:
  ```css
  div p {
    color: red; /* Todos los p dentro de un div */
  }
  ```

---

## 2. Propiedades clave
Las propiedades más comunes que debes dominar:

- **Color y fondo**:
  ```css
  color: red; /* Color del texto */
  background-color: #f0f0f0; /* Color de fondo */
  ```
- **Texto**:
  ```css
  font-size: 16px; /* Tamaño de la fuente */
  font-family: Arial, sans-serif; /* Familia tipográfica */
  text-align: center; /* Alineación del texto */
  ```
- **Espaciado**:
  ```css
  margin: 10px; /* Margen exterior */
  padding: 20px; /* Espaciado interno */
  ```
- **Bordes**:
  ```css
  border: 2px solid black; /* Borde */
  border-radius: 10px; /* Bordes redondeados */
  ```
- **Tamaño y posición**:
  ```css
  width: 200px; /* Ancho */
  height: 100px; /* Alto */
  ```

---

## 3. Modelo de Caja (Box Model)
Cada elemento HTML es una "caja" compuesta por:

- **Contenido** (content)
- **Relleno** (padding)
- **Borde** (border)
- **Margen** (margin)

Ejemplo:
```css
div {
  width: 100px;
  padding: 10px;
  border: 5px solid black;
  margin: 15px;
  box-sizing: border-box; /* Incluye padding y borde en el tamaño total */
}
```

---

## 4. Posicionamiento de elementos
Posiciona elementos con la propiedad `position`:

- **static**: Por defecto.
- **relative**: Posición relativa a su posición original.
- **absolute**: Posición respecto a su contenedor padre posicionado.
- **fixed**: Posición fija respecto a la pantalla.

Ejemplo:
```css
.ejemplo {
  position: relative;
  top: 10px;
  left: 20px;
}
```

---

## 5. Flexbox (Distribución flexible)
Flexbox permite **alinear** y **distribuir** elementos de manera eficiente.

- **Contenedor Flex**:
  ```css
  .contenedor {
    display: flex;
    justify-content: space-between; /* Distribuye elementos */
    align-items: center; /* Alinea verticalmente */
  }
  ```
- **Elementos hijos**:
  ```css
  .item {
    flex: 1; /* Elemento flexible */
  }
  ```

---

## 6. Media Queries (Diseño responsivo)
Adapta tu diseño a diferentes tamaños de pantalla:

```css
@media (max-width: 768px) {
  .contenedor {
    flex-direction: column; /* Cambia a una columna */
  }
}
```

---

## 7. Unidades de medida
Las unidades más importantes son:

- **Pixeles** (`px`): Tamaño fijo.
- **Porcentaje** (`%`): Relativo al contenedor padre.
- **Viewport** (`vw`, `vh`): Basado en el tamaño de la pantalla.
- **Em/Rem**: Unidades relativas al tamaño de la fuente.

Ejemplo:
```css
div {
  width: 50%; /* 50% del ancho del contenedor padre */
  font-size: 1.5rem; /* Relativo al tamaño base de la fuente */
}
```

---

## 8. Herencia y especificidad
- **Herencia**: Propiedades como `color` y `font-family` se heredan.
- **Especificidad**: Las reglas más específicas sobrescriben las generales.

Ejemplo:
```css
p {
  color: blue;
}
p.importante {
  color: red; /* Gana esta regla por ser más específica */
}
```

---

## Conclusión
Con estos conceptos básicos de CSS, podrás:

1. Seleccionar y estilizar elementos.
2. Controlar el espaciado y dimensiones.
3. Posicionar elementos en la página.
4. Crear diseños flexibles y responsivos.

Una vez dominados estos puntos, estarás preparado para profundizar en temas más avanzados como Grid, animaciones y preprocesadores como Sass.

---

¡Manos a la obra! 🚀

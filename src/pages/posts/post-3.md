---
layout: ../../layouts/MarkdownPostLayout.astro
title: My Therd Blog Post
author: 'Vaccari, Franco'
description: "After learning some Astro, I couldn't stop!"
image:
    url: "https://docs.astro.build/assets/arc.webp"
    alt: "Thumbnail of Astro arcs."
pubDate: 2024-02-01
tags: [ "blogging", "learning in public"]
----

<!---Títulos--->

# Título h1

## Título h2

### Título h3

#### Título h4

##### Título h5

###### Título h6

<!--- Italica, negita y tachado--->

Texto en _itálica_  
Texto en **negrita**  
Texto en ~~Tachado~~

<!--- Listas ordenadas y desordenadas --->

1. Item uno
   1. Item 1.1
2. Item dos
   1. Item 2.1
   2. Item 2.2
3. Item 3

- Item 1
  - subitem 1
  - subitem 2
- Item 2
- Item 3

<!--- Enlaces --->

[enlace de Github](https://github.com/FrancoVacc "Github profile")

<!--- Citas de texto--->

> Esta es una cita de un texto, para aclarar algunos puntos importantes

<!--- lineas divisorias--->

---

<!--- Código en una linea --->

` console.log("hola mundo")`

<!--- Multiples lineas de código--->

```javascript
const ordenarProducto = (producto) => {
  return new Promise((resolve, reject) => {
    console.log(`Ordenando ${producto}`);
    setTimeout(() => {
      if (producto == "taza") {
        resolve("Ordenando una taza con el logo de un auto");
      } else {
        reject("Este producto no esta disponible...");
      }
    }, 2000);
  });
};
```

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <link rel="stylesheet" href="./css/index.css" />
  </head>
  <body>
    <div class="container">
      <div class="header-container">
        <header>
          <div></div>
        </header>
      </div>
      <div class="description-container">
        <article>
          <p>PERFUME</p>
          <h2>Gabrielle Essence Eau De Perfum</h2>
          <p class="description">
            A floral, solar and voluptuous interpretation composed by Oliver
            Polge, Perfume-Creator for the House of CHANEL.
          </p>
        </article>
        <section>
          <h3>$149.99</h3>
          <p>$169.99</p>
        </section>
        <div class="boton">
          <button>
            <img src="./images/icon-cart.svg" alt="Cart" />
            <p>Add to Cart</p>
          </button>
        </div>
      </div>
    </div>
  </body>
</html>
```

<!--- Tablas --->

| Encabezado | Encabezado 2 | Encabezado 3 |
| ---------- | ------------ | ------------ |
| Contenido  | Contenido    | Contenido    |
| Contenido  | Contenido    | Contenido    |

<!---imagenes--->

![Visual Studio Code Imgagen](https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Visual_Studio_Code_1.35_icon.svg/2048px-Visual_Studio_Code_1.35_icon.svg.png "visualStudio")

<!--GitHub Markdown-->

#### Lista de tareas

- [x] tarea 1 (cumplida)
- [x] tarea 2 (cumplida)
- [ ] tarea 3 (sin cunplir)

#### Etiquetar usuario

@FrancoVacc

#### Emojis

:smily: :+1:

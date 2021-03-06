# QA

* Tipo: `seminario`
* Formato: `guiado`
* Duración: `10min`

***

## `PropTypes`

Define los `PropTypes` para los siguientes tipos de `props`

* Cualquier tipo
* `String` o `boolean`
* Una fecha
* Un elemento `JSX`
* Alguno de estos tres valores: `'manzanas'`, `'naranjas'`, `'plátanos'` o la
  siguiente forma `{ otro: '[cualquier otra fruta]' }`
* una lista de `items` con identificadores únicos:
  ```js
  // valor valido
  const items = [
    { id: 'id-1', texto: 'Un texto' },
    { id: 'id-2', texto: 'Otro texto' },
    // el texto puede repetirse
    { id: 'id-3', texto: 'Otro texto' },
  ]

  // valor inválido
  const items = [
    { id: 'id-1', texto: 'Un texto' },
    { id: 'id-2', texto: 'Otro texto' },
    // id repetido
    //      ↓
    { id: 'id-2', texto: 'Otro texto' },
  ]
  ```

## Distintos `hijos` con comportamiento similar

Desarrolla un componente `Lista` que dado el siguiente código `jsx`

```html
  <Lista>
    <span>Child 1</span>
    <strong>Child 2</strong>
    <a href="#">Child 3</a>
    <em>Child 4</em>
  </Lista>
```

retorne

```html
<ul>
  <li><span>Child 1</span></li>
  <li><strong>Child 2</strong></li>
  <li><a href="#">Child 3</a></li>
  <li><em>Child 4</em></li>
</ul>
```

## Plantilla

Desarrolla una plantilla que permita crear múltiples `Paginas` distintas que
compartan un `Header` y un `Footer`, solo definiendo el contenido que es
diferentes. Por ejemplo:

```html
<Pagina titulo="Seccion">
  <section>
    <h3>Titulo de una seccion</h3>
    <p>Lorem...</p>
  </section>
</Pagina>
```

retorna algo parecido a esto

```html
  <div class="pagina">
    <header>
      <h1 class="brand">Nombre fijo</h1>
      <h2 class="titulo">Seccion</h2>
    </header>
    <section>
      <h3>Titulo de una seccion</h3>
      <p>Lorem...</p>
    </section>
    <footer>
      <small>Algunos derechos reservados</small>
    </footer>
  </div>
```

Y lo siguiente

```html
<Pagina titulo="Lista de elementos">
  <ul>
    <li>elemento 1</li>
    <li>elemento 2</li>
    <li>elemento 3</li>
  </ul>
</Pagina>
```

retorna

```html
  <div class="pagina">
    <header>
      <h1 class="brand">Nombre fijo</h1>
      <h2 class="titulo">Seccion</h2>
    </header>
    <ul>
      <li>elemento 1</li>
      <li>elemento 2</li>
      <li>elemento 3</li>
    </ul>
    <footer>
      <small>Algunos derechos reservados</small>
    </footer>
  </div>
```

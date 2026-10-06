# Agenda de contactos

Aplicación web que muestra el listado de contactos guardados y permite agregar nuevos. Cada contacto tiene **nombre**, **apellido** y **teléfono**.

## Capturas

### Listado de contactos
![Listado de contactos](capturas/lista.png)

### Formulario para agregar un contacto
![Formulario de nuevo contacto](capturas/formulario.png)

### Contacto agregado
![Contacto agregado a la lista](capturas/agregado.png)

## Tecnologías

- HTML, CSS y JavaScript (sin librerías externas)
- `fetch` para consumir la API

## API utilizada

URL: `http://www.raydelto.org/agenda.php`

| Método | Acción | Cuerpo |
|--------|--------|--------|
| `GET` | Devuelve el listado de contactos en JSON | — |
| `POST` | Agrega un contacto nuevo | `{ "nombre": "", "apellido": "", "telefono": "" }` |

Ejemplo del `POST`:

```js
fetch("http://www.raydelto.org/agenda.php", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({ nombre: "Ana", apellido: "Pérez", telefono: "809-555-0101" })
});
```

## Funcionalidades

- Carga y muestra todos los contactos al abrir la página.
- Formulario con validación: los tres campos son obligatorios.
- Al guardar, el contacto se envía a la API y la lista se actualiza.
- Mensajes de estado (guardando, guardado, error).
- Diseño adaptable a pantallas de escritorio y móvil.

## Cómo ejecutarlo

1. Clone el repositorio:
   ```bash
   git clone https://github.com/K-oss47/Agenda_Multicapas.git
   ```
2. Abra la carpeta en VS Code.
3. Abra `agenda.html` con la extensión **Live Server** o directamente en el navegador.

> La API usa `http://`, por lo que la página debe abrirse en local. Si se publica con HTTPS (por ejemplo GitHub Pages), el navegador bloquea las peticiones.

## Estructura

```
Agenda_Multicapas/
├── agenda.html
├── README.md
└── capturas/
    ├── lista.png
    ├── formulario.png
    └── agregado.png
```

## Autor

Kelvin Mercedes — ITLA
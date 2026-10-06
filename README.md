# Agenda de contactos

Aplicación web que muestra el listado de contactos guardados y permite agregar nuevos. Cada contacto tiene **nombre**, **apellido** y **teléfono**.

## Capturas

### Listado de contactos
<img width="1906" height="935" alt="image" src="https://github.com/user-attachments/assets/d2089db8-7e24-41e6-88c6-b428c8a00917" />


### Formulario para agregar un contacto
<img width="991" height="895" alt="image" src="https://github.com/user-attachments/assets/4bb5b58f-25ca-4d04-ba90-02f6324a3089" />


### Contacto agregado
<img width="1600" height="781" alt="image" src="https://github.com/user-attachments/assets/947a44f3-cf66-4bb2-8a0a-f66cbe82cf88" />


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
└── README.md
    
```

## Autor

Kelvin Mercedes — ITLA

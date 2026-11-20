# Simulación de prueba técnica: Sistema de Biblioteca en C#

¡Bienvenida! Este ejercicio no busca que lo hagas perfecto. Queremos ver cómo piensas, cómo organizas tu código y cómo trabajas con Git y GitHub. Es una buena práctica de lo que se hace en el día a día de un equipo.

- **Fecha de entrega:** 04 de diciembre
- **Lenguaje:** C# (.NET 8 o superior)
- **Tipo de proyecto:** aplicación de consola

---

## 1. Reglas del juego

Lo más importante es que aprendas y te sientas preparada para una entrevista real. Por eso:

- ✅ Puedes consultar la documentación de Microsoft, tutoriales, foros y videos.
- ✅ Puedes escribir con toda confiazaza si te bloqueas. Preguntar a tiempo es una buena señal.
- ❌ Por favor no le pidas a una IA que haga el trabajo por ti. Si la usas para entender un concepto está excelente, pero el código debe ser tuyo y debes poder explicarlo.
- 🗣️ Después de la entrega te pediremos que expliques lo que hiciste y que cambies algo pequeño en vivo.

---

## 2. El problema

Una biblioteca pequeña necesita un programa de consola para manejar sus **libros**, sus **usuarios** y los **préstamos**.

### Clases que debes crear

| Clase | Datos mínimos |
|---|---|
| `Libro` | Id, título, autor, año, género y si está disponible o prestado |
| `Usuario` | Id, nombre y correo |
| `Prestamo` | Id, libro, usuario, fecha de préstamo, fecha límite y fecha de devolución (puede estar vacía si aún no lo devuelve) |

---

## 3. Lo que debe hacer tu programa (obligatorio)

### Funciones
1. Registrar y mostrar libros.
2. Registrar y mostrar usuarios.
3. Prestar un libro a un usuario.
4. Devolver un libro.
5. Un menú en la consola para usar todo lo anterior.

### Reglas que debe cumplir
- Un libro que ya está prestado **no** se puede volver a prestar.
- Un usuario no puede tener más de **3 préstamos activos** (sin devolver) al mismo tiempo.
- No se pueden registrar dos usuarios con el mismo correo.
- Si algo sale mal (por ejemplo, el libro no existe), el programa debe mostrar un mensaje claro y **no cerrarse con error**.

### Consultas con LINQ
Haz estas consultas y que se puedan usar desde el menú:
1. Mostrar los libros disponibles.
2. Buscar libros por autor (que funcione aunque escriba en mayúsculas o minúsculas).
3. Mostrar los préstamos activos de un usuario.
4. Mostrar los préstamos vencidos (pasó la fecha límite y no se han devuelto).
5. Mostrar los 3 libros más prestados.
6. Mostrar cuántos libros hay de cada género.

### Cómo debe estar hecho el código
- Usa **POO**: crea cada clase con sus propiedades y su constructor, y no pongas todo el código en una sola clase.
- Separa las tareas: una clase para manejar la biblioteca (libros, usuarios, préstamos) y otra para el menú y los mensajes en pantalla.
- Guarda los datos en memoria usando `List<T>`.
- Usa nombres claros para clases, métodos y variables.
- Los `Console.WriteLine` deben estar en el menú, no dentro de las clases que manejan la lógica.

---

## 4. Extras opcionales (suman, pero no son obligatorios)

Elige solo si te sobra tiempo. Es mejor uno bien hecho que tres a medias.

- 💾 Guardar y cargar los datos en un archivo JSON.
- 🧪 Pruebas automáticas (con xUnit) para al menos 3 de las reglas.
- 💸 Cobrar una multa por cada día de retraso al devolver un libro.
- 🧱 Usar herencia o una interfaz en alguna parte del programa y explicar por qué.

---

## 5. Cómo entregar tu trabajo en GitHub

Esta parte también se evalúa. Es práctica para trabajar en equipo.

1. **Clona** este repositorio en tu computador (lo descargas con Git):
   ```bash
   git clone URL-DEL-REPOSITORIO
   ```
2. **No trabajes en la rama `main`.** Crea tu propia rama:
   ```bash
   git checkout -b practica/tu-nombre
   ```
3. Mientras avanzas, guarda tu trabajo con **commits pequeños y con mensajes claros** (no un solo commit gigante al final):
   ```bash
   git add .
   git commit -m "Agrega la clase Libro"
   ```
   Otros ejemplos de mensajes:
   - `Agrega regla de máximo 3 préstamos`
   - `Crea consulta de libros disponibles`
4. **Sube** tu rama al repositorio en GitHub:
   ```bash
   git push -u origin practica/tu-nombre
   ```
5. En GitHub, crea un **Pull Request** (es una solicitud para revisar tus cambios y los unamos a `main`), puedes hacer el pull cuando ya termines. Usa la plantilla de la sección 6.
6. Si te dejamos comentarios en el Pull Request, responde y haz los cambios en la misma rama.

---

## 6. Plantilla para el Pull Request

Copia esto en la descripción de tu Pull Request y respóndelo **con tus propias palabras**:

```md
## ¿Qué hice?
(Un resumen corto de lo que programé)

## ¿Cómo organicé mi código?
- ¿Qué clases creé y para qué sirve cada una?

## ¿Qué fue lo más difícil y cómo lo resolví?

## ¿Qué aprendí?

## ¿Qué mejoraría si tuviera más tiempo?

## Extras que hice (si hiciste alguno)

## Cómo ejecutar el proyecto
```

---

## 7. Cómo vamos a revisar tu trabajo

| Qué miramos | Detalle |
|---|---|
| Que funcione | Que cumpla lo que se pide y las reglas |
| POO | Clases bien creadas y cada una con su tarea |
| LINQ | Consultas correctas y fáciles de leer |
| Orden del código | Nombres claros, código limpio y manejo de errores |
| Git y GitHub | Rama propia, commits claros y Pull Request bien explicado |
| Explicación | Que puedas contar lo que hiciste y por qué |

No esperamos que sea perfecto. Valoramos más un código sencillo que entiendes que uno complicado que no puedes explicar.

---

## 8. ¿Dudas?

Si te sientes atascada con lo mismo (después de revisar la documentación, ver tutoriales, etc.), escríbenos. Preferimos que preguntes a que llegues al final sin avanzar. ¡Mucho éxito! 🚀

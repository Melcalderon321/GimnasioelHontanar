# Gimnasio El Hontanar - Sitio Web Oficial

Un proyecto web descriptivo diseñado para gestionar, presentar e ilustrar las actividades, programas académicos, servicios de consejería y bienestar del Gimnasio El Hontanar.

Este repositorio sirve como entorno para la publicación, pruebas y despliegue del sitio web oficial a través de GitHub.

---

## 🚀 Guía de Git y GitHub para Principiantes

Esta guía contiene los comandos fundamentales para gestionar cambios, subir actualizaciones y navegar por el historial del proyecto.

### 1. Guardar y Subir Cambios a GitHub

Cuando realices modificaciones en los archivos del sitio web (`.html`, `.css`, `.js`), sigue estos pasos para registrarlos y subirlos a la nube:

#### Paso 1: Ver el estado del proyecto
Muestra los archivos modificados, nuevos o eliminados.
```bash
git status
```

#### Paso 2: Seleccionar los cambios para guardar (Add)
Puedes agregar archivos específicos o todos a la vez.
* Para agregar un archivo en particular:
  ```bash
  git add nombre-del-archivo.html
  ```
* Para agregar todos los cambios de una sola vez (recomendado):
  ```bash
  git add .
  ```

#### Paso 3: Confirmar los cambios (Commit)
Crea una especie de "punto de control" con un mensaje descriptivo que resuma lo que hiciste.
```bash
git commit -m "Descripción clara de los cambios realizados"
```

#### Paso 4: Subir a GitHub (Push)
Envía tus puntos de control locales a la rama principal en la nube.
```bash
git push
```

---

### 2. Traer Cambios desde GitHub (Sincronizar)

Si realizaste cambios directamente desde la interfaz web de GitHub o si estás trabajando en equipo, debes descargar las actualizaciones en tu equipo local antes de seguir trabajando:
```bash
git pull
```

---

### 3. Trabajar con Ramas (Branches)

Las ramas te permiten experimentar o agregar nuevas secciones web sin alterar la versión estable del sitio (`main`).

#### Crear una nueva rama y cambiarse a ella:
```bash
git checkout -b nombre-de-la-rama
```
*(Por ejemplo: `git checkout -b nueva-galeria`)*

#### Listar todas las ramas disponibles:
```bash
git branch
```

#### Cambiar de una rama a otra ya existente:
```bash
git checkout main
```

#### Unir los cambios de otra rama a la rama principal (`main`):
1. Asegúrate de estar en `main`: `git checkout main`
2. Fusiona la otra rama:
   ```bash
   git merge nombre-de-la-rama
   ```

---

### 4. Volver al Pasado (Historial y Commits anteriores)

Si cometiste un error o necesitas ver/recuperar una versión anterior del código, puedes moverte a través del historial de confirmaciones.

#### Paso 1: Ver el historial de confirmaciones (Logs)
Muestra la lista de commits con su identificador único (un código hexadecimal largo llamado `HASH`).
```bash
git log --oneline
```
*Esto mostrará algo como:*
`a1b2c3d Modificaciones en la página de admisiones`
`e5f6g7h Creación de la sección de robótica`

#### Paso 2: Volver temporalmente a un commit anterior
Si deseas inspeccionar el código tal como estaba en un punto específico sin borrar nada:
```bash
git checkout HASH
```
*(Ejemplo: `git checkout e5f6g7h`)*

*Para regresar al presente (la última versión en la rama principal):*
```bash
git checkout main
```

#### Paso 3: Deshacer cambios no confirmados (Reset local)
* Si quieres descartar todos los cambios locales no guardados en un archivo específico y volver al último commit:
  ```bash
  git checkout -- nombre-del-archivo.html
  ```
* Si quieres descartar por completo todos los cambios locales en todos los archivos:
  ```bash
  git reset --hard HEAD
  ```

---

### 🧑‍💻 Consejos útiles para desarrollo web
* Realiza confirmaciones (`git commit`) pequeñas y frecuentes para evitar conflictos complejos.
* Mantén el sitio ordenado organizando tus hojas de estilo `.css` en sus carpetas correspondientes.
* Antes de iniciar una jornada de código, ejecuta siempre `git pull` para asegurarte de tener la versión más actualizada.

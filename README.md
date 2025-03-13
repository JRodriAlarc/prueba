# 📌 Práctica de Git y GitHub  

![Estado del Proyecto](https://img.shields.io/badge/STATUS-EN%20DESARROLLO-green)

Este repositorio está destinado a la práctica de conceptos y comandos de Git, facilitando el control de versiones y la gestión de repositorios tanto locales como remotos en GitHub.  

## 🚀 Acceso rápido a VS Code Web  

Puedes abrir este repositorio en el editor web ligero de VS Code (`vscode.dev`) presionando la tecla `"."` en la página del repositorio.  

## 📂 Reglas para nombrar carpetas y archivos  

Al nombrar archivos y carpetas, sigue estas buenas prácticas:  

✅ Usa solo **letras minúsculas**  
✅ Separa palabras con **guiones medios (`-`)**  
✅ Evita caracteres especiales  
✅ No uses **espacios en blanco** ni **guiones bajos (`_`)**  
✅ Mantén los nombres **cortos y descriptivos**  


## 📝 Commits Convencionales  

Seguir una convención clara al nombrar los commits facilita la comprensión del historial de cambios. Algunas buenas prácticas son:  

### ✨ Formato recomendado 

```bash
<tipo> (área): <descripción corta>
```

### 📌 Ejemplo:

```
feat(auth): agregar autenticación con JWT
fix(ui): corregir error en el botón de inicio
docs(readme): actualizar sección de commits
```

### 🔹 Tipos de commits comunes

| Tipo  | Descripción |
|-------|------------|
| `feat` | Añade una nueva funcionalidad |
| `fix`  | Corrige un error |
| `docs` | Cambios en la documentación |
| `style` | Cambios de formato (espacios, comas, etc.), sin afectar código |
| `refactor` | Refactorización de código sin cambiar su funcionalidad |
| `test` | Agrega o modifica pruebas |
| `chore` | Cambios en configuración o mantenimiento del proyecto |

### ✅ Reglas generales  

- Usa el **modo imperativo** en la descripción: _"añadir login"_, _"corregir bug"_.  
- Mantén la descripción breve y clara (máximo 72 caracteres).  
- Si el commit es muy grande, usa la opción `-m "mensaje"` varias veces o un commit extendido con `git commit` sin `-m`.  

---

## ✍️ Comandos de Git

### 🗃️ 1. Git Clone

El comando `git clone` se utiliza para clonar un repositorio existente, es decir, para crear una copia del mismo en tu entorno local. Esta copia mantiene todo el historial del repositorio original, incluyendo sus archivos y configuraciones, permitiéndote trabajar de forma aislada del repositorio principal.

Puedes clonar un repositorio en tu máquina local y trabajar con él sin afectar al repositorio original

- #### 1.1 Con el `git clone` también puedes clonar el repositorio para una carpeta específica:
```bash
git clone <repositorio> <mi-proyecto-clone>
```

- #### 1.2 El repositorio localizado en `repositorio` es clonado para una carpeta llamada:

```bash
mi-proyecto-clone
```

- #### 1.3 También puedes configurar el `git clone` y clonar el repositorio desde una **branch** específica, diferente a la original, de esta manera:

```bash
git clone -branch new_feature <repositorio>
```
Consulta la [documentación oficial](https://git-scm.com/docs/git-clone) para más detalles.


### ⌛ 2. Git Log

El comando `git log` te permite visualizar el historial de commits de un repositorio. Esto incluye los mensajes de commit, el autor y la fecha. Puedes usar diversas opciones para personalizar la salida y obtener solo la información que necesites.

- #### 2.1 Puedes visualizar un **resumen** de todos los commits:

```bash
git log –oneline
```

- #### 2.2 Si, en lugar de menos informaciones, queremos ver más, como las `alteraciones del commit`, podemos usar:

```bash
git log -p
```

- #### 2.3 También podemos buscar las informaciones de la persona **autora** del commit con el comando:

```bash
git log --author="user_name"
```

- #### 2.4 Y buscar informaciones por fecha:

```bash
git log --since=1.month.ago --until=1.day.ago
```

**Opciones comunes**:  
- Visualizar los commits en una línea.
- Ver los cambios detallados realizados en cada commit.
- Filtrar los commits por autor o por fechas específicas.

- #### 2.5 También es posible `formatear la visualización` de las informaciones del commit con el comando:

```bash
git log --pretty="format:%h %s"
```

Para más opciones y personalizaciones, revisa la [documentación oficial](https://devhints.io/git-log-format).

### ⏸️ 3. Git Status

El comando `git status` te permite ver el estado actual del repositorio en tu entorno local. Muestra los cambios que no han sido registrados **(staged)** o confirmados **(committed)**, así como las ramas activas y las diferencias con el repositorio remoto.

- #### 3.1 Con `git status`, puedes revisar qué archivos están modificados, cuáles están listos para ser confirmados **(staged)** y si hay archivos sin seguimiento **(untracked)**.

```bash
git status
```

Este comando te ayudará a mantenerte informado sobre el estado de tus cambios antes de realizar una confirmación **(commit)**.

### ⛔ 4. Git Diff

El comando `git diff` te permite ver las diferencias entre los archivos modificados en tu entorno local y el último commit. Es útil para revisar cambios antes de hacer un commit y asegurarte de que solo se incluyan los cambios deseados.

- #### 4.1 Por defecto, `git diff` muestra las diferencias en el contenido de los archivos

```bash
git diff
```

- #### 4.2 Si deseas comparar los cambios de un archivo específico, puedes indicar el **nombre del archivo**:

```bash
git diff <archivo>
```

### 🔄 5. Git Restore

El comando `git restore` se utiliza para descartar cambios locales que aún no han sido confirmados. Es útil si realizas cambios en un archivo pero decides que no deseas conservarlos.

Puedes usar git restore para `restaurar un archivo` a su estado en el último commit o incluso restaurar archivos eliminados.

- #### 5.1 Restaurar un archivo específico al último commit

```bash
git restore <archivo>
```

- #### 5.2 Restaurar archivos a un commit específico

Primero debes obtener el HASH del commit utilizando el comando `git log --oneline`, que muestra una lista de los commits con su respectivo identificador (SHA-1 hash). Luego, puedes usar el comando `git restore` especificando el commit y el archivo que deseas restaurar.

- ##### 5.2.1 Obtener los commits recientes:

```bash
git log --oneline
```

- ##### 5.2.2 Restaurar un archivo desde un commit específico:

```bash
git restore --source <SHA-1-hash> <archivo>
```

Este comando **descarta los cambios locales** sin guardarlos, por lo que es importante estar seguro de que no necesitas esos cambios antes de ejecutar el comando.
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
<tipo>(<área>): <descripción corta>
```

#### 📌 Ejemplo:

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
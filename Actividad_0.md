# 🧭 Actividad 0 – Configura tu entorno Git

> Actividad inicial de Git para GitHub Classroom.  
> Objetivo: dejar tu **usuario de Git** correctamente configurado y listo para usar en futuras actividades.

---

## 📌 Información de la tarea (para el alumnado)

- **Tipo de actividad:** Individual  
- **Entrega:** Mediante repositorio de GitHub Classroom (este repositorio)  
- **Requisitos para completar la tarea:**
  - Configurar tu identidad en Git.
  - Ajustar opciones básicas (rama `main`, saltos de línea, editor, colores, alias).
  - Subir al repositorio un archivo con tu configuración y respuestas.

---

## ✅ Objetivos de aprendizaje

Al finalizar esta actividad serás capaz de:

- Configurar tu **nombre** y **correo** en Git.
- Establecer la rama principal por defecto como `main`.
- Configurar los **saltos de línea** según tu sistema operativo.
- Elegir tu **editor** por defecto y activar colores en la terminal.
- Crear algunos **alias** útiles de Git.
- Crear tu **primer repositorio local** y verificar la rama `main`.

---

## 🧰 Paso 0. Comprobación de instalación

### 🔍 Explicación
Antes de empezar, asegúrate de que Git está instalado en tu ordenador.

### 🧩 Reto 0
En tu terminal, ejecuta:

```bash
git --version
```

Si no aparece una versión (por ejemplo `git version 2.43.0`), instala Git en tu sistema.

> No es necesario subir nada en este paso, pero **sin Git instalado no podrás continuar**.

---

## 👤 Paso 1. Configura tu identidad de usuario

### 💬 Explicación
Git necesita saber quién eres para asociar tus cambios (commits) a tu identidad.

### 🧩 Reto 1
Ejecuta en tu terminal, sustituyendo por tus datos reales:

```bash
git config --global user.name "Tu Nombre Completo"
git config --global user.email "tucorreo@example.com"
```

### ✅ Checkpoint 1 – Evidencia en el repositorio
1. Ejecuta:
   ```bash
   git config --global --list
   ```
2. Copia el resultado en un archivo llamado:  
   `config-git-global.txt`  
3. Añádelo y súbelo a **este repositorio**.

---

## ⚙️ Paso 2. Ajusta la configuración global básica

### 💬 Explicación
Vas a personalizar cómo se comporta Git en todos tus proyectos.

### 🧩 Reto 2

1. **Rama principal por defecto como `main`:**
   ```bash
   git config --global init.defaultBranch main
   ```

2. **Saltos de línea según tu sistema operativo:**
   - Si usas Linux o macOS:
     ```bash
     git config --global core.autocrlf input
     ```
   - Si usas Windows:
     ```bash
     git config --global core.autocrlf true
     ```

3. **Editor de texto por defecto (ejemplo: VS Code):**
   ```bash
   git config --global core.editor "code --wait"
   ```

4. **Colores en la terminal:**
   ```bash
   git config --global color.ui auto
   ```

### ✅ Checkpoint 2 – Evidencia en el repositorio

1. Vuelve a ejecutar:
   ```bash
   git config --global --list
   ```
2. Comprueba que aparecen:
   - `user.name`
   - `user.email`
   - `init.defaultBranch`
   - `core.autocrlf`
   - `core.editor`
   - `color.ui`
3. En el archivo `config-git-global.txt`, añade al final una breve explicación (1–2 líneas) de qué hace **cada uno** de esos parámetros.

> Ejemplo de explicación:  
> `init.defaultBranch=main → Hace que la rama inicial de un nuevo repositorio se llame main en lugar de master`.

---

## 🌈 Paso 3. Personaliza Git con alias

### 💬 Explicación
Los alias te permiten escribir comandos más cortos y trabajar más rápido.

### 🧩 Reto 3
Configura estos alias:

```bash
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.cm "commit -m"
```

Prueba en tu terminal:

```bash
git st
```

### ✅ Checkpoint 3 – Evidencia en el repositorio

1. Ejecuta:
   ```bash
   git config --global --list
   ```
2. Asegúrate de que aparecen los alias (`alias.st`, `alias.co`, etc.).  
3. En el archivo `config-git-global.txt`, añade una breve explicación de **al menos dos alias** indicando por qué te parecen útiles.

---

## 📁 Paso 4. Crea un repositorio local de prueba

> **Nota:** Este paso es local, sirve para comprobar que tu configuración funciona correctamente.

### 🧩 Reto 4

En tu terminal:

```bash
mkdir mi_primer_repo_git
cd mi_primer_repo_git
git init
git branch
```

Comprueba que la rama que aparece se llama `main`.

### ✅ Checkpoint 4 – Evidencia en el repositorio

1. En el repositorio de Classroom (este), crea un archivo llamado:  
   `reflexion-repo.md`
2. Escribe (en 3–5 líneas):
   - Qué has hecho en este paso.
   - Si la rama inicial se llama `main` o no, y por qué crees que es importante.

---

## 🎓 Paso 5. Reflexión final (obligatoria para la entrega)

Crea (o edita) el archivo `reflexion-repo.md` y añade:

1. Una explicación breve de por qué es importante:
   - Tener bien configurado `user.name` y `user.email`.
   - Configurar correctamente los saltos de línea (`core.autocrlf`) en equipos con diferentes sistemas operativos.
2. Indica qué alias crees que vas a usar más y por qué.
3. Si has tenido algún problema durante la configuración, descríbelo y cómo lo has solucionado.

---

## 📦 Qué debe contener tu repositorio al entregar

Al finalizar la actividad, este repositorio **debe incluir** al menos:

- `config-git-global.txt`  
  - Salida de `git config --global --list`
  - Explicaciones de los parámetros indicados
- `reflexion-repo.md`  
  - Respuestas a las preguntas de reflexión

> No es necesario subir tu repositorio local de prueba (`mi_primer_repo_git`), solo las evidencias pedidas en este repositorio.

---

## 🧑‍🏫 Nota para el profesorado

- Este repositorio está pensado como **repositorio plantilla** para una **actividad individual** en GitHub Classroom. [web:1][web:3]
- Se recomienda:
  - Configurar la actividad como **individual assignment**.
  - Usar este repositorio como **template repository** en GitHub Classroom. [web:1][web:3][web:8]
  - Evaluar principalmente:
    - Existencia y contenido de `config-git-global.txt`.
    - Existencia y calidad de `reflexion-repo.md`.
    - Coherencia entre la configuración reportada y lo esperado (rama `main`, alias, etc.).

---

## 🏁 Criterios de evaluación sugeridos

- ✅ 4 pts – Configuración de Git completa y correcta (nombre, email, rama `main`, `core.autocrlf`, editor, colores, alias).  
- ✅ 3 pts – Archivo `config-git-global.txt` presente y bien documentado.  
- ✅ 2 pts – Archivo `reflexion-repo.md` presente con respuestas claras y razonadas.  
- ✅ 1 pt – Presentación, orden y claridad de los archivos.

**Puntuación máxima: 10 puntos.**

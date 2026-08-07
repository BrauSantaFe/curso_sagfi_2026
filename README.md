# Curso Práctico de Git y GitHub

Este repositorio contiene las notas, ejercicios y comandos revisados durante el Curso de Git y GitHub. El objetivo principal fue dominar el flujo de trabajo esencial del control de versiones, desde los comandos básicos locales hasta la colaboración y sincronización con repositorios remotos en GitHub.

---

## Contenido del Curso

1. Introducción al Control de Versiones: Conceptos de árbol de trabajo (Working Directory), área de preparación (Staging Area) y repositorio (Repository).
2. Configuración Inicial de Git: Nombre de usuario, email e identificación.
3. Flujo de Trabajo Local: Inicialización, estados de archivos, commits y revisión de historial.
4. Conexión con GitHub: Autenticación, vinculación de repositorios locales y remotos.
5. Clonación y Sincronización: Clonar repositorios existentes y subir cambios mediante push.

---

## Comandos Esenciales Revisados

### 1. Configuración de Entorno

# Configurar nombre de usuario
git config --global user.name "TuNombre"

# Configurar correo electrónico asociado a GitHub
git config --global user.email "tu_email@ejemplo.com"

# Verificar la configuración aplicada
git config --list


### 2. Flujo de Trabajo Local

# Inicializar un nuevo repositorio en la carpeta actual
git init

# Consultar el estado de los archivos (Working Tree vs Staging Area)
git status

# Añadir archivos al área de preparación (Staging Area)
git add nombre_archivo.ext   # Archivo específico
git add .                    # Todos los archivos modificados

# Registrar los cambios en el historial local
git commit -m "Mensaje claro explicativo de los cambios"

# Visualizar el historial de commits
git log --oneline


---

## Conexión con un Repositorio Remoto (GitHub)

Para vincular un proyecto local existente a un repositorio alojado en GitHub:

### Paso 1: Vincular el repositorio remoto

# Crear la rama principal (main) si no existe
git branch -M main

# Añadir la URL del repositorio remoto
git remote add origin https://github.com/usuario/nombre-del-repositorio.git

# Verificar la conexión remota
git remote -v


### Paso 2: Subir cambios locales por primera vez

# Enviar el código de la rama local 'main' al remoto 'origin'
git push -u origin main

(Nota: El parámetro -u vincula la rama local con la remota, permitiendo usar simplemente `git push` en ejecuciones posteriores)

---

## Clonar un Repositorio Existente

Para descargar una copia de un repositorio que ya se encuentra en GitHub hacia tu equipo local:

# Clonar repositorio mediante HTTPS
git clone https://github.com/usuario/nombre-del-repositorio.git

# Entrar a la carpeta descargada
cd nombre-del-repositorio


Una vez clonado, puedes realizar modificaciones locales, hacer `git add`, `git commit` y subir los cambios directamente con:

git push


---

## Resumen del Flujo Diario

[ Modificar archivos ] -> git add . -> git commit -m "..." -> git push
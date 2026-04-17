# 🚀 Guía básica Git para GitHub
[![Website](https://img.shields.io/badge/Web-miquelnebot.eu-blue)](https://miquelnebot.eu)
[![License](https://img.shields.io/badge/Licencia-CC_BY--SA_4.0-green)](LICENSE)
[![Descarga MD](https://img.shields.io/badge/Descarga_guía-Español-yellow)](https://raw.githubusercontent.com/miquelnebotaragon/guia_basica_git/refs/heads/main/README.md)
![Guía básica Git para Github](./static/git_para_github.png)
## Crear repositorio local y subirlo a GitHub
### Flujo de trabajo

1. Configuración inicial

Antes de empezar, Git necesita saber quién eres para firmar tus avances.

❗ Atención: Solo será necesario realizar este paso la primera vez.
```bash
git config --global user.name "Tu nombre" # No es el nombre de usuario, es un nombre descriptivo para firmar los "commit". Por ejemplo: "Miquel hizo este cambio"
git config --global user.email "tu@email.es"
```
2. Inicializamos el repositorio de Git en nuestro equipo local
```bash
git init
```
➡️ De esta manera arranca el control de versiones en la carpeta de nuestro proyecto.

❗ Atención: De manera predeterminada y sin que sea necesaria intervención alguna por nuestra parte, se creará una carpeta oculta de nombre ".git" que será la que contendrá todo lo necesario para sincronizar con el repositorio remoto. ¡No la edites manualmente ni la borres!  

3. Añadir archivos al repositorio
```bash
git add .
```
➡️ En este comando, el argumento punto (.) indica que quieres incluir todos los cambios del directorio actual.

➕ Tip: Usa `git status` antes de este paso para ver qué archivos están modificados.

4. Confirmar los cambios (crear *commit*)
```bash
git commit -m "Comentario para identificar la primera subida, por ejemplo Subida inicial"
```
➡️ Crea una "fotografía" o estado permanente de tu proyecto en ese momento exacto.

5. Renombrar la rama de trabajo principal
```bash
git branch -M main
```
➡️ GitHub utiliza por defecto el nombre "main". Este comando asegura que tu rama local se llame igual (antiguamente se usaba "master").

6. Vincular con GitHub (remoto)
```bash
git remote add origin https://github.com/usuario/nombre_del_repo.git
```
❗ Atención: Antes de ejecutar este paso, debes haber creado el repositorio en la web de GitHub (vacío, sin README ni licencia) para obtener la correspondiente URL que habremos utilizado aquí.

➡️ Estableces el puente entre tu PC y el servidor. El nombre "origin" es el estándar para referirse al servidor principal.

7. Subir el repositorio
```bash
git push -u origin main
```
➡️ El parámetro -u vincula tu rama local con la remota. En las próximas subidas, solo necesitarás escribir git push.

## 🧩 Resumen
```bash
git init
git add .
git commit -m "Carga inicial de archivos"
git branch -M main
git remote add origin https://github.com/miquelnebotaragon/mi_primer_repo.git # Solicitará loguearse en GitHub
git push -u origin main
```
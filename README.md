Curso: F4101 Lenguajes para aplicaciones comerciales 
Estudiante: Keinth Viales Reyes
Este documento detalla la secuencia de comandos de Git ejecutados para completar el laboratorio sobre control de versiones.


# Inicialización del repositorio y cambio de rama principal 
git init 
git branch -M main

# Primer commit de la estructura 
git add . 
git commit -m "Estructura inicial del proyecto" 

# Ver historial resumido 
git log --oneline 

# Creación y cambio a rama desarrollo 
git checkout -b desarrollo 

# (Después de modificar index.html con Bootstrap) 
git add index.html 
git commit -m "Agrega contenido en index" 

# Unir rama desarrollo a main 
git checkout main 
git merge desarrollo 

# Ver diferencias en styles.css sin hacer commit 
git diff styles.css

# Commit temporal y eliminación del mismo 
git add styles.css 
git commit -m "Cambio temporal" 
git reset --hard HEAD~1 

# Recuperación del último commit eliminado 
git reflog
git reset --hard <ID_DEL_COMMIT> 

# Creación de archivo .gitignore

# Contenido: *.log, .env, .vscode/ 
git add .gitignore 
git commit -m "Agrega gitignore"

# Vinculación y subida al repositorio remoto 
git remote add origin URL DEL REPOSITORIO
git push -u origin main

# Crear nueva rama login y subir archivo login.html 
git checkout -b login 
git add login.html 
git commit -m "Agrega login" 

# Subir rama login al servidor 
git push origin login 


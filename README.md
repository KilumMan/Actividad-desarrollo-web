Guía de Supervivencia: Mi Primer Commit Colaborativo

Actividad: Registro de Asistencia en GitHub

Esta guía te ayudará a subir tu nombre al repositorio grupal sin morir en el intento (y sin borrar a nadie en el proceso).

1. Preparación (Solo la primera vez)

Antes de empezar, asegúrate de que Git sepa quién eres. Abre tu terminal (CMD, PowerShell o Git Bash) y escribe:

git config --global user.name "Tu Nombre Real"
git config --global user.email "tu-correo@ejemplo.com"

2. El camino (Paso a Paso)

1. Clonar el repositorio: (Solo si no lo has hecho)
git clone [URL_DEL_REPOSITORIO]
cd [NOMBRE_DE_LA_CARPETA]


2. Sincronizar (¡VITAL!): Trae los nombres que otros ya subieron.

git pull origin main


3. Editar: Abre `asistencia.py`, ve al final y agrega:

print("✅ Tu Nombre Aquí")

5. Preparar el envío:

git add asistencia.py
git commit -m "Registro de [Tu Nombre]"


5. Subir a GitHub:

git push origin main

3. Resolución de Problemas

A. El error "Rejected"

Si al hacer `push` te sale un texto rojo que dice `error: failed to push some refs`, significa que alguien más subió su nombre mientras tú escribías el tuyo.

Solución: Escribe `git pull origin main`. Si se abre un editor de texto raro (Vim), presiona la tecla `Esc`, escribe `:q` y dale a `Enter`. Luego intenta el `git push` de nuevo.

B. Conflicto de Merge

Si Git dice `CONFLICT (content): Merge conflict in asistencia.py`:

1. Abre el archivo. Verás unas marcas raras: `<<<<<<< HEAD`.
2. Borra las marcas y acomoda los nombres para que se vean bien (uno debajo del otro).
3. Guarda, y haz de nuevo: `git add`, `git commit` y `git push`.

4. Plan de Emergencia

Si la terminal te da problemas de autenticación o el internet va muy lento:

1. Entra al link del repositorio en tu navegador.
2. Haz clic en el archivo `asistencia.py`.
3. Haz clic en el icono del lápiz (Edit).
4. Escribe tu línea al final del archivo.
5. Haz clic en el botón verde "Commit changes..." arriba a la derecha.

Tips

* No borres nada
* Estatus Si no sabes en qué paso vas, escribe `git status`.
